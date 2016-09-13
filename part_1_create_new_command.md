# Writing your first Archy Command

Command is an HTTP server. When User interacts with Archy, it makes requests to related commands. In this tutorial we will show how to create a simple Hacker News client.

This tutorial uses *archy-sdk*, it hides protocol implementation from a developer. We recommend to use *archy-sdk*, it should save you from re-factoring, when we change protocol (and we planing changes).

You can deploy your command anywhere. In this tutorial, we use Heroku, but feel free to contact us if you have questions about other platforms.

The tutorial assumes that you have [a free Heroku account](https://signup.heroku.com/signup/dc), and that you have [Node.js and npm](https://nodejs.org/en/download/) installed locally, and [Heroku CLI tools installed](https://devcenter.heroku.com/articles/heroku-command-line#download-and-install).

## Step 1. Set Up

*In this step you will create heroku app, and learn about Command Endpoint.
*

**Create git repository and Heroku app**

In new empty directory, use ```git init``` and ```heroku create``` commands:

Example of output:
```bash
$ git init
Initialized empty Git repository in /path/to/your/command/.git/
$ heroku create
Creating app... done, ⬢ limitless-reef-53583
https://limitless-reef-53500.herokuapp.com/ | https://git.heroku.com/limitless-reef-53500.git
``` 

Remember the endpoint, created for your new heroku app, you will need it later. In the output above it's https://limitless-reef-53500.herokuapp.com.

You can always lookup heroku app endpoint using ```heroku info```.


**Create a package.json file with dependencies**

Create a package.json file with following content:

```json
{
  "version": "0.0.1"
  "scripts": {
    "start": "node index.js"
  }
}
```
**It's important** that your package.json file has declaration of a start script.

Add archy-sdk as a dependency:

```
npm install --save archy-sdk
```


## Step 2. Write first code

Now that we have setup everything, let's write some code.

In package.json above we specified index.js as a start script. Here is the full content of the script with comments.

**Create index.js file with the following content.**

```javascript
// import archy sdk, provides a basic http server and implements archy protocol
var archy = require('archy-sdk');

// command is described as an object
// only one required property - handler
// handler - is a function, that will be processing all requests from Archy
var showEvents = {
  handler: function () {
    // it must return array of objects
    return [{
      id: 1,
      title: "example event 1",
      text: "something happend today"
    }];
  }
};

// create new archy app instance and add new commands
var app = archy.App({
  commands: {
    'events': showEvents,
  }
});

// start HTTP server
// by default port 3000
app.start();
```



Now you can make your first commit and deploy new command:

```
$ git commit -m "Init command"
$ git push heroku master
```

```git push heroku master```  will push to remote heroku repositry and trigger auto-deployment. Heroku will auto-detect that you have node.js application and all required deployment actions.

After that you should be able to make POST requests to your new command:

```
curl -X POST -H "Content-Type: application/json" -d '{"payload":{ "perPage": null, "page": 1, "meta": {}, "args": {}}}' "https://your_heroku_app_endpoint/events"
```

Don't forget to replace *your_heroku_app_endpoint*, use ```heroku info```, if you need to lookup heroku app endpoint.

Command should return to you JSON object with some metadata.

## Step 3. Add command to Archy App

Now it's time to test your command with Archy App. Download it for [iOS](https://archy.ai/downloads/ios) or [Android](https://archy.ai/downloads/android).

Every command should be registered in Archy. This is a simple process, you don't need to create any accounts for that. Just go to [Create New Command page](https://archy.ai/developer/command/add) and register your new command.

