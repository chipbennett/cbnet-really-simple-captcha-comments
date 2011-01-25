=== cbnet Really Simple CAPTCHA Comments ===
Contributors: chipbennett
Donate link: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=QP3N9HUSYJPK6
Tags: cbnet, plugin, comments, CAPTCHA, Really Simple CAPTCHA
Requires at least: 3.0
Tested up to: 3.0.3
Stable tag: 1.0.2

Comment form CAPTCHA using  Really Simple CAPTCHA plugin. Proof-of-concept for other plugin developers.

== Description ==

This plugin adds a CAPTCHA field to your comment form, using the API provided by the <a href="http://wordpress.org/extend/plugins/really-simple-captcha/">Really Simple CAPTCHA</a> plugin to provide the CAPTCHA image and validation.

This plugin is fully functional, but is mostly intended to be a "proof of concept" for other plugin developers who may want to use the Really Simple CAPTCHA plugin's API to provide CAPTCHA functionality for their own plugins.

**Note:** Version 1.0 of the plugin has no admin options page. In a future version, I will provide one, but for now, API options can be configured from within the PHP file. 

== Installation ==

Manual installation:

1. Upload the `cbnet-really-simple-captcha-comments` folder to the `/wp-content/plugins/` directory

Installation using "Add New Plugin"

1. From your Admin UI (Dashboard), use the menu to select Plugins -> Add New
2. Search for 'cbnet Really Simple CAPTCHA Comments'
3. Click the 'Install' button to open the plugin's repository listing
4. Click the 'Install' button

Activiation and Use

**NOTE** You *must* Install and activate the <a href="http://wordpress.org/extend/plugins/really-simple-captcha/">Really Simple CAPTCHA</a> plugin in order for this plugin to work.

1. Activate the plugin through the 'Plugins' menu in WordPress
2. The plugin requires no configuration.


== Frequently Asked Questions ==

= I activated the plugin, but don't see a CAPTCHA field in my comment form. What's going on? =

Make sure you have the <a href="http://wordpress.org/extend/plugins/really-simple-captcha/">Really Simple CAPTCHA</a> plugin installed and activated.

= What API settings can be configured? =

`// Characters to use in CAPTCHA image.
$comment_captcha->chars = 'ABCDEFGHJKLMNPQRSTUVWXYZ23456789';

// Number of characters in CAPTCHA image.
$comment_captcha->char_length = '4';

// Width/Height dimensions of CAPTCHA image.
$comment_captcha->img_size = array( '72', '24' );

// Font color of CAPTCHA characters, in RGB (0 - 255).
$comment_captcha->fg = array( '0', '0', '0' );

// Background color of CAPTCHA image, in RGB (0 - 255).
$comment_captcha->bg = array( '255', '255', '255' );

// Font Size of CAPTCHA characters.
$comment_captcha->font_size = '16';

// Width between CAPTCHA characters.
$comment_captcha->font_char_width = '15';

// CAPTCHA image type. Can be 'png', 'jpeg', or 'gif'
$comment_captcha->img_type = 'png';`

= What other settings can be configured? =

`// Comment form CAPTCHA field label text
$comment_captcha_form_label = 'Anti-Spam:';`

= The CAPTCHA field doesn't look right in my comments form. How can I style it? =

The HTML output is wrapped in a paragraph tag, with class="comment-form-captcha".

== Screenshots ==

1. The default CAPTCHA field in action

== Changelog ==

= 1.0.2 [2010.12.13] =
* Bugfix.
* Fixes minor bug that caused $comment_data not to be returned for logged-in users.
= 1.0.1 [2010.08.23] =
* Minor Bugfix.
* Fixes minor bug that caused non-existent CAPTCHA to be checked for logged-in users.
= 1.0 =
* Initial Release

== Upgrade Notice ==

= 1.0.2 =
Fixes bug that caused $comment_data not to be returned for logged-in users.
= 1.0.1 =
Fixes minor bug that caused non-existent CAPTCHA to be checked for logged-in users.
= 1.0 =
Initial Release.