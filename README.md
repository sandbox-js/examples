JavaScript Client Library for DeployR
=====================================

The JavaScript client library is a light-weight fluent API used to communcate 
with DeployR from both the Browser and Node.js environments. It is crafted for 
flexibility, readability, and a low learning curve.

Links
-----

  * [User Guide Documentation](http://deployr.revolutionanalytics.com/documents/dev/client-jsdoc)
  * [API Documentation](http://deployr.revolutionanalytics.com/documents/dev/client-jsdoc/api/)
  * [Installation](http://deployr.revolutionanalytics.com/documents/dev/client-jsdoc/#install)  
  * [Simple examples](#examples)
  * [Gulp, for building](#building)
  * [License](#license)

Examples
========

The DeployR JavaScript client library ships with a set of small examples under 
the __/deployr/examples__ directory that run in both the Browser and Node.js 
environments. The intention of the examples are to demonstrate the syntax and 
core areas of the JavaScript API. They are not intended to be a tutorial on how 
to write web applications.

We encourage you to start here and customize these examples and adapt them to 
suit your needs as you explore the API.

Building
========

This section only pertains to _Browser_ environments. 

Our dev and release builds are handled by [gulp.js](http://gulpjs.com/).


Installation
------------

First you need to install `gulp` (`$ npm install --global gulp`)

After cloning you can simply do an NPM install.

`$ npm install`

This will install the development tools needed locally.

Shortcuts
---------

 * `gulp` Runs a build.
 * `gulp start` Runs a build and starts a local webserver with LiveReload on 
 port 8080 rebuilding on file changes.

Destination
-----------
The build destination rests in the _browser_ directory.

License
=======

Copyright (C) 2010-2014 by Revolution Analytics Inc.

This program is licensed to you under the terms of Version 2.0 of the
Apache License. This program is distributed WITHOUT
ANY EXPRESS OR IMPLIED WARRANTY, INCLUDING THOSE OF NON-INFRINGEMENT,
MERCHANTABILITY OR FITNESS FOR A PARTICULAR PURPOSE. Please refer to the
Apache License 2.0 (http://www.apache.org/licenses/LICENSE-2.0) for more 
details.
