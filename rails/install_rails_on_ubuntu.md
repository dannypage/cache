# Install Rails on Ubuntu

```
$ gem install bundle
$ bundle install
$ bundle exec rails s
$ yarn install --check-files
```

Needed Yarn, so time to install that:

```
$ curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
$ echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
$ sudo apt-get update && sudo apt-get install yarn
$ yarn install --check-files
```

Needed Postgres to be running. #TODO finish this:
```
$ sudo apt install postgresql postgresql-contrib
$ bundle exec rake db:setup
$  service postgresql status
$  bundle exec rake db:setup
```

Work in progress, as I've still not gotten this to work on first try. 
