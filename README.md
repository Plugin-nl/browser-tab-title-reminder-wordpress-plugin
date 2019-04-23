# Browser tab title reminder WordPress plugin

Change the browser tab Title when the tab is not active as a reminder or to get the attention back from the user.

## Description

Change the browser tab Title when the tab is not active as a reminder or to get the attention back from the user.

The variables that can be set are:

*   Time before the title changes
*   The title when page is inactive

## Installation

You can download the plugin from Github.

1. Upload `browser-tab-title-reminder` directory to the `/wp-content/plugins/` directory.
2. Activate the plugin through the 'Plugins' menu in WordPress.

## Frequently Asked Questions

### Can I use emoji in the title?
Yes, using emoji is a great way to get the users attention.

## Is it supported in all browsers?
From what we tested it is.

## What if I'm not using WordPress?
Load in jQuery first and use the following code:
`
$(function() {
		var pageTitle = $("title").text();
		$(window).blur(function() {
				$("title").delay(3000).queue(function() {
					$("title").text("Don't forget us 🙂");
					$(this).clearQueue();
				});
		});
		$(window).focus(function() {
			$("title").text(pageTitle);
		});
	});
`
