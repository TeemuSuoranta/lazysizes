# lazysizes

- Contributors: 16patsle
- Tags: Lazy Load, lazysizes, iframe, image, media, video, YouTube, Vimeo, audio
- Requires at least: 3.1
- Requires PHP: 5.6
- Tested up to: 4.8.2
- Stable tag: 0.1.0
- License: GPLv3 or later
- License URI: <http://www.gnu.org/licenses/gpl-3.0.html>

High performance and SEO friendly lazy loader for images, iframes and more

## Description

**lazysizes** is a WordPress plugin for the fast (jank-free), SEO-friendly and self-initializing lazyloader [with the same name](https://github.com/aFarkas/lazysizes). Support includes images (including responsive images `picture`/`srcset`), iframes, scripts/widgets and much more. It also prioritizes resources by differentiating between crucial in view and near view elements to make perceived performance even faster.

This plugin works by loading the lazysizes script and replacing the `src` and `srcset` attributes with `data-src` and `data-srcset` on the front end of a WordPress site. When a post or page is loaded, the lazysizes javascript will load the images and iframes dynamically when needed.

Thanks to aFarkas and contributors for making the [lazysizes project](https://github.com/aFarkas/lazysizes) possible. Also thansk to dbhynds for making the Lazy Load XT plugin this plugin is based on.

## Installation

1. Install and activate the plugin through the 'Plugins' menu in WordPress

or

1. Download and unzip lazysizes.
2. Upload the `lazysizes` folder to the `/wp-content/plugins/` directory
3. Activate the plugin through the 'Plugins' menu in WordPress

## Frequently Asked Questions

### Why aren't my images lazy loading?

Lazysizes filters images added to the page using `the_content`, `post_thumbnail_html`, `widget_text` and `get_avatar`. If your images are added using another function (`wp_get_attachment_image` for example), lazysizes does not filter them. However, as of v0.4, you can filter the HTML yourself by passing it to `get_lazysizes_html`.

For example, if a theme has: `echo wp_get_attachment_image($id);` Changing it to the following would lazy load the image: `echo get_lazysizes_html( wp_get_attachment_image($id) );`

### But this plugin looks like Lazy Load XT!!

Yes, it does. The PHP code for this plugin is heavily based on that of Lazy Load XT. The main difference is that this plugin is a bit simplified, and is using a completely different lazy loading library, with no jQuery dependency.

Thanks to dbhynds for making Lazy Load XT. Without that project, this one would not be possible.

## Changelog

### 0.1.0

- Initial version of the plugin
