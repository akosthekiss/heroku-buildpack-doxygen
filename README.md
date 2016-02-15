# Doxygen Buildpack for Heroku

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpack) for
the automatic generation of [Doxygen](http://www.doxygen.org) documentation of
software projects.

## Usage

Since this buildpack only generates the documentation, it requires another
buildpack to deploy the app. By default, the PHP buildpack is used: if the
project root contains no `Procfile`, a default one is generated during the
compile phase that starts `heroku-php-apache2`.

A multi-buildpack configuration can look like the following:

```bash
$ heroku buildpacks:set https://github.com/akiss77/heroku-buildpack-doxygen.git
$ heroku buildpacks:add --index 2 heroku/php
```

## Licensing

See [LICENSE](LICENSE) for copyright and licensing.
