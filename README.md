JavaScript Client Library for DeployR
=====================================

The JavaScript client library is a light-weight fluent API used to communcate 
with DeployR from both the browser and Node.js environments. It is crafted for 
flexibility, readability, and a low learning curve.

Links
-----

  * [User Guide Documentation](http://deployr.revolutionanalytics.com/documents/dev/client-jsdoc)
  * [API Documentation](http://deployr.revolutionanalytics.com/documents/dev/client-jsdoc/api/)
  * [Installation](http://deployr.revolutionanalytics.com/documents/dev/client-jsdoc/#install)  
  * [Simple examples](#examples)
  * [Gulp, for building](#building)
  * [Tests](#tests)
  * [License](#license)

Examples
========

The DeployR JavaScript client library ships with a set of small examples under 
the __./deployr/examples__ directory that run in both the browser and Node.js 
environments. The intention of the examples are to demonstrate the syntax and 
core areas of the JavaScript API. They are not intended to be a tutorial on how 
to write web applications.

We encourage you to start here and customize these examples and adapt them to 
suit your needs as you explore the API.

- __./examples/api:__ Introduces the core areas of the JavaScript API.

- __./examples/tutorial:__ Introduces the top-level R analytics services exposed 
on the DeployR API.

Running
-------

__Browser:__

- Copy the _.html_ files under `./examples` to your webserver
- Inside each of the .html files set the DeployR endpoint and basic 
authentication credentials:

```
var config = {
	"deployrEndpoint": "http://dhost:port",
	"cors": true,
	"credentials": {
	   "username": "USERNAME",
	   "password": "PASSWORD"
	}
};		
```

Alternatively, you can run via embedded web server:

`$ npm install --global gulp`

`$ cd ./deployr`

`$ npm install`

`$gulp start`

Open your browser to _http://localhost:8080/examples/_ and select an example 
.html file

__Node.js:__

Set the DeployR endpoint and basic authentication credentials in 
```./examples/config.json```

```
{
	"deployrEndpoint": "http://dhost:port",
	"credentials": {
	   "username": "USERNAME",
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

First you need to install `gulp` (`$ npm install --global gulp`)

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
