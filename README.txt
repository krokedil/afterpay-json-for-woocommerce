=== AfterPay Nordics for WooCommerce ===
Contributors: krokedil, arvato, NiklasHogefjord, slobodanmanic
Tags: ecommerce, e-commerce, woocommerce, afterpay, arvato
Requires at least: 4.2
Tested up to: 5.1
Requires PHP: 5.6
Stable tag: trunk
WC requires at least: 3.0.0
WC tested up to: 3.5.5
License: GPLv3
License URI: http://www.gnu.org/licenses/gpl-3.0.html

AfterPay Nordics for WooCommerce is a plugin that extends WooCommerce, allowing you to take payments via AfterPay's new RESTful Json API.

== Description ==

With this extension you get access to [AfterPay's](http://www.afterpay.se/en/) payment methods - Invoice and Part Payment in Sweden & Invoice in Norway.

= Get started =
More information on how to get started can be found in the [plugin documentation](http://docs.krokedil.com/documentation/afterpay-nordics-for-woocommerce/).

== Installation ==

1. Download and unzip the latest release zip file.
2. If you use the WordPress plugin uploader to install this plugin skip to step 4.
3. Upload the entire plugin directory to your /wp-content/plugins/ directory.
4. Activate the plugin through the 'Plugins' menu in WordPress Administration.
5. Go to --> WooCommerce --> Settings --> Checkout and configure your AfterPay settings.

== Frequently Asked Questions ==
= Which countries does this payment gateway support? =
Invoice payments work for Sweden and Norway. Part payment only works for Sweden at the moment. Norway will be added in short.

= Where can I find AfterPay for WooCommerce documentation? =
For help setting up and configuring AfterPay for WooCommerce please refer to our [documentation](http://docs.krokedil.com/documentation/afterpay-nordics-for-woocommerce/).

= Where can I get support? =
If you get stuck, you can send a support ticket to support@krokedil.se. You can ask your question in English, Swedish or Norwegian. Support tickets written in Norwegian will be answered in Swedish. 



== Changelog ==
= 0.7.0 		- 2019.03.05 =
* Feature       - Improved handling of refunds (allow order line refunds).
* Fix           - Updated/corrected Norwegian translation.

= 0.6.7 		- 2019.01.30 =
* Fix           - Fixed refunds on order with no tax rate.
* Fix           - Description on refund no longer required.
* Fix           - Improved error handling of refunds.

= 0.6.6 		- 2018.10.19 =
* Tweak			- Limit first and last name to max 50 characters when sending them to AfterPay.
* Tweak			- Changed the limit for yourReference to max 19 characters when sending it to AfterPay.
* Tweak			- Add support for multiple subscriptions.
* Tweak			- Keep address fields disabled in checkout for SE after get address request (even if checkout page is reloaded).

= 0.6.5 		- 2018.10.02 =
* Tweak			- Added filter afterpay_failed_capture_status.
* Tweak			- Send free shipping  info to AfterPay as well (previously only shipping with a price where sent).
* Fix			- Tax rate fix if multiple shipping methods exist in order.

= 0.6.4 		- 2018.09.27 =
* Fix			- Limit yourReference to 20 characters (sent to AfterPy for B2B purchases in order capture request).
* Fix			- PHP notice fix.

= 0.6.3 		- 2018.09.12 =
* Tweak			- Improved messaging when entered personal number is in wrong format.
* Tweak			- Display part payment example for all countries (previously only displayed for Norway).
* Tweak			- Updated default Norwegian account payyment method description.
* Tweak			- Translation updates.
* Tweak			- Change AfterPay terms page link for SE.
* Tweak			- Change order of when AfterPay terms link is displayed next to payment method.
* Fix			- CSS change - make sure get address response is displayed after a linebreak.
* Fix			- Make sure TotalNetAmount is sent with 2 decimals.
* Fix			- Add order note that order hasn't been cancelled in AfterPays system when trying to cancel order after it already being captured.

= 0.6.2 		- 2018.06.12 =
* Tweak			- Add error message as order note + revert status to Processing if AfterPay capture fails.
* Tweak			- Changed url to Swedish afterpay terms URL.
* Tweak			- Added link to AfterPay privacy policy next to get address field (for Sweden).
* Fix			- Fixed PHP warning that caused refunds to not work in some environments.


= 0.6.1 		- 2018.05.09 =
* Tweak			- Improved messaging to customer in checkout when purchase (Authorize request) is denied by AfterPay.
* Tweak			- Display get address form even if AfterPay isn't the selected payment gateway.

= 0.6.0 		- 2018.04.29 =
* Feature       - Add support for recurring payments (for invoice) via WooCommerce Subscriptions.
* Tweak         - Store AfterPay customer number in WooCommerce order.
* Tweak         - Added filters afterpay_authorize_order & afterpay_authorize_subscription_renewal_order.
* Tweak         - Only display detailed part payment info to Norwegian customers.
* Fix           - WC 2.6 support in Cancel reservation request.
* Fix           - Send correct params in authorize and capture request for B2B purchases.
* Fix           - Sync afterpay-pre-check-mobile-number field with billing phone field.

= 0.5.1 		- 2018.04.04 =
* Fix           - Send correct shipping vat to AfterPay even for v2.6.x.

= 0.5.0 		- 2018.03.23 =
* Tweak         - Compatible with WC 2.6.
* Fix           - Fix so products with 0 amount price & 0% vat can be included in order data sent to AfterPay.

= 0.4.0 		- 2018.03.12 =
* Feature		- Added Account payments.
* Feature		- Added Part payment Norway.
* Feature		- Add support for partial refunds (if order only contain one tax rate).
* Tweak			- Add setting for separate Description fields for Sweden & Norway.
* Tweak			- Plugin checked against AfterPay design guidelines.
* Tweak			- Remove feature for allowing separate shipping address for companies.
* Tweak			- Remove get address masking.
* Tweak			- Make address fields readonly for Sweden when get address feature has been used.
* Tweak			- Added loading spinner to get address button.
* Tweak			- Added setting for account profile number.
* Fix			- Send correct payment type (installment) for part payment.
* Tweak			- Don’t change address data when switching payment method.
* Tweak			- Update WC order with address information received from AfterPay.

= 0.3.2 		- 2017.11.24 =
* Fix			- Remove - from personal/organization number sent to AfterPay.

= 0.3.1 		- 2017.11.19 =
* Fix			- Don’t display payment method if it isn’t enabled in settings.
* Fix			- Don’t display part payment if only selling to companies.
* Tweak			- Hide part payment if customer type company is selected.

= 0.3 			- 2017.11.17 =
* WordPress.org release

= 0.2.1 		- 2017.11.09 =
* Fix			- Get address feature is not available for companies.
* Tweak			- Improved handling of returned address data.

= 0.2.0 		- 2017.11.08 =
* Tweak			- Changed textdomain name.

= 0.1 			- 2017.08.24 =
* Initial release