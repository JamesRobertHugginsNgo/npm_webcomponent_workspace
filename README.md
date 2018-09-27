# NPM Web Component Workspace

A starter project for ES6 web component development.

Includes JQuery 3, Bootstrap 4, Backbone, Underscore & Babel Polifill.

## Setup

1. Clone workspace repo and assign a new workspace name. Then check out the latest version.

   ``` shell
   git clone https://github.com/JamesRobertHugginsNgo/npm_webcomponent_workspace.git NEW_WORKSPACE
   git checkout 1.0.0
   ```

1. Remove the dot-git folder and everything inside.

   ``` shell
   rm -rf .git
   ```

1. Generate a new dot-git folder. Then assign the remote repository.

   ``` shell
   git init
   git remote add origin https://github.com/JamesRobertHugginsNgo/NEW_WORKSPACE.git
   ```

1. Update package.json by removing everything but "devDependencies" and "dependencies".

   From

   ``` json
   {
      "name": "npm_webcomponent_workspace",
      "description": "A starter project for ES6 web component development.",
      "version": "1.0.0",
      "main": "gulpfile.babel.js",
      "directories": {
        "test": "test"
      },
      "scripts": {
        "test": "echo \"Error: no test specified\" && exit 1"
      },
      "repository": {
        "type": "git",
        "url": "git+https://github.com/JamesRobertHugginsNgo/npm_webcomponent_workspace.git"
      },
      "keywords": [],
      "author": "",
      "license": "ISC",
      "bugs": {
        "url": "https://github.com/JamesRobertHugginsNgo/npm_webcomponent_workspace/issues"
      },
      "homepage": "https://github.com/JamesRobertHugginsNgo/npm_webcomponent_workspace#readme",
      "devDependencies": {
         "babel-cli": "^6.26.0",
         "babel-preset-env": "^1.7.0",
         "babel-register": "^6.26.0",
         "browserify": "^16.2.2",
         "del": "^3.0.0",
         "eslint": "^4.19.1",
         "gulp": "^4.0.0",
         "gulp-autoprefixer": "^5.0.0",
         "gulp-babel": "^7.0.1",
         "gulp-cssnano": "^2.1.3",
         "gulp-debug": "^4.0.0",
         "gulp-eslint": "^4.0.2",
         "gulp-less": "^4.0.1",
         "gulp-mustache": "^3.0.1",
         "gulp-rename": "^1.2.3",
         "gulp-sass": "^4.0.1",
         "gulp-sourcemaps": "^2.6.4",
         "gulp-uglify": "^3.0.0",
         "gulp-web-dependencies": "^1.1.2",
         "gulp-webserver": "^0.9.1",
         "merge-stream": "^1.0.1"
      },
      "dependencies": {
         "babel-polyfill": "^6.26.0",
         "backbone": "^1.3.3",
         "bootstrap": "^4.1.1",
         "jquery": "^3.3.1",
         "underscore": "^1.9.1"
      }
   }
   ```

   To

   ``` json
   {
      "devDependencies": {
         "babel-cli": "^6.26.0",
         "babel-preset-env": "^1.7.0",
         "babel-register": "^6.26.0",
         "browserify": "^16.2.2",
         "del": "^3.0.0",
         "eslint": "^4.19.1",
         "gulp": "^4.0.0",
         "gulp-autoprefixer": "^5.0.0",
         "gulp-babel": "^7.0.1",
         "gulp-cssnano": "^2.1.3",
         "gulp-debug": "^4.0.0",
         "gulp-eslint": "^4.0.2",
         "gulp-less": "^4.0.1",
         "gulp-mustache": "^3.0.1",
         "gulp-rename": "^1.2.3",
         "gulp-sass": "^4.0.1",
         "gulp-sourcemaps": "^2.6.4",
         "gulp-uglify": "^3.0.0",
         "gulp-web-dependencies": "^1.1.2",
         "gulp-webserver": "^0.9.1",
         "merge-stream": "^1.0.1"
      },
      "dependencies": {
         "babel-polyfill": "^6.26.0",
         "backbone": "^1.3.3",
         "bootstrap": "^4.1.1",
         "jquery": "^3.3.1",
         "underscore": "^1.9.1"
      }
   }
   ```

1. Reinitialize NPM. Then update package.json as desired.

   ``` shell
   npm init -y
   ```

1. Update README.md.

1. Perform first commit and push to origin.

   ``` shell
   git add .
   git commit -m "First Commit"
   git push -u origin master
   ```

1. Install dependencies.

   ``` shell
   npm install
   ```

## Development

All development are done on the src folder and built to the dist folder.

To build the project, issue the gulp command.

``` shell
gulp
```

To build the project and run a web server, use the serve parameter.

``` shell
gulp serve
```

<small>Note: Use CNTRL + C to end gulp serve.</small>

The web server, by default, opens the root folder.
To open on the dist folder, update gulpfile.babel.js

Change

``` JavaScript
const servePath = '.';
```

To

``` JavaScript
const servePath = '.\src\';
```

## Testing

Test related code should be writted in the test folder.
