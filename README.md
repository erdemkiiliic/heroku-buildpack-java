Heroku buildpack for Java [![CI](https://github.com/heroku/heroku-buildpack-java/actions/workflows/ci.yml/badge.svg)](https://github.com/heroku/heroku-buildpack-java/actions/workflows/ci.yml)
=========================

If you want to have Maven available to use at runtime in your application, you should copy it from the cache directory to the build directory by adding the following lines to the compile script. I updated the current java buildpack with these lines and created this repo. So, you can use this repo. <br><br>
<code>for DIR in ".m2" ".maven" ; do
 cp -r $CACHE_DIR/$DIR $BUILD_DIR/$DIR
done</code>


example procfile: <br>
<b>worker: .maven/bin/mvn compile</b>
