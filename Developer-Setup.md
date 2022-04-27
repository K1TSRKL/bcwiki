# Developer Setup

## Table of contents

* [Introduction](#introduction)
* [UI Setup](#ui-setup)
  * [Running a dev server through your IDE](#running-a-dev-server-through-your-ide)
  * [Web Server for Chrome](#web-server-for-chrome)
  * [Running a PHP Dev Server](#running-a-php-dev-server)
  * [Running a Python Dev Server](#running-a-python-dev-server)
* [Server Setup](#server-setup)
  * [Installing MongoDB](#installing-mongodb)
  * [Installing Node JS and npm](#installing-node-js-and-npm)
  * [Running the server](#running-the-server)

## Introduction

[Top of page](#developer-setup)

There are two main components to the application: the UI and the server. The UI is written using HTML and JavaScript. The server is written in JavaScript using NodeJS, and is backed by a MongoDB database.

For most development purposes (for example if you're just testing a new asset), it is sufficient to only set up the UI and have it point at the game's development server (which will happen automatically when you run the game locally). For more complex changes, or for more control over the dev environment, it may be useful to also have a local copy of the server running. This page walks through how to set up both the UI and the server.

This guide (currently) assumes you have already cloned the relevant repositories - git guidance may be added later. The main game repositories are here:

* UI: [https://github.com/Ben987/Bondage-College](https://github.com/Ben987/Bondage-College)
* Server: [https://github.com/Ben987/Bondage-Club-Server](https://github.com/Ben987/Bondage-Club-Server)

> ℹ️ If you notice any issues with this guide, or would like to suggest improvements, you can raise an issue here in Github, or get in touch with Ellie#7890 in the [Club Discord](https://discord.gg/dkWsEjf).

## UI Setup

[Top of page](#developer-setup)

To run the UI standalone, pointed at the live server, all that's needed is a simple HTTP server to serve up `BondageClub/index.html`. There are several options here, and this page will cover a handful. Below are two easy options, and further down are a couple of more advanced options (which might be useful for those already fairly familiar with PHP or Python).

> ⚠️ The game's dev server uses its own database for character accounts, so you won't be able to log in with your usual Bondage Club credentials if you're only running the UI. The first time you connect using one of the methods below, you'll want to create a new account on the dev server, which you'll then be able to use each time you run the game locally.

### Running a dev server through your IDE

Depending on your choice of code editor, many modern IDEs come with a built-in development server. Below we cover two options: Visual Studio Code and JetBrains IDEs (e.g. WebStorm). If you use a different IDE, check your IDE's documentation to see if this option is available to you, and to learn how to do it.

#### Visual Studio Code

The [Live Server extension](https://ritwickdey.github.io/vscode-live-server/) for VS Code allows you to serve up the club statically.

Install the extension and use it to launch the `BondageClub/index.html` file (the link above gives a pretty comprehensive guide on how to do this).

#### JetBrains Suite

JetBrains WebStorm comes with built-in functionality for serving static web content. Simply locate the `BondageClub/index.html` file in the project explorer, right click it, and select "Run 'index.html'". This should open up the club in your default browser.

### Web Server for Chrome

This is a Chrome app that allows you to serve up static files quickly and easily (but obviously, it requires that you have Google Chrome installed).

You can install the app from [the Chrome web store](https://chrome.google.com/webstore/detail/web-server-for-chrome/ofhbbkphhbklhfoeikjpcbhemlocgigb).

Once the app is installed, launch it and click the "Choose Folder" button - use this to select the `BondageClub` directory inside the Bondage-College repository. Ensure the "Automatically show index.html" checkbox is checked, then click the link to the provided web server URL.

### Running a PHP Dev Server

First, you'll need to install PHP ([https://www.php.net/](https://www.php.net/)). Depending on your operating system, how you do this will vary - the PHP website has fairly comprehensive installation guidance for most operating systems: [https://www.php.net/manual/en/install.php](https://www.php.net/manual/en/install.php). For Mac users, a version of PHP should come installed with the operating system. To verify that PHP has been installed correctly, open a terminal and enter:

```
php -v
```

If PHP is installed correctly, you should see something like this printed:

```
PHP 7.4.4 (cli) (built: Mar 17 2020 13:49:13) ( NTS Visual C++ 2017 x64 )
Copyright (c) The PHP Group
Zend Engine v3.4.0, Copyright (c) Zend Technologies
```

Once you have PHP installed, navigate to the `BondageClub` directory inside the repository, and run:

```
php -S localhost:8000
```

Once the server has started, you should be able to browse to [http://localhost:8000](http://localhost:8000) in your browser, and the game should be running.

### Running a Python Dev Server

Mozilla have a fairly succinct guide to [running a Python dev server](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/set_up_a_local_testing_server#Running_a_simple_local_HTTP_server).

First, you'll need to install Python (either Python 2.x or Python 3.x). Python can be downloaded from [https://www.python.org/downloads/](https://www.python.org/downloads/).

To verify that Python has been installed correctly, open a terminal and enter:

```
python -V
```

If Python is installed correctly, you should see something like this printed:

```
Python 2.7.17
```

Once you have Python installed, navigate to the `BondageClub` directory inside the repository. Then, depending on your python version, you'll need to run a different command to start the server.

#### Python 2.x

```
python -m SimpleHTTPServer
```

#### Python 3.x

```
python3 -m http.server
```

Once the server has started, you should be able to browse to [http://localhost:8000](http://localhost:8000) in your browser, and the game should be running.

## Server Setup

[Top of page](#developer-setup)

To run the server locally, you will need a MongoDB server listening on the default port (27017), and a working Node JS/npm installation. If you already have both of these, you can safely skip to the Running the server section below.

### Installing MongoDB

The server stores user accounts inside a MongoDB database, so you'll need a MongoDB instance to point the server at in order to run it locally. The easiest way to do that is to install and run MongoDB Community Edition on your local machine.

* [You can download MongoDB for your OS here.](https://www.mongodb.com/try/download/community)
* [MongoDB has comprehensive for installation on most operating systems here](https://docs.mongodb.com/manual/installation/#install-mongodb)

Once MongoDB has been installed, you should make sure that the `mongo` and `mongod` executables are available on your `PATH` environment variable. They are usually found in:

```
<mongo installation directory>/Server/<version number>/bin
```

If you installed MongoDB as an automatically-starting service, then the MongoDB server should already be running. To connect to it, run the following in a terminal:

```
mongo
```

If successful, you should see something like the following:

```
MongoDB shell version: 4.2.0
connecting to: test
```

You can exit the Mongo shell using:

```
exit
```

If you did not set up MongoDB to start automatically, you will need to start it manually by running the following in a separate terminal:

```
mongod
```

Assuming you managed to get everything up and running, the MongoDB server will now be available and listening on `localhost:27017`.

To learn a little more about Mongo and how to use it, take a look at the [Getting Started](https://docs.mongodb.com/manual/tutorial/getting-started/) guide. MongoDB also a GUI, [Compass](https://www.mongodb.com/try/download/compass), which allows you to browse and perform operations on your MongoDB databases and collections.

### Installing Node JS and npm

Installing Node JS and npm is fairly straightforward. You can download the appropriate installer or binary for your system [from this page](https://nodejs.org/en/download/). Alternatively, [this page](https://nodejs.org/en/download/package-manager/) has guidance on installing Node via a package manager.

You can verify that Node has been installed correctly by running the following from a terminal (assuming the Node binary is available on your `PATH` environment variable):

```
node -v
```

This should print out something like this:

```
v12.18.0
```

Similarly, you can verify that npm has been installed correctly by running the following from a terminal:

```
npm -v
```

This should print out something like this:

```
6.14.5
```


### Running the server

Assuming you have a local MongoDB installation running, and a working Node/npm installation, you should now be able to run the server locally.

First, navigate to the `Bondage-Club-Server` directory, and run the following:

```
npm i
```

This will install the various Node JS dependencies needed to run the server. This might take a little while the first time you run it. Once the dependencies have been installed, you can run the server with:

```
npm start
```

If everything is working correctly, you should see the following:

```
> BondageClubServer@1.0.0 start J:\Other\dev\projects\Bondage-Projects\Bondage-Club-Server
> node app.js

****************************************
Database: BondageClubDatabase connected
Next Member Number: 7
Bondage Club server is listening on 4288
****************************************
```

That's it! Your local server is now up and running. The last thing that needs to be done is to ensure that the UI is configured to point at your local server rather than the live game server.

### Pointing the UI to your local server

To get the UI to use your local server, you need to make one small edit to the `BondageClub/index.html` file in the `Bondage-College` repository. Comment out the following line from the `window.onload` callback function:

```js
ServerURL = "https://bondage-club-server.herokuapp.com/";
```

Once that has been done, that section of the file should look something like this:

```js
// When the code is loaded, we start the game engine
window.onload = function() {
	// ServerURL = CommonGetServer();
	//CheatImport();
	GameVersion = "R79";
	// etc.
};
```

Once that's done, you can start your UI as in the UI Setup section above.
