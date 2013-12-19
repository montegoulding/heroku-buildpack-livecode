Apache+LiveCode build pack
========================

This is a build pack bundling LiveCode and Apache for Heroku apps.

Configuration
-------------

The config files are bundled with the build pack itself:

* conf/httpd.conf

Using the buildpack
-------------------

You can override the Heroku default buildpacks by specifying a custom buildpack in the BUILDPACK_URL config var:

    $ heroku config:set BUILDPACK_URL=https://github.com/montegoulding/heroku-buildpack-livecode

You can also specify a buildpack during app creation:

    $ heroku create myapp --buildpack https://github.com/montegoulding/heroku-buildpack-livecode

Your app needs to have an `index.lc` file in its root directory.

Hacking
-------

To change this buildpack, fork it on Github. Push up changes to your fork, then create a test app with --buildpack <your-github-url> and push to it.


Meta
----

Created by Monte Goulding based on the Apache+PHP buildpack by Pedro Belo.