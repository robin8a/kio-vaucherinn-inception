# Could not find 'bundler' (1.16.5)

bundle update is a command provided by the Bundler gem which will update all your gem dependencies to their latest versions. Providing you have a Gemfile.lock pre-existing, running bundle install will only install the versions specified in the Gemfile.lock and will complain that you have incompatible versions:

```sh
RAILS_ENV=development bundle install
```