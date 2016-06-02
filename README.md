# [emscripten](http://kripken.github.io/emscripten-site/)-playground

learn and experiment with [emscripten](http://kripken.github.io/emscripten-site/)

## Running

1. Follow the [Download and install](http://kripken.github.io/emscripten-site/docs/getting_started/downloads.html) instructions
2. Run the following

```sh
# base install location
# ~/dev/emsdk_portable

# source in environment to update PATH and make tools available
$ source ~/dev/emsdk_env.sh

# needed to add python2 symlink (see https://github.com/kripken/emscripten/issues/3872)
$ cd /usr/local/bin
$ ln -s /usr/bin/python2.7 python2

# compile c file to javascript -> generates output/hello_world.js
$ emcc hello_world.c -o output/hello_world.js
$ node output/hello_world.js

# compile c file and generate html to view it -> generates output/hello.html and output/hello.js
# NOTE: overwrites
$ emcc hello_world.c -o output/hello.html
```
