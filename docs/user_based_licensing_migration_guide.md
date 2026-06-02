# Migration Guide

Source: https://developer.ninjatrader.com/docs/desktop/user_based_licensing_migration_guide

---

# Migration Guide


## [Overview](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_migration_guide#overview)


NinjaTrader is excited to introduce a **streamlined, user-based license management model** that eliminates the limitations of legacy machine ID tracking and brings modern flexibility to how you distribute and protect your products.


User-based licensing streamlines the licensing process by verifying user IDs instead of machine IDs. You and your customers will save time because neither of you have to manually verify their machine ID.


## [Key Benefits](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_migration_guide#key-benefits)


- **Simplified user management**: Enable licenses instantly by adding a user’s email address. No more machine ID updates or device revalidation.
- **Custom license parameters**: Manage subscription length and free trials directly from your license management portal.
- **Seamless integration**: Fully compatible with your existing product via minimal updates to your licensing implementation.
- **Ecosystem product listing integration**: Built to integrate directly with the new NinjaTrader Ecosystem, launching later this year.
- **Automation-ready**: Includes **API access** to support license creation, validation, and status monitoring, ideal for integrating with CRMs, e-commerce platforms, or internal tools.


## [Machine ID Licensing vs User Licensing](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_migration_guide#machine-id-licensing-vs-user-licensing)


User-based licensing streamlines the licensing process by verifying user IDs instead of machine IDs. You and your customers will save time because neither of you have to manually verify their machine ID.


### Machine ID Licensing


- Linked to 21-digit machine IDs
- Customers have to be on a specific device to access their purchases
- Adds additional steps during licensing
- Windows updates, hardware changes, and BIOS updates can change Machine IDs, requiring updates to licenses
- If users have identical machines (for example, a VPS), they need a custom user ID


### User Licensing


- Linked to user accounts
- Customers can access purchases from different devices
- Eliminates manual verification of machine IDs


## [How Do I Update?](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_migration_guide#how-do-i-update)


- Log in to the NinjaTrader Ecosystem vendor dashboard.
- Create your product in the dashboard.
- Link the product in the dashboard to the product in NinjaTrader desktop.
- Distribute the updated file to new customers.
- Create new licenses using either the dashboard or the API.
See the [User-Based Licensing Quick Start Guide](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_quick_start_guide) for detailed instructions.


## [Migration Details](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_migration_guide#migration-details)


- User-based licensing is optional.
- You do not need to re-create your add-on. The new licensing simply links your product to the NinjaTrader Ecosystem vendor dashboard.
- This is only for new licenses. Customers with existing licenses will be unaffected.
- The only requirement for customers is that they use NinjaTrader Desktop 8.1.5.0 or later.
- Code obfuscation is still offered through Agile.net. The only thing that changes in your code`is the`VendorLicense` line.


## [Have Questions?](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_migration_guide#have-questions)


- [User-Based Licensing Quick Start Guide](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_quick_start_guide)
- [User-Based Licensing FAQ](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_faq)
- [NinjaTrader Distribution Procedure](https://developer.ninjatrader.com/docs/desktop/distribution_procedure)
- [Vendor Support](https://vendor-support.ninjatrader.com/s/contactsupport?language=en_US)
