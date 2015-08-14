# Laravel Elixir Uglify

This package allows you to uglify your javascript files. This is useful when you are loading scripts asynchronously.

## Installation

First you need to install this package.

```sh
npm install --save-dev laravel-elixir-js-uglify
```

Then require this package into your `gulpfile.js`.

```js
var Elixir = require('laravel-elixir');
require('laravel-elixir-js-uglify');
```

Then call the `uglify` method from your mix.

The `uglify` method can take up to four arguments:

  1. `src` (required): The files to uglify.
  2. `outputPath` (optional): The output folder (defaults to `public/js`).
  3. `baseDir` (optional): The folder in which your js files are stored (defaults to `resources/assets/js`).
  4. `options` (optional):  Options object passed to the `gulp-uglify` task.

This task defines a watcher for the path defined in `src`.

Sample code:

```js
Elixir(function(mix) {
    mix.uglify('**/*.js', 'public/js', 'resources/assets/js');
});
```