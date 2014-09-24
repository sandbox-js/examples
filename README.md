JavaScript RBroker Framework for DeployR
========================================

The JavaScript RBroker Framework provides a simple yet powerful API that 
supports the rapid integration of R Analytics inside any browser or Node.js 
based application. Simply define an _RTask_, submit your task to an instance of 
_RBroker_ and then retrieve your task results. It really is that simple.

Links
-----

  * [Tutorial](http://deployr.revolutionanalytics.com/documents/dev/rbroker/)
  * [API Documentation](http://deployr.revolutionanalytics.com/documents/dev/rbroker-jsdoc)
  * [Installation](#installationl)  
  * [Simple examples](#examples)
  * [Gulp, for building](#building)
  * [Tests](#tests)
  * [License](#license)

Installation
============

Install the JavaScript RBroker library using the instructions for your 
particular environment:

Browser
-------

```
<!-- Latest compiled raw JavaScript variation -->
<script src="./browser/deployr.js"></script>
```

Or

```
<!-- Latest compiled minified JavaScript variation -->
<script src="./browser/deployr.min.js"></script>
```

Node.js
-------

[Download and install](http://nodejs.org/download/) Node.js, which includes npm.
npm, which stands for _node packaged modules_, is a way to manage development 
dependencies through Node.js.

From the command line:

1. Navigate to the root ```/rbroker/``` directory.

2. Run ```npm install --production```. npm will look at the package.json file 
and automatically install the necessary local runtime dependencies listed there.

3. Include the JavaScript Client Library for DeployR ```deployr``` dependency 
by first installing it using the directions outlined [here](http://deployr.revolutionanalytics.com/documents/dev/client-jsdoc/#install). 

4. Once installed copy the entire ```/deployr``` directory into ```./rbroker/node_modules```.
This step is needed because the JavaScript Client Library for DeployR is 
**not yet** registered as a public npm package. This is comming soon.

5. Similar to the JavaScript Client Library for DeployR, the JavaScript RBroker 
library is **not yet** registered as a public npm package either. After running 
```npm install --production``` in step 2, you will need to manually copy the 
entire ```/rbroker/``` directory into the ```node_modules``` directory of the 
Node.js project that will be using it.

6. ```require``` the directory:

```
var rbroker = require('rbroker');
````

Examples
========

The JavaScript RBroker library ships with a set of small examples under the 
__./rbroker/examples__ directory that run in both the browser and Node.js 
environments. The intention of the examples are to demonstrate the syntax and 
core areas of the JavaScript API. They are not intended to be a tutorial on how 
to write web applications.

We encourage you to start here and customize these examples and adapt them to 
suit your needs as you explore the API.

- __./examples/tutorial:__ Introduces the three RBroker runtimes available. 
These runtimes are identified as:

 1. Discrete Task Runtime
 2. Pooled Task Runtime
 3. Background Task Runtime


Running
-------

__Browser:__

- Copy the _.html_ files under `./examples` to your webserver
- Copy the `./examples/config.json` file under `./examples` to your webserver
- Set the DeployR endpoint and basic authentication credentials in 
`./examples/config.json`

```
{
	"host": "http://dhost:port",
	"cors:" true,
	"credentials": {
	   "username": "testuser",
	   "password": "PASSWORD"
	}
}	
```

Alternatively, you can run the examples without moving them via the embedded 
web server:

`$ npm install --global gulp`

`$ cd ./rbroker`

`$ npm install`

`$gulp start`

Open your browser to _http://localhost:8080/examples/_ and select an example 
.html file to run.

__Node.js:__

Set the DeployR endpoint and basic authentication credentials in 
`./examples/config.json`

```
{
	"host": "http://dhost:port",
	"credentials": {
	   "username": "testuser",
	   "password": "PASSWORD"
	}
}

```

From the command line run one of the Node.js examples:

```$ node ./examples/PATH_TO_EXAMPLE_FILE.js```

Building
========

This section only pertains to _Browser_ environments. 

Our dev and release builds are handled by [gulp.js](http://gulpjs.com/).

Installation
------------

First you need to install `gulp` (`$ sudo npm install --global gulp`)

After cloning you can simply do an NPM install.

`$ npm install`

This will install the development tools needed to build locally.

Shortcuts
---------

 * `gulp` Runs a build.
 * `gulp start` Runs a build and starts a local webserver with LiveReload 
 (port __8080__) rebuilding on file changes.

Destination
-----------
The browser build destination is located in the __./browser__ directory.

Tests
=====

Coming soon...

License
=======

Copyright (C) 2010-2014 by Revolution Analytics Inc.

This program is licensed to you under the terms of Version 2.0 of the
Apache License. This program is distributed WITHOUT
ANY EXPRESS OR IMPLIED WARRANTY, INCLUDING THOSE OF NON-INFRINGEMENT,
MERCHANTABILITY OR FITNESS FOR A PARTICULAR PURPOSE. Please refer to the
Apache License 2.0 (http://www.apache.org/licenses/LICENSE-2.0) for more 
details.
