# heroku-buildpack-jq

> [!WARNING]
> JQ is [now installed](https://devcenter.heroku.com/changelog-items/2893) in both Heroku's build and run images.
> As such, this buildpack is no longer required to use JQ on Heroku.

Use [Heroku multi-buildpacks](https://devcenter.heroku.com/articles/using-multiple-buildpacks-for-an-app).

For example:

```
$ heroku buildpacks:add --index 1 https://github.com/chrismytton/heroku-buildpack-jq.git
$ heroku buildpacks
=== app-name Buildpack URLs
1. https://github.com/chrismytton/heroku-buildpack-jq.git
2. heroku/python
```

Perform a deploy to rebuild with multi-buildpacks.

You can confirm `jq`'s installation by running:

```
$ heroku run which jq
/app/vendor/jq/bin/jq
```

That confirms it's installed and in the `PATH`.
