In the Terminal, yu must start a Heroku app
    - heroku create
        This creates a git remote that is added to your local repository
    This will create a random name for your app, but you can pass in a parameter to give it a custom name

Deploy code to heroku
    - git push heroku master

Ensure and instance is running
    - heroku ps:scale web=1

Open the site 
    - heroku open

Heroku treats logs as time ordered events from the output of your streams
    - heroku logs --tail
    - cntrl+C stops the log streaming

Procfile:  A txt file in the root directory of your application to explicitly declare what command should execute your app
    web: node index.js
      ^declares the process: web

    - heroku ps checks how many dynos are running

### Node.js

- Node.js is an event-based, non-blocking, asynchronous I/O runtime that uses Google’s V8 JavaScript engine and libuv library

#### Run JS in Terminal using node app.js

    jshint - lint a .js file
    
    npm init -y - create and autpopulate a package.json file in a folder

(alt)[https://dab1nmslvvntp.cloudfront.net/wp-content/uploads/2012/10/1516152673node_event_loop.png]


