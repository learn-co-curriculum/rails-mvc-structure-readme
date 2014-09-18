# The Rails File Structure

You should be relatively familiar with the Rails file structure having already built Rails out of Sinatra. Below is the standard file structure, which is automatically generated when you generate a new rails app with `rails new`. Look for comments explaining some new directories and files you may not be familiar with.

```bash
├── Gemfile
├── Gemfile.lock
├── Guardfile
├── README.md
├── Rakefile
├── app
│   ├── assets # for js and css that you've written
│   │   ├── images
│   │   ├── javascripts
│   │   │   └── application.js a manifest file for the asset pipeline
│   │   └── stylesheets
│   │       └── application.css.scss # a manifest file for the asset pipeline
│   ├── controllers
│   │   ├── application_controller.rb # from which all controllers inherit from
│   │   └── concerns # for keeping reusable code that applies to all controllers
│   ├── helpers # for view helper modules
│   │   └── application_helper.rb
│   ├── mailers # for code pertaining to mailer functionality
│   ├── models
│   │   └── concerns # for keeping reusable code that applies to all models
│   └── views
│       └── layouts
│           └── application.html.erb # for wrapping and yielding to views
├── bin # Rails command line tools; we have a few extras with flatiron-rails
│   ├── bundle
│   ├── deploy
│   ├── rails
│   ├── rake
│   ├── setup
│   └── spring
├── config # configuration code
│   ├── application.rb # loads rails gems, gems for the specified Rail.env, and configures the application
│   ├── boot.rb # sets up Bundler and load paths
│   ├── database.yml # database configuration
│   ├── environment.rb # runs all initializers
│   ├── environments # settings for specific environments
│   │   ├── development.rb
│   │   ├── production.rb
│   │   └── test.rb
│   ├── initializers # these configuration files load after the framework and gems
│   │   ├── assets.rb
│   │   ├── backtrace_silencers.rb
│   │   ├── cookies_serializer.rb
│   │   ├── filter_parameter_logging.rb
│   │   ├── inflections.rb
│   │   ├── mime_types.rb
│   │   ├── session_store.rb
│   │   └── wrap_parameters.rb
│   ├── locales # for language/international configuration
│   │   └── en.yml
│   ├── routes.rb # where we build our routes for requests to our app
│   └── secrets.yml # Rails' built in secret key management
├── config.ru # for Rack-based servers to start the application
├── db # db files, migrations, seed files
│   └── seeds.rb
├── lib # external libraries go here
│   ├── assets
│   └── tasks
├── log # Error logs live here
│   └── development.log
├── public # files for the web server that don't change
│   ├── 404.html
│   ├── 422.html
│   ├── 500.html
│   ├── favicon.ico
│   └── robots.txt
├── spec # all tests
│   ├── feature_helper.rb
│   ├── features
│   ├── rails_helper.rb # as of RSpec 3.x this replaces spec_helper
│   └── spec_helper.rb
├── tmp # where Rails holds temporary files for immediate processing
│   └── cache
│       └── assets
└── vendor # where we keep third-party assets (like Bootstrap Themes)
    └── assets
        ├── javascripts
        └── stylesheets
```

## Resources

* [The Rails 4 Way, Chapter 1: Rails Environments and Configuration](http://beta-library.herokuapp.com/books/the-rails-4-way#page=24)
