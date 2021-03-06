analytics.js-integration-xng
============================

__In construction__

###How to build
This integration uses [duo.js](http://duojs.org/) to build itself but everything is taken care of by [Makefile](http://makepp.sourceforge.net/1.19/makepp_tutorial.html). What you need is `make` command and you are good to go.

###Commands
* Clean whole project (with installed packages): `[sudo] make distclean`
* Only delete generated files: `[sudo] make clean`
* Import node packages: `[sudo] make node_modules`
* Build: `[sudo] make build`

You don't need to import and clean packages every time, once you have them do `clean` and `build` and you should be good to go.

More details about what's going on when project is built can be found in `Makefile`, `component.json` and `package.json`.

###Troubleshooting 
 * If you see some EcmaScript 6 syntax-related errors buring build, make sure that your nodejs is version 0.11 or above.
 * Duo.js uses GitHub API to get it's dependencies, keep that in mind and configure you GitHub authorisation or you will hit the rate limit fast. It's 60 calls unauthorized and 5000 othewise. [Here's how to do it.](https://confluence.atlassian.com/stash/permanently-authenticating-with-git-repositories-282989712.html#notfound)
