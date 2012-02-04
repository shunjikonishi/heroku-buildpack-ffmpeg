Heroku buildpack: Hello
=======================

This is an example [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks).

Usage
-----

Example usage:

    $ ls
    hello.txt

    $ heroku create --stack cedar --buildpack http://github.com/heroku/heroku-buildpack-hello.git

    $ git push heroku master
    ...
    -----> Heroku receiving push
    -----> Fetching custom buildpack
    -----> HelloFramework app detected
    -----> Found a hello.txt

The buildpack will detect that your app has a `hello.txt` in the root. If this file has contents, it will be copied to `goodbye.txt` with instances of the world `hello` changed to `goodbye`.

Hacking
-------

To use this buildpack, fork it on Github.  Push up changes to your fork, then create a test app with `--buildpack <your-github-url>` and push to it.

For example, you can change the displayed name of the buildpack to `GoodbyeFramework`. Open `bin/detect` in your editor, and change `HelloFramework` to `GoodbyeFramework`.

Commit and push the changes to your buildpack to your Github fork, then push your sample app to Heroku to test.  You should see:

    -----> GoodbyeFramework app detected
