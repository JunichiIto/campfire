# campfire
Sample app from https://www.youtube.com/watch?v=n0WUjGkDFS0

## How to run

Install Redis beforehand.

```
brew install redis
```

Clone this repository, and:

```
bundle install
bundle exec rails db:migrate RAILS_ENV=development
redis-server
rails server
open http://localhost:3000
```

You should be able to chat like this:

![c7ERfXIREG.gif](https://qiita-image-store.s3.amazonaws.com/0/7465/b58e0bc4-eb80-3176-9baf-3009323c4485.gif "c7ERfXIREG.gif")

### Deploy to Heroku

NOTE: This project is experimental. It might be risky for production. See also [this pull request](https://github.com/JunichiIto/campfire/pull/3) (in Japanese).

```
heroku create
heroku addons:create heroku-redis
git push heroku master
heroku run rails db:migrate
heroku open
```

## License

MIT License.
