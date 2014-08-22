#!/bin/sh

indent() {
  sed -u 's/^/       /'
}

echo "-----> Install ffmpeg"
BUILD_DIR=$1
VENDOR_DIR="vendor"
DOWNLOAD_URL="http://flect.github.io/heroku-binaries/libs/ffmpeg.tar.gz"

echo "DOWNLOAD_URL = " $DOWNLOAD_URL | indent

cd $BUILD_DIR
mkdir -p $VENDOR_DIR
cd $VENDOR_DIR
curl -L --silent $DOWNLOAD_URL | tar xz

echo "exporting PATH and LIBRARY_PATH" | indent
PROFILE_PATH="$BUILD_DIR/.profile.d/ffmpeg.sh"
mkdir -p $(dirname $PROFILE_PATH)
echo 'export PATH="$PATH:$HOME/vendor/ffmpeg/bin"' >> $PROFILE_PATH
echo 'export LD_LIBRARY_PATH="$LD_LIBRARY_PATH:$HOME/vendor/ffmpeg/lib"' >> $PROFILE_PATH
