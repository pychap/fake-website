## For Lynda.com workflow - Gulp Git tutorial.
1.  previous items placeholder here
2.  Install gulp: `sudo npm install -g gulp`
3.  In workflows folder (main root folder), installed dev gulp `sudo npm install --save-dev gulp`   
4.  in same folder, create `gulpfile.js`  This tells gulp what to do when it runs. See gulpfile for details to add.
5.  Same root install `sudo npm install --save-dev gulp-util`
6.  Install plugin to tell gulp to process our coffee files `sudo npm install --save-dev gulp-coffee`
7.  run `gulp coffee`  
8.  Javascript to take rest of scripts and push to development folder to a single file via `gulp-concat` `sudo npm install --save-dev gulp-concat` add variable to `gulpfile.js` - `concat = require('gulp-concat')` - see file. Set up sources, create var - `jsSources`. 
9.  Our js files are using 2 libraries, jQuery to take care of JSON importing and Mustache.js to handle JavaScript templating. Easiest way is through Browserfify.
10. Install Browserify: `sudo npm install --save-dev gulp-browserify`
11. Install jQuery: `sudo npm install --save-dev jquery` (_notice no_ `gulp` _in command_)
12. Install Mustache: `sudo npm install --save-dev mustache` (_notice no_ `gulp` _in command_)
13. Install SASS and Compass, just need to install compass but needed to upgrade Ruby first, then install gems, then compass. Best to [refer to this execellent step-by-step article](http://railsapps.github.io/installrubyonrails-mac.html) as was hitting a wall up to this point.
14.  Added watch tasks, lines 42 - 46. Don't know at this point why watching is valuable. On line 48 `watch` is added to the default task (which _makes it better_).
15.  Install `gulp-connect` plugin. `npm install --save-dev gulp-connect`
16.  Added Live Reloading, also added `.pipe(connect.reload())` in several tasks. 
17.  In `scss` file, added `@import "compass/reset";` - this is a complete browser reset provided by compass!
18.  Added `html` and `json` watcher task with new variables `htmlSources` and `jsonSources` pointing to paths.