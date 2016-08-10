# \<x-dashboard\>

[![GitHub release](https://img.shields.io/github/release/tony19-sandbox/x-dashboard.svg)](https://github.com/tony19-sandbox/x-dashboard/releases)
[![Build Status](https://travis-ci.org/tony19-sandbox/x-dashboard.svg?branch=master)](https://travis-ci.org/tony19-sandbox/x-dashboard)

> [Event Dashboard](http://www.site.uplabs.com/posts/dashboard-for-event-management-project) implementation, using [Polymer CLI](https://github.com/Polymer/polymer-cli) template 

<img src="https://github.com/tony19-sandbox/x-dashboard/blob/master/images/screenshot.png" height="220">

#### Quick Start

If not already, install [Node.js](https://nodejs.org/en/) (6.x.x or newer), and
then [Gulp](http://gulpjs.com/), [Bower](https://bower.io/), and
[Polymer CLI](https://github.com/Polymer/polymer-cli) with:

```sh
npm install -g gulp bower polymer-cli
```

To build and open a demo, run these commands from the project's root directory:

```sh
npm install
bower install
polymer serve -o
```

Note the `serve` command serves the app at `http://localhost:8080` and provides
basic URL routing for the app. Use the `-o` flag to automatically open the browser.

    polymer serve [-o]


#### Build

This command performs HTML, CSS, and JS minification on the application
dependencies, and generates a service-worker.js file with code to pre-cache the
dependencies based on the entrypoint and fragments specified in `polymer.json`.
The minified files are output to the `build/unbundled` folder, and are suitable
for serving from a HTTP/2+Push compatible server.

In addition the command also creates a fallback `build/bundled` folder,
generated using fragment bundling, suitable for serving from non
H2/push-compatible servers or to clients that do not support H2/Push.

    polymer build


#### Test the build

This command serves the minified version of the app in an unbundled state, as it would
be served by a HTTP2-push-compatible server:

    polymer serve build/unbundled

This command serves the minified version of the app generated using fragment bundling:

    polymer serve build/bundled


### Useful Polymer CLI commands

```sh
Usage
  polymer [COMMAND] [OPTIONS...]

Available Commands

  build   Build the application
  help    Shows this help message, or help for a specific command
  lint    Lints the project
  serve   Runs the polyserve development server
  test    Runs web-component-tester
```
