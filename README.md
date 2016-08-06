# Python Nigeria community Site

### Gulp & BrowserSync Section
Ensure your have `node >= 4` on your system.

    git clone <repo>
    npm install -g gulp # if you haven't installed gulp
    npm install

Start up a local server 
<p>If you have python on your system</p>
    
    python -m SimpleHTTPServer 8002 # python2
    python -m http.server 8002 # python 3

Edit this line in the `gulpfile.js` to point to the local server url setup

    gulp.task('browserSync', function() {
    browserSync.init(
        [paths.css + '/*.css', paths.js + '*.js', paths.templates + '/*.html'], {
            proxy: '<local server url>',
        });
    });


And finally

    gulp watch

This setup also supports `sass` in case you prefer writing sass to css just create the `sass` directory 
<p>and everything should work as expected</p>
