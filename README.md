# mlproj

Project and environment manager for MarkLogic.

All details on: http://mlproj.org/.

![Animated intro](dev/mlproj-intro.gif)

## Install

Use the following:

```
npm install mlproj -g
```

This needs Node to be installed on your system.  Package managers for all
systems include it.  Look at [Node](http://nodejs.org/) website for details and
install options.

## Features

`mlproj` let you manage, deploy and configure MarkLogic projects.  In order to
achieve this, it also let you describe your environments and automatically set
them up.

Use `mlproj help` for an overview.  Go to http://mlproj.org/ for all details.

## TODO

- document the environment file format on the website
- allow command `new` to create projects with different scaffoldings
  - using "embedded" scaffoldings (empty, plain, complete, annotated, web, rest...)
  - using "remotes" ones (on Git repos?)
- new command `load` to load data on databases
- new command `add` to add components, indexes, etc. by answering few questions
- new command `mlcp` to invoke MLCP with info from the environment files
- new command `test` to run tests from command line
- new command to install a XAR/XAW file
- new command to install a XAR/XAW from CXAN
- new command to publish to CXAN
- edit environment files from the Console
  - move website in `mlproj-web` repo
  - move core libs in `mlproj-core` package
  - use `mlproj-core` in the Console
- word lexicons
- allow changing a server port, as it restarts the instance
- add support for triggers in space files

Support the following scenario (e.g. for the EXPath ML Console):

```
# check values are correct (supported)
mlproj -e dev -h myvm -u admin -z -p port:8010 show

# setup the environment (supported)
mlproj -e dev -h myvm -u admin -z -p port:8010 setup

# deploy modules (supported)
mlproj -e dev -h myvm -u admin -z -p port:8010 deploy

# initialize the app (to support)
mlproj -e dev -h myvm -u admin -z -p port:8010 init
```

which could/should be made easier:

```
# install everything (setup + deploy + init) (to support)
mlproj -e dev -h myvm -u admin -z -p port:8010 install
```
