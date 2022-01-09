![license](https://camo.githubusercontent.com/7564c4f51086d05c91ab09865b0ab1eaf457f172/68747470733a2f2f696d672e736869656c64732e696f2f3a6c6963656e73652d6d69742d626c75652e737667)

# Heroku buildpack - Git get latest tag

This Heroku buildpack exports the latest git tag (retrieved using `git describe --tags --abbrev=0`) as an environment variable accessible by your app as `APP_VERSION` at runtime.

# Usage

This buildpack must be used in concert with one or more others. Heroku supports
[multiple buildpacks](https://devcenter.heroku.com/articles/using-multiple-buildpacks-for-an-app#adding-a-buildpack)
out of the box.

Order of buildpacks is important. You most likely want this first in order. For example:

```bash
heroku buildpacks:add --index 1 https://github.com/zivrio/heroku-buildpack-git-latest-tag.git
```
