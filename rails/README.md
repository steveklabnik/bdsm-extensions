# BDSM Rails Extension

The Rails extension is used to manage all aspects of a Ruby/Rails
application project deployment as a user.

For example, if the project name is 'appx' then for deployment
you would typically create an 'appx' user on the server with
home directory of /home/appx.

An example walkthrough of using BDSM Rails extension in conjunction
with other extensions (below) to manage an application deployment.

    root# bdsm install rails deploy unicorn nginx

    appx$ bdsm bdsmrc
    appx$ vim ~/.bdsmrc # Adjust any settings necessary, set repo url.
    appx$ bdsm rails setup
    appx$ vim ~/shared/config/database.yml # Tune your database.
    appx$ bdsm deploy # Deploy the applicatoin using the 'deploy' ext.
    appx$ cd ~/current
    appx$ gem install bundler && bundle install # If you swing that way.
    appx$ bdsm unicorn install
    appx$ bdsm rails console
    appx$ bdsm unicorn start # If console loaded properly, start er up!

    root# bdsm nginx install
    root# bdsm nginx server appx


