# Hello Build Pack

The Hello Build Pack will look for a file named `hello.txt` in the app root and
display its contents during push.

## Usage

Add this language pack to your `BUILDPACK_URL`.

    heroku config:add BUILDPACK_URL="http://github.com/heroku/heroku-buildpack-hello.git"
