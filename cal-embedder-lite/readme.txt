=== UseStrict's Calendly Embedder ===
Contributors: useStrict
Donate link: https://paypal.me/usestrict
Tags: calendar, calendly, embed
Requires at least: 4.5
Tested up to: 7.1.3
Requires PHP: 7.4
Stable tag: 1.2.3
License: GPLv2 or later
License URI: https://www.gnu.org/licenses/gpl-2.0.html

Simple but powerful embedding for Calendly.

== Description ==

Embed Calendly on any WordPress page with a shortcode you build by pointing and clicking, instead of hand-writing Calendly's embed code.

**What the free plugin does**

* **Three embed types.** Inline calendar, pop-up text link, or the floating pop-up widget (badge), each with its own options.
* **Connect your Calendly account** with a Personal Access Token and pick your profile page or any event type from a dropdown. No copying URLs around. Without a token, paste the Calendly URL instead.
* **Caching-safe prefill.** Fill the booking form with the logged-in user's name and email, or with values from the query string. The prefill runs in the browser through AJAX after the page loads, so it keeps working behind full-page caches and CDNs, where server-side prefill can serve one visitor's details to the next.
* **Up to ten custom answers**, prefilled the same way.
* **Match your site.** Background, text and button colours, minimum width and height, extra CSS classes and inline styles.
* **Hide what you do not need.** The GDPR cookie banner, landing page details and event type details.
* **Shortcode builder** under Settings. Choose the options, copy the generated shortcode, paste it into any page, post, widget or page builder that runs shortcodes.

The builder generates a shortcode; it does not store it. To change an embed later, edit the shortcode where you pasted it, or build a new one.

**Going further: Calendly Embedder Pro**

<a href="https://usestrict.net/calendly-embedder-pro/?utm_source=readme&utm_medium=plugin&utm_campaign=promotion" target="_blank" title="UseStrict's Calendly Embedder Pro">Pro</a> picks up where the free plugin stops, and your existing embeds come with you: Pro finds the shortcodes already in your posts and pages and pulls them into a library, so upgrading is not a rebuild.

* **A shortcode library.** Save each embed once, reuse it anywhere, edit it in one place and every page updates. Place it with a shortcode, the Calendly Embed block, or the Elementor widget.
* **Booking analytics on your own site.** The funnel from profile view to completed booking, plus kept, no-show and cancelled outcomes by month.
* **Ask your AI assistant.** A read-only MCP server lets Claude, ChatGPT or Cursor query your booking data live. No extra API key; it uses the Calendly connection you already have. "What was my no-show rate in September?" is one question.
* **Campaign tagging.** Tag any embed with UTM parameters — source, medium, campaign, content and term — globally or per embed. These are standard UTM tags, so whichever analytics you run reads them, and Calendly records them against the booking as well.
* **Conversion tracking.** GA4 and Meta Pixel events on every completed booking, through the tags already on your site.
* **Lead capture.** Posts each new booking to any webhook URL: Zapier, Make, n8n, or a HubSpot workflow.
* **More ways to book.** Multi-event tabs, live availability next to the embed, email reminders, a bookings screen in wp-admin, WooCommerce integration, a redirect after booking, and a CSV export of your tracking data.

Pro runs alongside the free plugin, and your existing shortcodes keep working.

== Installation ==

= From the Admin =

1. Go to Admin > Plugins > Add New and search for UseStrict's Calendly Embedder.
1. Click Install.
1. Click Activate.
1. Find the settings under Settings > UseStrict's Calendly Embedder.

= Via FTP =

1. Download and unpack the plugin zip file.
1. Upload the entire folder to your plugins directory.
1. Activate the plugin through the 'Plugins' menu in WordPress.
1. Find the settings under Settings > UseStrict's Calendly Embedder.

== Frequently Asked Questions ==

= Does it work with page caching and CDNs? =

Yes. Prefilling happens in the browser, through an AJAX call after the page loads, so cached pages still show each visitor their own details.

= Do I need a Calendly API token? =

No. The Personal Access Token only powers the dropdown of your profile page and event types in the builder. Without one, paste your Calendly URL into the builder instead.

= Can I edit a shortcode after I have generated it? =

The free builder does not save what you build. Edit the shortcode's attributes where you pasted it, or build a new one and replace it. If you have many embeds to keep in sync, Pro keeps them in a library and imports the shortcodes already on your site.

= Can I use it in the block editor or Elementor? =

Yes. Paste the shortcode into a Shortcode block, Elementor's Shortcode widget, or anywhere else shortcodes run. Pro adds a dedicated Calendly Embed block and Elementor widget that pick a saved embed from a dropdown.

== Screenshots ==

1. The settings screen, before connecting to the Calendly API.
2. By connecting to the Calendly API, we display a drop-down with your Profile screen and individual Event Types.
3. Sample drop-down values.
4. Extra options for displaying the **Pop-up Text Widget**, a.k.a. **Link** widget. Default is inline, as seen in the previous screenshots.
5. Extra options for displaying the **Pop-up Widget**, a.k.a. the **Badge** widget.


== Changelog ==
= 1.2.3 =
* Settings screen: refresh the Calendly Embedder Pro section. It now leads with the shortcode importer, which brings the shortcodes already on your site into Pro's library, and drops a stale feature list.
* Correct a long-standing description: the five campaign settings emit standard UTM parameters, so any analytics tool reads them. They were previously described as Google Analytics variables.
* Add a phpcs ruleset for the plugin and fix a missing translator comment.

= 1.2.2 =
* Security: the Calendly Personal Access Token is no longer displayed in the settings page and is stored in a non-autoloaded option.
* Reliability: guard against malformed/failed Calendly API responses (no more PHP warnings or empty dropdowns on a transient outage).
* Add a direct-access guard to the settings template; fix the Pro-detection hook name and the API request Content-Type header.

= 1.2.1 =
* Fix version number.
* Update tested up to.

= 1.2 =
* Patch XSS vulnerability.
* Update tested up to.

= 1.1.7.2 =
* Fix typo, reported by @ovassolutions.
* Update tested up to.

= 1.1.7.1 =
* Fix missing classes and styles attributes for link-type calendar reported by @aabdullaev.
* Update tested up to.

= 1.1.6.2 =
* Update stable tag.

= 1.1.6.1 =
* Fix stable tag in readme.txt.

= 1.1.6 =
* Decode URI Component for custom answers.
* Remove spurious code block left over from copy/paste.

= 1.1.5.1 =
* Adjusted admin documentation to point out which query-string variables are supported.

= 1.1.5 =
* Break away query-string from prefill options. They now work independently, but prefill still overrides query-string.
* Support prefilling of the email via query-string.

= 1.1.4 =
* Fix problems with query strings and custom answers.

= 1.1.3 =
* Bumping the version to get readme.txt tested up to 6.1.

= 1.1.2 =
* Bumping the version to get the readme.txt stable tag fix.

= 1.1.1 =
* Tweak notices when using bad PATs.

= 1.1 =
* Added deprecation notice for API Key
* Added support for Calendly API v2 via Personal Access Token.

= 1.0.2 =
* Add missed hide* options to calendly URL.

= 1.0.1 =
* Fix the plugin name in the Settings screen.
* Add sections headers in the Shortcode Builder.
* Fix a bug in the JS when prefilling.

= 1.0 =
* Initial release.

== Upgrade Notice ==

= 1.0 =
No upgrade required at this time.
