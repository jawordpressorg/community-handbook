# Setting up a Local WordCamp.org Sandbox

If you’d prefer to develop your custom CSS and other content locally before adding it to WordCamp.org, or want to contribute to make the platform better, then the easiest way to setup a local sandbox is with [WordCamp.org’s Docker environment](https://github.com/WordPress/wordcamp.org/blob/production/.docker/readme.md).

It will automatically provision a local virtual server with the same code that runs WordCamp.org, as well as some sample content so you can see how things are setup behind the scenes.

After you [follow the instructions](https://github.com/WordPress/wordcamp.org/blob/production/.docker/readme.md) and can access the server, you can get started on your site by adding your content and CSS to the 2014.content.wordcamp.test demo site. You can also create a new site if you prefer, but that requires creating a new WordCamp post type on the Central site, modifying the VVV hosts file to add the domain name, etc, so it’s easier to just re-use the Content demo site.

Once you’re ready to launch the production site, you can use WordPress’s import/export tools to transfer most of your content, although you’ll still need to configure some things manually. Right now there isn’t a good way to sync back and forth, so we recommend that you wait until you’re ready to launch before you transfer everything to production, and then make any post-launch changes directly on production.

If you find any problems with this process, or have any ideas for making it better, please report them as [issues in the WordCamp.org repository](https://github.com/WordPress/wordcamp.org/issues).

If you’d like to check out an alternative to the Docker environment, there’s also [the Meta Environment](https://github.com/WordPress/meta-environment), and [a Chassis extension to setup a WordCamp.org environment](https://github.com/stuartshields/chassis-wordcamp). The Meta Environment contains an older version of the WordCamp environment, but is based on Vagrant/VVV, which may work better than Docker on Windows machines.

## More Resources & Alternative Approaches

*   [Local Development for WordCamp Websites](https://ryelle.codes/2016/07/18/local-development-for-wordcamp-websites/) by Kelly Dwan (WordCamp Boston)
*   [WordCamp US 2019 GitHub repo](https://github.com/wcus/wcus-2019/)
*   [WordCamp Seattle 2019 GitHub repo](https://github.com/iandunn/wordcamp-seattle-2019)
*   [WordCamp São Paulo 2019 GitHub repo](https://github.com/wordpress-sao-paulo/wordcamp-saopaulo-2019)
*   [CampSite-2017 theme style guide](https://github.com/lucijanblagonic/wceu-2018)
*   [WordCamp Europe 2018](https://github.com/lucijanblagonic/wceu-2018)

*   [To-do](# "To-do")