# Could not find 'bundler' (1.16.5)

bundle update is a command provided by the Bundler gem which will update all your gem dependencies to their latest versions. Providing you have a Gemfile.lock pre-existing, running bundle install will only install the versions specified in the Gemfile.lock and will complain that you have incompatible versions:

```sh
rvm default ruby-2.6.1
RAILS_ENV=development bundle update --bundler
```


# gems/devise-4.2.0/app/controllers/devise/sessions_controller.rb:5: syntax error, unexpected '{'
- [*** Works *** Stack Overflow](https://stackoverflow.com/questions/55945489/rails-syntaxerror-unexpected-in-sessionscontroller)

```sh
RAILS_ENV=development bundle update devise
RAILS_ENV=development bundle install
```


# Bundler could not find compatible versions for gem "bundler":
  In Gemfile:
    rails (~> 5.0.1) was resolved to 5.0.1, which depends on
      bundler (>= 1.3.0, < 2.0)

  Current Bundler version:
    bundler (2.1.4)
This Gemfile requires a different version of Bundler.
Perhaps you need to update Bundler by running `gem install bundler`?

Could not find gem 'bundler (>= 1.3.0, < 2.0)', which is required by gem 'rails (~>
5.0.1)', in any of the sources.

- [Official Bundler update](https://bundler.io/guides/bundler_2_upgrade.html)

## Check the Bundle version
```sh
grep -A 1 "BUNDLED WITH" Gemfile.lock
```

## Modify Gemfile.lock

```rb
from bundler (>= 1.3.0, < 2.0) to bundler (>= 1.3.0, <= 2.1.4)
# run 
RAILS_ENV=development bundle update devise

```