# The Rails File Structure

You should be relatively familiar with the Rails file structure having basically built a version of Rails using Sinatra. Below is the standard file structure of a Rails 4.2 app, which is automatically generated when you generate a new rails app with `rails new`. Look for comments explaining some new directories and files you may not be familiar with.

```bash
app_name/
├── app
│   ├── assets # For js and css that you've written
│   │   ├── images
│   │   ├── javascripts
│   │   │   └── application.js # A manifest file for the asset pipeline
│   │   └── stylesheets
│   │       └── application.css # A manifest file for the asset pipeline
│   ├── controllers
│   │   ├── application_controller.rb # From which all controllers inherit from
│   │   └── concerns # For keeping reusable code that applies to all controllers
│   ├── helpers # For view helper modules
│   │   └── application_helper.rb 
│   ├── mailers # For code pertaining to sending emails
│   ├── models
│   │   └── concerns # For keeping reusable code that applies to all models
│   └── views
│       └── layouts
│           └── application.html.erb # For HTML that will be on all web pages. <head> tag for example
├── bin # Rails command line tools; we have a few extras with flatiron-rails
│   ├── bundle
│   ├── rails
│   ├── rake
│   ├── setup
│   └── spring
├── config # Configuration code
│   ├── application.rb # Loads rails gems, gems for the specified Rail.env, and configures the application
│   ├── boot.rb # Sets up Bundler and load paths
│   ├── database.yml # Database configuration
│   ├── environment.rb # Runs all initializers
│   ├── environments # Settings for specific environments, production, testing, development, etc. 
│   │   ├── development.rb
│   │   ├── production.rb
│   │   └── test.rb
│   ├── initializers # These configuration files load after the framework and gems
│   │   ├── assets.rb
│   │   ├── backtrace_silencers.rb
│   │   ├── cookies_serializer.rb
│   │   ├── filter_parameter_logging.rb
│   │   ├── inflections.rb
│   │   ├── mime_types.rb
│   │   ├── session_store.rb
│   │   └── wrap_parameters.rb
│   ├── locales # For language/international configuration. If you want your app in multiple languages!
│   │   └── en.yml # English localization file
│   ├── routes.rb # Where we build our routes for requests to our app
│   └── secrets.yml # Rails' built in secret key management
├── config.ru # For Rack-based servers to start the application
├── db # database files. Migrations, seed files, etc.
│   └── seeds.rb
├── lib # External libraries go here
│   ├── assets
│   └── tasks
├── log # Error logs live here
├── public # files for the web server that don't change. Static web pages.
│   ├── 404.html
│   ├── 422.html
│   ├── 500.html
│   ├── favicon.ico
│   └── robots.txt
├── spec # all tests
│   ├── feature_helper.rb
│   ├── features
│   ├── rails_helper.rb # As of RSpec 3.x this replaces spec_helper
│   └── spec_helper.rb
├── tmp # Where Rails holds temporary files for immediate processing
│   └── cache
│       └── assets
├── vendor # Where we keep third-party assets (like Bootstrap Themes)
│   └── assets
│       ├── javascripts
│       └── stylesheets
├── Gemfile
├── Gemfile.lock
├── README.rdoc
└── Rakefile
```

