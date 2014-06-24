# asamoah

> Opionated frontend setup for Browserify, stylus, nib and GNU Make.

An opionated setup for frontend development using [browserify](http://browserify.org/), [stylus](http://learnboost.github.io/stylus/), [nib](https://github.com/visionmedia/nib), [GNU Make](http://www.gnu.org/software/make/) and [git](http://git-scm.com/).

## Getting Started
```bash
$ git clone https://github.com/Hanse/asamoah
$ cd asamoah
$ rm -rf .git
$ git init
$ git commit -am "Initial commit"
$ npm install
```

Build the JS and CSS files by running
```bash
$ make
```

Try it in your browser
```bash
$ PORT=2345 make server
-> Server running on localhost:2345
```

## Directory Structure
All uncompiled JS and CSS/Stylus assets reside in the `assets/` directory. They are by default compiled into `public/app.js` and `public/app.css` respectively. This can be changed in the `Makefile`. Having compiled files in the public directory makes it trivial to serve this folder from [nginx]() without serving the source files for example.

## Watching For Changes
It can be cumbersome to run `make` for every change. A way to solve this is to use [visionmedia/watch]() for periodical runs:

```bash
$ watch make
```

## Compress JS and CSS files
JS and CSS files are by default compressed when `NODE_ENV` is set to something other than `development`.

```bash
NODE_ENV=production make
```

## License
MIT