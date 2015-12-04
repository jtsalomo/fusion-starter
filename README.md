# Ultimate React Starter Kit
React is a lightweight library, so to build real apps, you need more. This starter kit offers a comprehensive framework for building fast, testable applications with React. It offers a rich development experience including:

* [React](https://facebook.github.io/react/) for rich, fast, client-side components  [Pluralsight Course](https://app.pluralsight.com/library/courses/react-flux-building-applications/table-of-contents)  
* [Redux](http://redux.js.org) for data flows (An alternative to [Facebook's Flux](https://facebook.github.io/flux/docs/overview.html) - Useful on larger apps with complex data flows). [Tutorial](https://egghead.io/series/getting-started-with-redux)  
* [Babel](http://babeljs.io) for compiling ES6 to ES5. Enjoy the new version of JavaScript today. [ES6 REPL](https://babeljs.io/repl/) [ES6 vs ES5](http://es6-features.org) [ES6 Katas](http://es6katas.org) [Pluralsight course](http://www.pluralsight.com/courses/javascript-fundamentals-es6)  
* [Browserify](http://browserify.org/) for bundling all JS including npm packages for use in the browser  
* [Mocha](http://mochajs.org) for automated tests with [Chai](http://chaijs.com/) for assertions and [Cheerio](https://www.npmjs.com/package/cheerio) for DOM testing without a browser.
* [Istanbul](https://github.com/gotwarlost/istanbul) for code coverage data
* [TrackJS](http://trackjs.com) for JS error tracking in production  
* [ESLint](http://eslint.org/) for linting JS. Using [eslint-plugin-react](https://github.com/yannickcr/eslint-plugin-react) for additional React specific linting rules.
* [SASS](http://sass-lang.com/) for styling  
* [Editor Config](http://editorconfig.org) to support consistent editor settings. [IDE Plugins](http://editorconfig.org/#download)
* [BrowserSync](http://www.browsersync.com) for serving the app via a lightweight HTTP server that supports mobile testing and debugging.
* [Gulp](http://gulpjs.com) glues all this together in a handy automated build [Pluralsight course](https://app.pluralsight.com/library/courses/javascript-build-automation-gulpjs)  

The starter kit includes a working example app that puts all of the above to use.

## Get Started
1. **[Install Node](https://nodejs.org).**
2. **[Install Git](https://git-scm.com/downloads).**
3. **Clone the project from GitHub.**  `git clone https://github.com/coryhouse/vin-javascript-starter-kit.git`.
4. **Install Packages.** `npm install`. 
5. **Run Gulp.** Type `gulp` in the root of your project (same dir where you just ran `npm install`). This will run the automated build process, start up a webserver, and open the application in your default browser. When doing development with this kit, you'll want to keep the command line open at all times so that your code is rebuilt and tests run automatically every time you hit save.
6. **Review the example app.** This starter kit includes a working example app that calculates fuel savings. Note how all source code is placed under /src. Tests are placed alongside the file under test. The final built app is placed under /dist. These are the files you run in production.
7. **Delete the example app files.** Once you're comfortable with how the example app works, you can delete those files and begin creating your own app. You can always refer to this repo for the example app code that you deleted.

## Testing
Streamlined automated testing is a core feature of this starter kit. All tests are placed in files that end in .spec.js. They are placed in the same directory as the file under test. Why?
+ The existence of tests is highly visible. If a corresponding .spec file hasn't been created, it's obvious.
+ Easy to open since they're in the same folder as the file being tested.
+ Easy to create new test files when creating new source files.
+ Short import paths are easy to type and less brittle.
+ As files are moved, it's easy to move tests alongside.

## Code Coverage
Code coverage is calculated and reported via Istanbul. To view your current code coverage, run `gulp coverage`. This will open a tab in your default browser which displays code coverage statistics.

## Debugging
When you run the default Gulp task by typing `gulp`, no JS is minified. Why? Because minifying slows the build. For production or in-browser debugging, you'll want to minify the JS via `gulp build`.  A [sourcemap](http://www.html5rocks.com/en/tutorials/developertools/sourcemaps/) is generated by the `gulp build` task to enable easy debugging of minified JS. This means your original JS source will be displayed in your browser's dev console.

###Tips for Debugging Via Sourcemaps: 
1. Browsers vary in the way they allow you to view the original source. Chrome automatically shows the original source if a sourcemap is available. Safari, in contrast, will display the minified source and you'll [have to cmd+click on a given line to be taken to the original source](http://stackoverflow.com/questions/19550060/how-do-i-toggle-source-mapping-in-safari-7).
2. Do **not** enable serving files from your filesystem in Chrome dev tools. If you do, Chrome (and perhaps other browsers) may not show you the latest version of your code after you make a source code change. Instead **you must close the source view tab you were using and repoen it to see the updated source code**. It appears Chrome clings to the old sourcemap until you close and reopen the source view tab. To clarify, you don't have to close the actual tab that is displaying the app, just the tab in the console that's displaying the source file that you just changed.
3. If the latest source isn't displaying the console, force a refresh. Sometimes Chrome seems to hold onto a previous version of the sourcemap which will cause you to see stale code.

##Potential Features Coming Soon...
* Streamlined gulpfile via gulp-sequence (or via Node Scripts)
* Babel 6 upgrade
* Sass Linting
* Cache busting bundle naming
* Hot Reloading
* Growl support
* GraphQL and Relay
* Organize with ops to run prod build step and utilized the resulting code in QA and Prod
* Use Yeoman / npm for easy updates and config
* Bootstrap
* Kendo
* Superagent or jQuery for API calls
* Authentication example  
* Isomorphic Rendering  

#Alternative Names
* React Foundation
* Ultimate React Starter
* React Redux Starter
* React Framework
* React Boiler
* Comprehensive, Complete, Framework
* Stilts
* Slingshot
