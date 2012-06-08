Heroku buildpack: Vert.x
========================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpack) for [Vert.x](http://vertx.io/) apps.

Usage
-----

Example usage:

    $ ls
    server.js

    $ heroku create --stack cedar --buildpack https://github.com/blalor/heroku-buildpack-vertx-jdk7.git
	
	$ git push heroku master

    -----> Heroku receiving push
    -----> Fetching custom build pack... done
    -----> Vert.x app detected
    -----> Installing Vert.x..... done

The buildpack will detect your app as a Vert.x project if it has a file called server.js. If you don't provide a Procfile, the build pack will default to launching your app with `vertx run server.js`
