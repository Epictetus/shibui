Shibui for Compass
==================

To create your first project, you'll need to have the Shibui gem installed, this will include all the necessary dependencies.

To install locally
------------------

In Terminal:

* `git clone git://github.com/heroku/shibui.git`
* `cd shibui`
* `sudo gem build shibui.gemspec`
* `sudo gem install shibui-0.0.1.gem`

To create your first project
----------------------------

* `cd path/to/where-you-want-new-project`
* .scss syntax: `compass create <my_project> -r shibui --using shibui --force`
* .sass syntax: `compass create <my_project> -r shibui --using shibui --syntax sass --force`

Now you should have a new project folder created with the Shibui file structure, but with the awesome advantages of having all the css pre-processed with Sass.

To add Shibui to an existing project
------------------------------------

* Add `require "shibui"`
* `cd path/to/your-project`
* run: `compass install shibui`