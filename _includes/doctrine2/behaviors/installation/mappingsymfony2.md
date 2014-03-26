If you use **translatable**, **tree** or **loggable**
extension you will need to map those abstract mappedsuperclasses. Add mapping info to your `doctrine.orm` configuration, edit `app/config/config.yml`:

```YAML
doctrine:
    dbal:
# your dbal config here

    orm:
        auto_generate_proxy_classes: %kernel.debug%
        auto_mapping: true
# only these lines are added additionally 
        mappings:
            translatable:
                type: annotation
                alias: Gedmo
                prefix: Gedmo\Translatable\Entity
                # make sure vendor library location is correct
                dir: "%kernel.root_dir%/../vendor/gedmo/doctrine-extensions/lib/Gedmo/Translatable/Entity"
```

After that, running **php app/console doctrine:mapping:info** you should see the output:

```
Found 3 entities mapped in entity manager default:
[OK]   Gedmo\Translatable\Entity\MappedSuperclass\AbstractPersonalTranslation
[OK]   Gedmo\Translatable\Entity\MappedSuperclass\AbstractTranslation
[OK]   Gedmo\Translatable\Entity\Translation
```

**Note:** there is **Gedmo\Translatable\Entity\Translation** which is not a super class, in that case
if you create doctrine schema, it will add **ext_translations** table, which might not be useful
to you also. To skip mapping of these entities, you can map **only superclasses**

```YAML
mappings:
    translatable:
        type: annotation
        alias: Gedmo
        prefix: Gedmo\Translatable\Entity
        # make sure vendor library location is correct
        dir: "%kernel.root_dir%/../vendor/gedmo/doctrine-extensions/lib/Gedmo/Translatable/Entity/MappedSuperclass"
```

The configuration above, adds a **/MappedSuperclass** into directory depth, after running
**php app/console doctrine:mapping:info** you should only see now:

```
Found 2 entities mapped in entity manager default:
[OK]   Gedmo\Translatable\Entity\MappedSuperclass\AbstractPersonalTranslation
[OK]   Gedmo\Translatable\Entity\MappedSuperclass\AbstractTranslation
```

To map every extension use:

```YAML
# only orm config branch of doctrine
orm:
    auto_generate_proxy_classes: %kernel.debug%
    auto_mapping: true
# only these lines are added additionally 
    mappings:
        translatable:
            type: annotation
            alias: Gedmo
            prefix: Gedmo\Translatable\Entity
            # make sure vendor library location is correct
            dir: "%kernel.root_dir%/../vendor/gedmo/doctrine-extensions/lib/Gedmo/Translatable/Entity"
        loggable:
            type: annotation
            alias: Gedmo
            prefix: Gedmo\Loggable\Entity
            dir: "%kernel.root_dir%/../vendor/gedmo/doctrine-extensions/lib/Gedmo/Loggable/Entity"
        tree:
            type: annotation
            alias: Gedmo
            prefix: Gedmo\Tree\Entity
            dir: "%kernel.root_dir%/../vendor/gedmo/doctrine-extensions/lib/Gedmo/Tree/Entity"
```