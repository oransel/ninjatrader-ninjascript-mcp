# Set Up

Source: https://developer.ninjatrader.com/docs/desktop/set_up10

---

# Set Up


The first step in creating a custom strategy is to use the custom **Strategy Builder**. The builder provides two options:


- Allow you to create a functional strategy without any programming
- Generate the required **NinjaScript** code that will serve as the foundation for your custom strategy for further coding


- Within the **NinjaTrader Control Center** window select the **New Strategy Builder...** menu
- Press the "Next" button


![SimpleMACrossoverSetUp1](https://cdn.sanity.io/images/1hlwceal/production/dce1c1b17cc7352e039c73eaa19a5c43d7e65929-825x550.png)


- Enter the information as shown above
- Press the "Next" button


## [Setting Default Properties](https://developer.ninjatrader.com/docs/desktop/set_up10#setting-default-properties)


The next page will allow you to set defaults for basic properties related to your strategy, including its **Calculate** and **EntryHandling** settings. Click the **More Properties** button to expose additional properties. For this tutorial, we will not change any basic properties' defaults, and instead will leave them all set to the values shown below:


![SimpleMACrossoverSetUp2](https://cdn.sanity.io/images/1hlwceal/production/20868680bc0fc7897fdd3019d7e099ea94456167-825x550.png)


## [Adding Additional Data](https://developer.ninjatrader.com/docs/desktop/set_up10#adding-additional-data)


The next page will allow you to configure one or more additional **Bars** objects for use by the strategy. For our purposes, we will leave this page blank and move forward by clicking the "Next" button.


![SimpleMACrossoverSetUp3](https://cdn.sanity.io/images/1hlwceal/production/e2ea156b62d5d9eeb7fba476d6c9315546a29aed-825x550.png)


## [Defining Input Parameters](https://developer.ninjatrader.com/docs/desktop/set_up10#defining-input-parameters)


Below you will define your strategy's input parameters. These are any input parameters that can be changed by the user when running or backtesting a strategy. If your strategy does not require any parameters leave the "Name" fields blank.


![SimpleMACrossoverSetUp4](https://cdn.sanity.io/images/1hlwceal/production/d14fbb30c09eac83b955a90f2ccf4f0e258cda4a-825x550.png)


- Click the add button to add a property
- Add input parameters into the newly created **Input Parameters** window and click Ok once the input parameter is set up


![SimpleMACrossoverSetUp5](https://cdn.sanity.io/images/1hlwceal/production/c3a9a38bf7d2275497c3cc4e2407e8281b4f42f3-825x550.png)


- Add the inputs as per the image above
- Press the "Next" button


## [Defining Conditions and Actions](https://developer.ninjatrader.com/docs/desktop/set_up10#defining-conditions-and-actions)


Below you can define conditions that trigger user-defined actions such as placing orders, drawing on a chart, or creating an alert.


Notice how there are two buttons on the screen below:


- **View Code...** - Pressing this button loads the strategy code in the **NinjaScript Editor** for viewing purposes only. This is a great approach if you are new to programming or you want to see how the strategy wizard dynamically generates the correct script code on the fly.
- **Unlock Code** - Pressing this button loads the strategy code in the **NinjaScript** editor for further manual editing. Once this button is pressed, you can NOT go back to the Wizard for strategy construction and editing.


![SimpleMACrossoverSetUp6](https://cdn.sanity.io/images/1hlwceal/production/4ff4dc0cdd7a6e799b628e165c31443e7e3adc63-825x550.png)


If you want to proceed with this tutorial through **self programming** [continue here](https://developer.ninjatrader.com/docs/desktop/creating_the_strategy_via_self_programming) after pressing the "Unlock Code" button.


If you want to proceed with this tutorial through **using the Strategy Builder** please [click here](https://developer.ninjatrader.com/docs/desktop/creating_the_strategy_via_the_wizard).
