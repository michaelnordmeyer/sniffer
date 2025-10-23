# Sniffer

A JavaScript library for sniffing out information about pages, such as what CMS the site runs on, which JavaScript libraries are used, what font services, commenting system, or analytics packages it uses, and more. It is intended to be used in bookmarklets or injected JavaScript widgets that need to gather information about the host page and its component parts.

Where it can, Sniffer will return a string with more information (such as a version number) for each test; otherwise it will return boolean `true` or `false`.

Created for use in [Snoopy](https://github.com/michaelnordmeyer/snoopy), a bookmarklet to display detected features of the current web page.

## Detection Capabilities

Sniffer can detect the following items:

* General page information
  * Doctype
  * Charset
* Content Management Systems
  * Astro
  * Blogger
  * ClassicPress
  * Docusaurus
  * Drupal
  * Eleventy
  * Gatsby
  * Ghost
  * Gridsome
  * Hexo
  * Hugo
  * Jekyll
  * Jimdo
  * Joomla
  * Lume
  * Medium
  * Metalsmith
  * MovableType
  * Nikola
  * Obsidian Publish
  * Octopress
  * Pandoc
  * Publii
  * Scully
  * Squarespace
  * Sushy
  * Tumblr
  * Typepad
  * Typo3
  * VitePress
  * VuePress
  * Weebly
  * Wix
  * WordPress
  * Write.as
  * WriteFreely
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
* Font embedding (technique)
  * Adobe Fonts
  * Cufon
  * Google Fonts
  * sIFR
* Commenting systems
  * Cactus Comments
  * Commento
  * Cusdis
  * Discourse
  * Disqus
  * Giscus
  * Isso
  * OpenWeb
  * Remark42
  * Utterances
* Analytics
  * Ackee
  * Bearblog
  * Burst Statistics
  * Cabin
  * Chartbeat
  * Clicky
  * Cloudflare Insights
  * Fathom
  * Gauges
  * GoatCounter
  * Google Analytics (urchin.js, GA3 (=UA, ga.js, analytics.js, gtag.js), and GA4)
  * Google Tag Manager
  * Hotjar
  * Koko Analytics
  * Matomo
  * Microanalytics
  * New Relic
  * Open Web Analytics
  * Pirsch
  * Plausible
  * Posthog
  * Rybbit
  * Seline
  * Simple Analytics
  * Slimstat Analytics
  * Statcounter
  * Statify
  * Statsig
  * TinyAnalytics.io
  * Tinybird
  * Tinylytics
  * Trackboxx
  * Umami
  * Usermaven
  * W3Counter
  * Webtrends
  * Woopra
  * WordPress Stats
  * WP Statistics

## Dependencies

None.

## Usage

Including (or for a more common use-case scenario, *injecting*) the `sniffer.js` file into a page will give you access to a single global variable, `Sniffer`.

### Sniffer.check

Run an individual check by calling `Sniffer.check('test_item')` where 'test_item' is a string representing the thing to test for - 'jQuery' or 'Wordpress', for example. See below for a list of currently implemented tests.

The result will be `undefined` if Sniffer does not have a check corresponding to that name, boolean `false` if the test was negative, boolean `true` if the item was found but no other information could be extracted, or a text string of further information (normally the version number) if some can be extracted.

### Sniffer.run

`Sniffer.run()` will run all the tests Sniffer has and return an JSON object of results, grouped by test type (i.e. CMS, JavaScript Library, etc).

It's probably easiest to play around with the results of this in Firebug or Web Inspector to understand the exact structure of the JSON object returned.

## Tests

All Sniffer tests can be unit-tested by loading `tests.html` in a browser. Note that Obsidian Publish cannot be tested and will always fail, because it uses the `<base>` tag, which breaks all tests on the test page.

### Sniffer.results

`Sniffer.results()` will return the same results object as `Sniffer.run()`, populated only with information about checks that have already been run.

## Contributors

* [Mark Perkins (original author)](https://github.com/allmarkedup)
* [Michael Nordmeyer (current maintainer)](https://github.com/michaelnordmeyer)
