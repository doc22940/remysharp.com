---
title: Complete Posts in WordPress Feeds
date: '2008-03-04 17:35:10'
published: true
tags:
  - code
  - hack
  - wordpress
modified: '2014-09-03 16:15:12'
---
# Complete Posts in WordPress Feeds

If you use WordPress and make use of the <code>&lt;!-- more --&gt;</code> tag, some of you may want to still show the complete post in the RSS feed.

You have to change some code, but it's easy to do.


<!--more-->

In all the <code>wp-includes/feed-*.php</code> files, change:

<pre><code>$more = 1;</code></pre>

To:

<pre><code>global $more;
$more = 1;</code></pre>

This will change the global more flag and include the complete post - as my blog does.  Happy hacking.
