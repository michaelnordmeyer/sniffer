Sniffer
=======

A JS library for sniffing out information about pages, such as which JS libraries are used, what CMS the site runs on, what analytics packages it uses, and more. It is intended to be used in bookmarklets or injected JS widgets that need to gather information about the host page and it's component parts.

Where it can, Sniffer will return a string with more information (such as a version number) for each test; otherwise it will return boolean `true` or `false`.

Please see the main site at [http://allmarkedup.com/sniffer/](http://allmarkedup.com/sniffer/) for more information and usage instructions.

Originally created for use in [Snoopy](https://github.com/allmarkedup/snoopy).

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
  * Chartbeat
  * Clicky
  * Cloudflare Insights
  * Fathom
  * Gauges
  * GoatCounter
  * Google Analytics (ga.js, analytics.js, and GA4)
  * Koko Analytics
  * Matomo
  * Microanalytics
  * Mint
  * New Relic
  * Open Web Analytics
  * Pirsch
  * Plausible
  * Reinvigorate
  * Slimstat Analytics
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


Contributors
------------

* Mark Perkins (owner)
* Michael Nordmeyer [https://github.com/michaelnordmeyer](https://github.com/michaelnordmeyer)
