# Memamug

An open-source app which helps you remember people you'd normally forget. See the live version at [memamug.com](http://www.memamug.com).

This app was built to demonstrate how to write a simple web-app, without resorting to a cliché to-do list. I'll be writing a number of tutorials to explain how to build this app, from creating the initial directory structure to deploying it live. Follow [@james_k_nelson](https://twitter.com/james_k_nelson) to keep updated.

## Getting Started

This server is built with [rails-api](https://github.com/rails-api/rails-api), so the installation process mostly follows that for a standard rails application, with a few differences:

* It uses the `uuid-ossp` PostgreSQL extension. Add this by typing `create extension "uuid-ossp";` into `psql` once your database is setup.
* You'll need to rename `.env-example` to `.env` and add your S3 and Facebook Login API keys.env`

Other than that, you can just follow the usual rails setup process:

* Setup your `config/database.yml`
* Run `rake db:migrate`

Once setup, install `foreman` and `mailcatcher` gems:

```
gem install foreman mailcatcher
```

Then start your server with

```
mailcatcher
foreman start
```

Then move on to getting [memamug-client](https://github.com/jamesknelson/memamug-client) working, so you can use it!

Need more specific details? I'll be writing more soon. Follow [@james_k_nelson](https://twitter.com/james_k_nelson) to stay up to date.
