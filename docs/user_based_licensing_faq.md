# FAQ

Source: https://developer.ninjatrader.com/docs/desktop/user_based_licensing_faq

---

# FAQ


## [Why is NinjaTrader updating the way licensing works?](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_faq#why-is-ninjatrader-updating-the-way-licensing-works)


User-based licensing streamlines the licensing process by verifying user IDs instead of machine IDs. You and your customers will save time because neither of you have to manually verify their machine ID.


## [Do I or my customers have to update to user-based licensing?](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_faq#do-i-or-my-customers-have-to-update-to-user-based-licensing)


While this update is intended to make your workflow easier by streamlining the licensing process, you and your customers do not have to update to user-based licensing.


## [Do I have to recreate my add-ons?](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_faq#do-i-have-to-recreate-my-add-ons)


No. You only need to create the add-on in the vendor dashboard and link it to the add-on in NinjaTrader desktop.


## [Do I have to upload my add-ons somewhere?](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_faq#do-i-have-to-upload-my-add-ons-somewhere)


No. You simply link your add-ons to the vendor dashboard.


## [Do my customers need to change anything?](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_faq#do-my-customers-need-to-change-anything)


Existing customers do not need to do anything.
Customers getting a new license simply need to make sure they are using NinjaTrader Desktop 8.1.5.0 or later.


## [How do I switch to user-based licensing?](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_faq#how-do-i-switch-to-user-based-licensing)


- Create your product in the NinjaTrader Ecosystem vendor dashboard.
- Link the product in the vendor dashboard to the product in NinjaTrader desktop.
- Distribute the updated file to new customers.
- Create new licenses using either the vendor dashboard or the API.
- For more information, see the [User-Based Licensing Quick Start Guide](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_quick_start_guide).


## [Is this available for desktop, mobile, and web?](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_faq#is-this-available-for-desktop,-mobile,-and-web)


Right now, user-based licensing is only available for NinjaTrader Desktop, but will be available soon for NinjaTrader Web and Mobile.


## [Will this work for NinjaTrader 7?](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_faq#will-this-work-for-ninjatrader-7)


Right now, user-based licensing is only available for NinjaTrader Desktop 8.1.5.0 or later.


## [What about my customers that already have a license?](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_faq#what-about-my-customers-that-already-have-a-license)


Existing licenses will not be affected. Once you update, you simply need to distribute the new file to customers who want a new license.


## [Is my code still obfuscated?](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_faq#is-my-code-still-obfuscated)


Obfuscation is still offered through Agile.net. The only thing that changes in your code is the `VendorLicense` line. For more information, see the [User-Based Licensing Quick Start Guide](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_quick_start_guide).


## [Since licensing no longer uses a machine ID, how can I verify that someone isn’t sharing their license?](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_faq#since-licensing-no-longer-uses-a-machine-id,-how-can-i-verify-that-someone-isn%E2%80%99t-sharing-their-license)


User IDs can only have two simultaneous market data active sessions, preventing users from sharing licenses with others.


## [Can I still create time-specific windows (for example, trial periods and license lengths) for my products?](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_faq#can-i-still-create-time-specific-windows-(for-example,-trial-periods-and-license-lengths)-for-my-products)


Yes. When you create a free trial or a license through the NinjaTrader Ecosystem Vendor Dashboard, you can select how long you want the license to last.


## [Is there a way to bulk load my customers into the licensing system?](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_faq#is-there-a-way-to-bulk-load-my-customers-into-the-licensing-system)


Yes. You can bulk load your customers into the licensing using the [NinjaTrader Ecosystem API](https://developer.ninjatrader.com/docs/ecosystem).
