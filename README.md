elasticbeanstalk-puma-rails4
============================

Quick store for my collection of .ebextension scripts that I use to get a Rails 4.1 app running on AWS ElasticBeanstalk (Puma + Ruby 2.0)

These scripts are really just pasted together from different sources and are not perfect. Feel free to fork and clean-up if you have the time.

__000fixrake.config__ - for some reason EB does not run migrations or precompile. This places some predeploy scripts to do this before starting puma.

__001fixpermissions.config__ - fixes permissions for the $GEM_HOME folder

__01packages.config__ - installs some basic yum packages (ImageMagick, gcc, libxml + libxslt, mysql, ruby-devel) and sets some config settings for bundler

__002bundle_pack.config__ - *magic*. Packing all gems to vendor/cache to make sure they are loaded correctly by the app.

__02nginx.config__ - nginx config to allow uploads of max. 4GB

__04rubylibs.config__ - fix RUBYLIB path
