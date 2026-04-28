# Protection DLL Security

Source: https://developer.ninjatrader.com/docs/desktop/protection_dll_security

---

# Protection DLL Security


## [Protection/DLL Security](https://developer.ninjatrader.com/docs/desktop/protection_dll_security#protection/dll-security)


Although **.NET DLL** files are compiled which prevents users from being able to see your proprietary source code, they are still subject to decompilation and reverse engineering attempts. If you want a higher level of security, you can select the "**Protect compiled assemblies**" option which adds an additional layer of protection. This additional protection layer is provided by [SecureTeam's Agile.NET](http://www.secureteam.net/ninja-pricing) product which has been licensed by **NinjaTrader** and available at a reduced price to protect **NinjaTrader** assemblies. This product claims to completely stop **MSIL** disassembly and decompilation. We use it ourselves and are extremely happy with it.


Should you wish to use **Agile.NET** for protecting your **NinjaScript** assemblies you will first need to go [here](http://www.secureteam.net/ninja-pricing) to download and purchase the product. Once installed, please run the **Agile.NET** standalone product once to input in the license information you should have received when you downloaded it. After that, when you use **NinjaTrader's Export NinjaScript** utility and select the "**Protect compiled assemblies**" option for export, it will automatically protect your **NinjaScript** assembly with **Agile.NET**.


Please note that this version of **Agile.NET** will only work for protecting **NinjaScript** assemblies within **NinjaTrader**. If you would like to protect other files outside of **NinjaTrader** please consider purchasing the full version of **Agile.NET** from **SecureTeam** directly [here](http://www.secureteam.net/ninja-pricing) 'Agile.NET 6.0 Code Protection'. **NinjaScript** assemblies protected with the full version of **Agile.NET** will also work in **NinjaTrader**.
