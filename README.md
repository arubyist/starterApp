# Starter App

Meant to be a "ready-made" starter app to which you can use to spin off for your own projects, and/or learn from so you can do it for yourself as well! =)

It will be set up with FactoryGirl, Database Cleaner, Capybara, RSpec, and Guard. 

(you can always add more to the Gemfile, and there are lots out there to explore!)


#### [FactoryGirl](https://github.com/thoughtbot/factory_girl_rails) 

It's an alternative to fixtures, and much better one to use. 

Very easy to set up, and to use in RSpec's testing process. 


#### [Capybara](https://github.com/teamcapybara/capybara) 


You use this to run integration tests. It can also be used for end-to-end testing as well. 

It can be used out of the box with RSpec. For the purposes of this starter app, all context is within RSpec framework, instead of Cucumber, Test::Unit, Minitest, Minitest::Spec, and etc. It is meant to be agnoistic, and fairly powerful to use. 

When it comes to writing test, you put your Capybara specs in spec/features folders. 

There are a lot of cheatsheets out there to keep around for Capybara's DSL. Here's a quick one which I just googled randomly for right now: [Capybara cheatsheet](http://www.railscook.com/recipes/capybara-cheat-sheet/) 

Suffice to say, there's a lot about Capybara out there. Spin off your apps, and explore! It doesn't have to be serious. Just go and have fun breaking apps and learning in the process. =) 

#### [RSpec](https://github.com/rspec/rspec-rails) 

It's meant for behavior-driven development (BBD). You write scenarios and test them. 

[Here's further information](http://rspec.info), check it out!

As mentioned in **changelog**, you set up the default files by running `rails g rspec:install`. Also have deleted the default test directory as it's not considered good practice to have both the default Rails testing libraries, and rspec as well. 


#### [Guard](https://github.com/guard/guard) 

Used to automate repetitive tasks. In context of texting, it's super useful as you don't keep to type 'bundle exec rspec.' It needs a Guardfile, and it has be set up. 

As mentioned in **changelog** at bottom, the [guard-rspec](https://github.com/guard/guard/wiki/Guard-Plugins#popular--featured--well-supported) plugin has been added and default configuration has been set up. You can now run 'bundle exec guard' and watch its magic =) 


#### [Database Cleaner](https://github.com/DatabaseCleaner/database_cleaner) 

Meant to keep your database clean. Especially useful when testing. It has three cleaning strategies: truncation, transaction, and deletion.

As mentioned in **changelog**, the default file is set up within `spec/support` directory, and adjusted a setting in `spec/rails_helper.rb` to turn off defaults Rails management. 


**Changelog**

April 13 - Have added guard-rspec plugin and set up default configuration file

April 15 - Have run `rails g rspec:install`. It sets up default files of `.rspec`, `spec`, `spec/spec_heper.rb`, and `spec/rails_helper.rb`. 

Also have added database_cleaner support file, and changed `config.use_transactional_fixtures = true` to `config.use_transactional_fixtures = false`. This simply tells RSpect to tell Rails not to manager the transactions. 

