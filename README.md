# Sniffer

A JavaScript library for sniffing out information about pages, such as which JS libraries are used, what CMS the site runs on, what analytics packages it uses, and more. It is intended to be used in bookmarklets or injected JS widgets that need to gather information about the host page and it's component parts.

Where it can, Sniffer will return a string with more information (such as a version number) for each test; otherwise it will return boolean `true` or `false`.

Originally created for use in [Snoopy](https://github.com/michaelnordmeyer/snoopy).

## Detection Capabilities

Sniffer can detect the following items:

* General page information
  * Doctype
  * Charset
* JavaScript libraries
  * Dojo
  * ExtJS
  * Glow
  * Google Closure
  * jQuery
  * JQuery Mobile
  * jQuery UI
  * Modernizr
  * MooTools
  * Prototype
  * Scriptaculous
  * YUI2
  * YUI3
* Content Management Systems
  * Blogger
  * Drupal
  * Ghost
  * Hugo
  * Jekyll
  * Jimdo
  * Joomla
  * Medium
  * MovableType
  * Octopress
  * Squarespace
  * Tumblr
  * Typepad
  * Typo3
  * Weebly
  * Wix
  * WordPress
* Analytics
  * Ackee
  * Cabin
  * Chartbeat
  * Clicky
  * Cloudflare Insights
  * Fathom
  * Gauges
  * GoatCounter
  * Google Analytics (urchin.js, GA3 (=UA, ga.js, analytics.js, gtag.js), and GA4)
  * Google Tag Manager
  * Koko Analytics
  * Matomo
  * Microanalytics
  * New Relic
  * Open Web Analytics
  * Pirsch
  * Plausible
  * Reinvigorate
  * Slimstat Analytics
  * Statcounter
  * TinyAnalytics
  * Umami
  * W3Counter
  * Webtrends
  * Woopra
  * WordPress Stats
* Font embedding (technique)
  * Adobe Fonts
  * Cufon
  * Google Fonts
  * sIFR
* Commenting systems
  * Cactus Comments
  * Discourse
  * Disqus
  * Giscus
  * Isso
  * Utterances

## Usage

Including (or for a more common use-case scenario, *injecting*) the `sniffer.js` file into a page will give you access to a single global variable, `Sniffer`.

### Sniffer.check

Run an individual check by calling `Sniffer.check('test_item')` where 'test_item' is a string representing the thing to test for - 'jQuery' or 'Wordpress', for example. See below for a list of currently implemented tests.

The result will be `undefined` if Sniffer does not have a check corresponding to that name, boolean `false` if the test was negative, boolean `true` if the item was found but no other information could be extracted, or a text string of further information (normally the version number) if some can be extracted.

### Sniffer.run

`Sniffer.run()` will run all the tests Sniffer has and return an JSON object of results, grouped by test type (i.e. CMS, JavaScript Library, etc).

It's probably easiest to play around with the results of this in Firebug or Web Inspector to understand the exact structure of the JSON object returned.

### Sniffer.results

`Sniffer.results()` will return the same results object as `Sniffer.run()`, populated only with information about checks that have already been run.

## Contributors

* [Mark Perkins (owner)](https://github.com/allmarkedup)
* [Michael Nordmeyer](https://github.com/michaelnordmeyer)
