# FeatureFlags

Manage (turn on/off) different features in your rails app.

## Installation

Add this line to your application's Gemfile:

    gem 'feature_flags'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install feature_flags

## Usage

with feature_flags gem you can easily manage different features in your rails application.You can turn on/off features.


    rails generate feature_flags:install

this will generate 3 files,
1) initializer file in config/initializer/feature_flags.rb
2) migration file for Feature model
3) Feature.rb 
then do 
    
    rake db:migrate
    

##############################################################################
    FeatureFlags.enabled?(:feature_name)      To check whether particular feature is enabled or not 

    FeatureFlags.enable_all                   To enable all features in your app.

    FeatureFlags.disable_all                  To disable all features in your app.

    FeatureFlags.set_disabled(:feature_name)  To disable feature in your app.

    FeatureFlags.create_and_enable(:feature_name)  To create and enable feature
    
    FeatureFlags.enable(feature_name)         To enable feature

##############################################################################

In feature_flags.rb initializer file you can mention which layout to use for view

    FeatureFlags.configure do |config|
      config.layout = "application" 
    end
    
##############################################################################

If you want to generate views use,

    rails generate feature_flags:views


For more info:[Click Here](http://ror-tech.blogspot.in/2013/08/manage-different-features-in-our-ruby.html)

Here are some screenshots,
main index view

![ScreenShot](https://raw.github.com/pandurang90/feature_flags/master/index.png)

adding new feature to rails application

![ScreenShot](https://raw.github.com/pandurang90/feature_flags/master/new.png)

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
