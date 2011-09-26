# Hello Language Pack

The Hello Language Pack will look for a file named `hello.txt` in the app root and
display its contents during push.

## Usage

Add this language pack to your `LANGUAGE_PACK_URL`.

    heroku config:add LANGUAGE_PACK_URL="http://github.com/heroku/language-pack-hello.git"
