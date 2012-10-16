Heroku buildpack: Vert.x
========================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpack) for [Vert.x](http://vertx.io/) apps.  

It was forked from blalor but I've changed it quite a bit.  This version uses vertx.1.2.3 and also uses the
'heroku way' of including JDK7 (taken from current buildpacks).  I also disabled the detect feature that inflicts 
a particular naming strategy on your app.  You now need a Procfile that runs vertx how you want to.

The resulting slug for a minimal app is reasonable at around 54mb.  

Usage
-----

Example usage:

    $ heroku create --buildpack https://github.com/carchrae/heroku-buildpack-vertx-jdk7.git

or if you want to add it after you create an app

    $ heroku config:add BUILDPACK_URL=https://github.com/carchrae/heroku-buildpack-vertx-jdk7

You must create a Procfile that calls vertx, such as:

Procfile:

    web: vertx run Main.java

