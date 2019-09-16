This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) with Firefox.

To install it, from the command line:

```bash
$ heroku buildpacks:add http://github.com/yegor256/firefox-buildpack
```

You may also need [buitron/geckodriver-buildpack](http://github.com/buitron/geckodriver-buildpack)
if you are planning to use Selenium.

The binary will be at `/vendor/firefox/firefox`.
