# Contributing to WordCamp.org

Do you have an idea to improve one of the custom tools on WordCamp.org? Do you want to report a bug? We welcome contributions from the community!

## New Features

If you’d like to add a new feature to WordCamp.org, then please follow the processes for [making feature requests](https://make.wordpress.org/community/feature-requests-for-community-sites/) and [building new features](https://make.wordpress.org/community/feature-requests-for-community-sites/design-implementation-process/).

## Bug Fixes

If you’d like to contribute **a bug fix**, then please follow these steps:

**Step One:** Search the [Meta Trac](https://meta.trac.wordpress.org) to check if a ticket already exists. If there is one, you can catch up on the progress of it and collaborate with those who are already working on it.

**Step Two:** If you want to contribute **a bug fix**, and there wasn’t an existing ticket, then create a new ticket. Describe the problem or idea you have in detail, and assign it to the “wordcamp.org” component.

**Step Three:** Gather feedback on the ticket and build a consensus for what action should be taken. [The Community team](https://make.wordpress.org/community) is the stakeholder for WordCamp.org and decides what contributions to accept, and [the Meta team](https://make.wordpress.org/meta) handles the technical implementation. You can ask for feedback on the ticket in their respective [Slack](https://chat.wordpress.org) channels.

**Step Four:** Setup your local development environment.

*   The easiest way to do this is to install the [WordPress Meta Environment](https://github.com/iandunn/wordpress-meta-environment), which is an add-on for Varying Vagrant Vagrants that automatically provisions a local copy of WordCamp.org’s source code, along with some sample data.
*   Alternately, you can build your own environment and then [clone the repo from GitHub](https://github.com/WordPress/wordcamp.org/).
    *   In addition to the code on GitHub, there are also a few plugins that live elsewhere. CampTix, [addons for CampTix](https://wordpress.org/plugins/search.php?q=camptix), and [Tagregator](https://wordpress.org/plugins/tagregator/) are available in the WordPress.org repository, and [SupportFlow](https://github.com/SupportFlow/supportflow) is available on GitHub. Although, as CampTix plugin has been closed as of August 15, 2019, it is now integrated into the WordCamp Central network.
    *   Check out [the `provision` folder](https://github.com/WordPress/meta-environment/tree/master/wordcamp.test/provision) in the Meta Environment for a sample database, `wp-config` file, and other useful code/scripts.

**Step Five:** Send a pull request on GitHub that implements the decisions reached in step three.

**Step Six:** Your patch will be reviewed by a developer on the Meta team, and they’ll either go ahead and commit the patch, or give you feedback on aspects that need to be improved before it can be committed.

## Resources

If you haven’t contributed to an open-source project before, the following resources should help you get started:

*   [Introduction to Trac](https://make.wordpress.org/core/handbook/trac/)
*   [Creating a Trac ticket](https://make.wordpress.org/core/handbook/working-with-trac/opening-a-ticket/)
*   [Contributing with Git](https://make.wordpress.org/meta/handbook/documentation/contributing-with-git/)

## Questions

If you have any questions or run into any problems, you can ask for help in the *[#meta-wordcamp](https://make.wordpress.org/community/tag/meta-wordcamp/)* channel on [Slack](https://chat.wordpress.org), or e-mail [support@wordcamp.org](mailto:support@wordcamp.org).

Here is [a quiz](https://wordpress.org/contributor-training/quiz/contributing-to-wordcamp-org-2/) on this article. Read [quizzes](https://make.wordpress.org/community/handbook/wordcamp-organizer/quizzes/) page if you have any questions about quizzes and how to navigate them.

*   [To-do](# "To-do")