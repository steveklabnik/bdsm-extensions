# BDSM Rails Extension

The Rails extension is used to manage all aspects of a Ruby/Rails
application project deployment as a user.

For example, if the project name is 'applicationx' then for deployment
you would typically create an 'applicationx' user on the server with
home directory of /home/applicationx.

You can setup

    root# bdsm install rails deploy unicorn
    user$ bdsm bdsmrc
    user$ vim ~/.bdsmrc # Adjust any settings necessary, set repo url.
    user$ bdsm rails setup
    user$ vim ~/shared/config/database.yml # Tune your database.
    user$ bdsm deploy # Assuming that all went well,
                        we can now deploy the applicatoin.
    user$ cd ~/current
    user$ gem install bundler && bundle install # If you swing that way.
    user$ bdsm unicorn install
    user$ bdsm rails console
    user$ bdsm unicorn start # If console loaded properly, start er up!
