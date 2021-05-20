# Local start on mac

```sh
# bundle update is a command provided by the Bundler gem which will update all your gem dependencies to their latest versions. Providing you have a Gemfile.lock pre-existing, running bundle install will only install the versions specified in the Gemfile.lock and will complain that you have incompatible versions:
rvm default ruby-2.6.1
RAILS_ENV=development bundle update --bundler
RAILS_ENV=development bundle install

```

# Database Postgres

- [RoR with postgres](https://www.digitalocean.com/community/tutorials/how-to-use-postgresql-with-your-ruby-on-rails-application-on-ubuntu-18-04)
- Configure .yml

```sh
# Server
rvm default ruby-2.6.1
RAILS_ENV=development bundle exec rake db:create
RAILS_ENV=development bundle exec rake db:migrate
RAILS_ENV=development bundle exec rake db:seed

# Console
RAILS_ENV=staging bundle exec rails console
RAILS_ENV=development bundle exec rails console
RAILS_ENV=production bundle exec rails console
```

# Devise

```sh
RAILS_ENV=development bundle update devise

```

## Gmail
- [Enable Less Security App](https://netcorecloud.com/tutorials/send-emails-with-ruby-on-rails/)
- [Sending Gmail](https://launchschool.com/blog/handling-emails-in-rails)


# Users

proveedor.juan.ochoa@yopmail.com/V4ucher1n2121
empresa_uno@yopmail.com/V4ucher1n2121
robin8a@gmail.com/V4ucher1n2121


# Testing
```sh
# Rails
rvm default ruby-2.6.1

# Test Server
RAILS_ENV=development bundle exec puma -p 8080
RAILS_ENV=production bundle exec puma -p 8080
RAILS_ENV=staging bundle exec puma -p 8080

RAILS_ENV=development yarn install --check-files
RAILS_ENV=production rails assets:precompile


```


# Heroku deploy
- [Heroku Getting Started](https://devcenter.heroku.com/articles/getting-started-with-rails5)

```sh
heroku create
#  ›   Warning: heroku update available from 7.41.0 to 7.53.1.
# Creating app... done, ⬢ arcane-cliffs-35060
# https://arcane-cliffs-35060.herokuapp.com/ | https://git.heroku.com/arcane-cliffs-35060.git
```