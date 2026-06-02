# Quick-Start Guide

Source: https://developer.ninjatrader.com/docs/desktop/user_based_licensing_quick_start_guide

---

# Quick-Start Guide


## [Accessing the NinjaTrader Ecosystem Vendor Dashboard](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_quick_start_guide#accessing-the-ninjatrader-ecosystem-vendor-dashboard)


To create a product for licensing, you must first access the [NinjaTrader Ecosystem vendor dashboard](https://ecosystem.ninjatrader.com/).


When you first access the vendor dashboard you will either be granted access with no options to create a product or your login will be rejected. In either case, you will need to send your NinjaTrader username to [Vendor Support](https://vendor-support.ninjatrader.com/s/contactsupport?language=en_US) so we may enable your account for access to the vendor dashboard as a vendor.


If you intend to utilize the [NinjaTrader Ecosystem API](https://developer.ninjatrader.com/docs/ecosystem) for the automation of licensing, you will need a Tradovate account created at [account.tradovate.com](https://account.tradovate.com). Once created, you will need to access the vendor dashboard and then reach out to [Vendor Support](https://vendor-support.ninjatrader.com/s/contactsupport?language=en_US) with your Tradovate username and request access to the vendor dashboard and the Ecosystem API.


## [Adding Products in the Vendor Dashboard](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_quick_start_guide#adding-products-in-the-vendor-dashboard)


Adding a product in the vendor dashboard gives you access to license the product to users and provides the needed **Product ID** for the `VendorLicense()` call in your NinjaScript files (see [Linking the product in the UI to the add-on in NinjaTrader desktop](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_quick_start_guide#linking-the-product-in-the-ui-to-the-add-on-in-ninjatrader-desktop)).


To create a product as an Add-On in the vendor dashboard:


- In the vendor dashboard, select the **Manage Add-Ons** option under your Profile in the top right-hand corner.
- Select **Create Add-On** in the upper right-hand corner below your profile.
- Provide a **Title** and **Description**.

- These do not need to match exactly to the NinjaScript file in the NinjaTrader desktop.

- Example: You may have a suite of products that includes multiple indicators that will all be licensed under one Product and you would create one Add-On as the suite for those indicators.
- Enable **Free Trial** if you plan to provide a set number of days that a user may be authorized automatically for your product (see [Free Trials](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_quick_start_guide#free-trials)).
- Select **Create Add-On** below the **Free Trial** option once you have filled in the details above.
- You will be taken to the **Edit Add-On** page for your newly created product.
- Within the **Edit Add-On** page, the two sections to focus on for licensing are **Desktop Integration** and **Licenses.**

- Expand the **Desktop Integration** section to see the Product ID needed for the `VendorLicense()` call in your NinjaScript files (see [Linking the product in the UI to the add-on in NinjaTrader desktop](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_quick_start_guide#linking-the-product-in-the-ui-to-the-add-on-in-ninjatrader-desktop)).
- Expand the **Licenses** section to view all current licensed users.
- Select **Create License** under the **Licenses** section to add a new license for a user (see [Adding a License for a Customer](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_quick_start_guide#adding-a-license-for-a-customer)).

- **Email** is the user's NinjaTrader account email address.
- **License Type** is the desired duration for the user's license.
- **License expires on** is the date the user's license will expire.


## [Linking the product in the UI to the add-on in NinjaTrader desktop](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_quick_start_guide#linking-the-product-in-the-ui-to-the-add-on-in-ninjatrader-desktop)


Once the product is created in the vendor dashboard, you need the **Product ID** from the **Desktop Integration** section of the **Edit Add-On** page to link the product to the Add-On through its NinjaScript file in the NinjaTrader desktop application.


- In NinjaTrader desktop, go to the Control Center, click **New** > **NinjaScript Editor**.
- In the NinjaScript Explorer pane, open the NinjaScript file for the Add-On through the folders on the right.

- If it opens in a new window (for example, Strategy Builder), click **View Code**.
- Under the public class inheritance line of your NinjaScript file you will need to create a new function/method that carries the same name as the public class.

- Example:


```csharp
namespace NinjaTrader.NinjaScript.Strategies
{
	public class TestExportStrategy : Strategy
	{
		public TestExportStrategy()
		{
		}
```


- In the newly created function/method, add the `VendorLicense()` with the Product ID.

- Example:


```csharp
namespace NinjaTrader.NinjaScript.Strategies
{
	public class TestExportStrategy : Strategy
	{
		public TestExportStrategy()
		{
			VendorLicense(/*Your Product ID*/);
		}
```


- Save and compile the code.
- The file will need to be exported and distributed by you to the users. Please see [Exporting NinjaScript as Assembly](https://developer.ninjatrader.com/docs/desktop/export#exporting-ninjascript-as-assembly) and [Distribution](https://developer.ninjatrader.com/docs/desktop/distribution#distribution) for more details.


## [Adding a License for a Customer](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_quick_start_guide#adding-a-license-for-a-customer)


Now that the product is linked in the vendor dashboard and NinjaTrader desktop, you are ready to create a customer license. You can do this either through the vendor dashboard or by using the API.


### Adding a customer license through the vendor dashboard


- From the **Manage Add-Ons** screen, find the add-on and click **Edit**.
- Under **Licenses**, click **Add License**.
- Add the user’s email address, select the license type, and then click **Create License**.
- Review the details of the new license and then click **Confirm**.


### Adding a customer license through the API


For more information, see the [NinjaTrader Ecosystem API Documentation](https://developer.ninjatrader.com/docs/ecosystem).


## [Free Trials](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_quick_start_guide#free-trials)


When you create an add-on, you can set how long free trials last. Users are limited to one free trial per product. If you have a free trial configured, customers using your product for the first time will be granted a free trial.


Free trials start the day a customer first uses your product and end after the number of free trial days has passed.


If you need to create a free trial for a user who already had a trial, you can create a temporary license using the *Adding a License for a Customer* process. Under **License Type**, select *Free Trial*.


## [Enabling Authentication](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_quick_start_guide#enabling-authentication)


The vendor license check is added in your code as a method call in NinjaTrader 8.1.5.0 or later.


The following is the *VendorLicense* class constructor:


```csharp
VendorLicense(productID)
```


Any time an add-on is used, NinjaTrader checks the user’s license. If the user doesn’t have a license, the OnBarUpdate() and Plot() methods will not be called in the Strategy. However, the script will still process any code within its SetDefaults State. Thus, if you have added any code within an “if (State == State.SetDefaults)” condition in the OnStateChange() method, this will be processed regardless of a user’s license status.


## [Protection and DLL Security](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_quick_start_guide#protection-and-dll-security)


NinjaTrader uses Agile.net to offer increased security for protected DLLs. This requires a yearly license fee which can be paid directly to SecureTeam. For more information, see [SecureTeam pricing](http://www.secureteam.net/ninja-pricing) and the [Protection / DLL Security section of the help guide](https://ninjatrader.com/support/helpGuides/nt8/en-us/?protection_dll_security.htm).


## [Have Questions?](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_quick_start_guide#have-questions)


- [User-Based Licensing Migration Guide](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_migration_guide)
- [User-Based Licensing FAQ](https://developer.ninjatrader.com/docs/desktop/user_based_licensing_faq)
- [NinjaTrader Distribution Procedure](https://developer.ninjatrader.com/docs/desktop/distribution_procedure)
- [Vendor Support](https://vendor-support.ninjatrader.com/s/contactsupport?language=en_US)
