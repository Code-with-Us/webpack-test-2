# README

In this second test, we'll use webpack-dev-server, and as before, we will not use a config file.
    
We've initialized our project and installed webpack, webpack-cli, and webpack-dev-server. 

We have a minimal html.index file and a 'src' directory in which we've placed our index.js file and a second file called hello.js. index.js imports hello.js and calls it from within a console.log statement. hello.js returns a greeting, e.g. "Hello, Julian". 

Now enter the command 'npx webpack-dev-server.' This command will serve our page to port 8080.

Notice that we don't yet see the console.log message, "Hello, Julian!" In order to see our script in action, we'll need to return to index.html and insert a script tag to import main.js. Because webpack-dev-server serves the bundled JS from the root directory, the path to main.js is simply "main.js." 

Notice that starting the dev server did not build a "dist" directory or a "main.js" file within the dist directory. webpack-dev-server serves the bundled JS file from memory, not from a directory.

We can now make changes to our JS files and see those chages reflected in our pages immediately without re-building our bundle and without a manual page reload. Note that this is only true of changes to our JS files. Changes to files that are not bundled in main.js will still require a reload.