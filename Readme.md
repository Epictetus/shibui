Shibui for Compass
==================

To create your first project, you'll need to have the [Shibui](http://en.wikipedia.org/wiki/Shibui) gem installed, this will include all the necessary dependencies.

To install locally
------------------

In Terminal:

* `git clone git@github.com:heroku/shibui.git`
* `cd shibui`
* `sudo gem build shibui.gemspec`
* `sudo gem install shibui-0.0.1.gem`

To create your first project
----------------------------

* `cd path/to/where-you-want-new-project`
* .scss syntax: `compass create <my_project> -r shibui --using shibui --force`
* .sass syntax: `compass create <my_project> -r shibui --using shibui --syntax sass --force`

Now you should have a new project folder created with the Shibui file structure, but with the awesome advantages of having all the css pre-processed with Sass.

To add Shibui to an existing Rails project
------------------------------------------

* Add it to your gemfile

```# Gemfile
group :assets do
  gem 'compass-rails'
  gem 'shibui', :git => 'git@github.com:heroku/shibui.git'
end```

* Add `require "shibui"` to your `application.rb`

In Terminal:

* `bundle`
* `bundle exec compass install shibui` or `bundle exec compass install shibui -x sass` if you prefer sass syntax instead of scss

To work on Shibui
-----------------

If you want to make changes to the Shibui plugin and see the effects locally follow these steps:

* `mkdir shibui-dojo`
* `cd shibui-dojo`
* `git clone git@github.com:heroku/shibui.git`
* `compass create sample-project -l shibui`
* `cd sample-project`
* `compass watch`

Shibui development with LiveReload
----------------------------------

[LiveReload](http://livereload.com/) is a great way to have your browser automagically refresh when changes to your project are made. Unfortunately LiveReload will not recognize changes to partials within a Compass extension. As a workaround:

- Use `compass watch` to generate updated stylesheets like described above.
- Add the project folder (`sample`) to LiveReload and uncheck the option Compile SASS.

The Compass watcher will take care of generating new CSS files and LiveReload will recognize changes to the CSS files and trigger a browser reload.