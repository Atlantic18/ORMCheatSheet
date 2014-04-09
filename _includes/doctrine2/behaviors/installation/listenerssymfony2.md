Edit and create an *yml* service file in your `app/config/doctrine_extensions.yml`

~~~YAML
# services to handle doctrine extensions
# import it in config.yml
services:
    # KernelRequest listener
    extension.listener:
        class: Acme\DemoBundle\Listener\DoctrineExtensionListener
        calls:
            - [ setContainer, [ @service_container ] ]
        tags:
            # translatable sets locale after router processing
            - { name: kernel.event_listener, event: kernel.request, method: onLateKernelRequest, priority: -10 }
            # loggable hooks user username if one is in security context
            - { name: kernel.event_listener, event: kernel.request, method: onKernelRequest }


    # Doctrine Extension listeners to handle behaviors
    gedmo.listener.tree:
        class: Gedmo\Tree\TreeListener
        tags:
            - { name: doctrine.event_subscriber, connection: default }
        calls:
            - [ setAnnotationReader, [ @annotation_reader ] ]
            
    gedmo.listener.translatable:
        class: Gedmo\Translatable\TranslatableListener
        tags:
            - { name: doctrine.event_subscriber, connection: default }
        calls:
            - [ setAnnotationReader, [ @annotation_reader ] ]
            - [ setDefaultLocale, [ %locale% ] ]
            - [ setTranslationFallback, [ false ] ]
    
    gedmo.listener.timestampable:
        class: Gedmo\Timestampable\TimestampableListener
        tags:
            - { name: doctrine.event_subscriber, connection: default }
        calls:
            - [ setAnnotationReader, [ @annotation_reader ] ]
    
    gedmo.listener.sluggable:
        class: Gedmo\Sluggable\SluggableListener
        tags:
            - { name: doctrine.event_subscriber, connection: default }
        calls:
            - [ setAnnotationReader, [ @annotation_reader ] ]
    
    gedmo.listener.sortable:
        class: Gedmo\Sortable\SortableListener
        tags:
            - { name: doctrine.event_subscriber, connection: default }
        calls:
            - [ setAnnotationReader, [ @annotation_reader ] ]
    
    gedmo.listener.loggable:
        class: Gedmo\Loggable\LoggableListener
        tags:
            - { name: doctrine.event_subscriber, connection: default }
        calls:
            - [ setAnnotationReader, [ @annotation_reader ] ]
~~~
**Note:** You will need to create `Acme\DemoBundle\Listener\DoctrineExtensionListener` if you use **loggable** or **translatable** behaviors. This listener will set the `locale used` from request and `username` to
loggable.

~~~php
<?php

// file: src/Acme/DemoBundle/Listener/DoctrineExtensionListener.php

namespace Acme\DemoBundle\Listener;

use Symfony\Component\HttpKernel\Event\GetResponseEvent;
use Symfony\Component\DependencyInjection\ContainerAwareInterface;
use Symfony\Component\DependencyInjection\ContainerInterface;

class DoctrineExtensionListener implements ContainerAwareInterface
{
    /**
     * @var ContainerInterface
     */
    protected $container;

    public function setContainer(ContainerInterface $container = null)
    {
        $this->container = $container;
    }

    public function onLateKernelRequest(GetResponseEvent $event)
    {
        $translatable = $this->container->get('gedmo.listener.translatable');
        $translatable->setTranslatableLocale($event->getRequest()->getLocale());
    }

    public function onKernelRequest(GetResponseEvent $event)
    {
        $securityContext = $this->container->get('security.context', ContainerInterface::NULL_ON_INVALID_REFERENCE);
        if (null !== $securityContext && null !== $securityContext->getToken() && $securityContext->isGranted('IS_AUTHENTICATED_REMEMBERED')) {
            $loggable = $this->container->get('gedmo.listener.loggable');
            $loggable->setUsername($securityContext->getToken()->getUsername());
        }
    }
}
~~~
Do not forget to import **doctrine_extensions.yml** in your **app/config/config.yml** etc.:

~~~YAML
# file: app/config/config.yml
imports:
    - { resource: parameters.yml }
    - { resource: security.yml }
    - { resource: doctrine_extensions.yml }

# ... configuration follows
~~~