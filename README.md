This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks)
with Firefox 68.0.2.

To install it, from the command line:

```bash
$ heroku buildpacks:add http://github.com/yegor256/firefox-buildpack
```

You may also need [buitron/geckodriver-buildpack](http://github.com/buitron/geckodriver-buildpack)
if you are planning to use Selenium.

The binary will be at `/app/vendor/firefox/firefox`.

You will also need to have `heroku-community/apt` buildpack in order
to install all libraries required by Firefox:

```bash
$ heroku buildpacks:add heroku-community/apt
```

The content of your `Aptfile` should include this line:

```
libcairo2 libcairo-gobject2 libxt6 libsm6 libice6 libgtk-3-0
```

Should work.
