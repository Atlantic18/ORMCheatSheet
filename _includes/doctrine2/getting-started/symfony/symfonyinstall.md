First we need to install the plugin from SVN with the following command from the root of your project:

~~~
$ svn co http://svn.symfony-project.org/plugins/sfDoctrinePlugin/branches/1.3-2.0/ plugins/sfDoctrine2Plugin
~~~

Now you just need to enable the plugin:

~~~php
class ProjectConfiguration extends sfProjectConfiguration
{
  public function setup()
  {
    $this->enablePlugins('sfDoctrine2Plugin');
  }
}
~~~
