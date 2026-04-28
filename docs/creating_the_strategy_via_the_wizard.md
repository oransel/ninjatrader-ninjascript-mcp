# Creating the Strategy via the Wizard

Source: https://developer.ninjatrader.com/docs/desktop/creating_the_strategy_via_the_wizard

---

# Creating the Strategy via the Wizard


## [Creating the Strategy via the Wizard](https://developer.ninjatrader.com/docs/desktop/creating_the_strategy_via_the_wizard#creating-the-strategy-via-the-wizard)


- Press the **Add** button to display the **Condition Builder** window as per the image below.


![SimpleMACrossoverBuilderStep1](https://cdn.sanity.io/images/1hlwceal/production/5e99a44c6fa795ed48e9a86e4f5bfccd7a678398-825x550.png)
- Expand the **Indicator** section to be able to select an indicator plot for your condition.


![SimpleMACrossoverBuilderStep2](https://cdn.sanity.io/images/1hlwceal/production/a74c23d53ebbbb09a512d4001456961e465ba97f-700x500.png)
- Scroll down and select the **SMA** indicator.
- Click the set menu item when your mouse is over the **Period** input field to select our **User Defined Input** parameter.


![SimpleMACrossoverBuilderStep3-4](https://cdn.sanity.io/images/1hlwceal/production/41d3336e4106dcbb8cca848b468d891c9d49ba8e-701x501.png)
- Select **User Input > Fast** to select the **Fast Period** user input we created, then click **OK**.


![SimpleMACrossoverBuilderStep5](https://cdn.sanity.io/images/1hlwceal/production/421081cb698986ac30d17c61a35cd4080c74cd74-303x500.png)
- Enable this indicator to be plotted on a chart.
- Select **CrossAbove** and set the look back period to a value of **1**.
- Select **SMA** indicator in the right window.
- Set the **Slow** period (just like you did for **Fast** in step 4).
- Enable this indicator to be plotted on a chart, then click **OK** to close the **Condition Builder**.


![SimpleMACrossoverBuilderStep6-10](https://cdn.sanity.io/images/1hlwceal/production/93e108ef2cb19234cd315902c715c857893a2060-700x500.png)


If you look at the image above, you just created an initial condition. The condition is "if the fast simple moving average crosses above the slow simple moving average".
- Click the **add** button under actions to add an action for this condition.


![SimpleMACrossoverBuilderStep11](https://cdn.sanity.io/images/1hlwceal/production/550ced5b6288c42b171e34cd268071b763e87986-825x550.png)
- Select **Order Management > Enter long position** to have this condition fire a **Buy Market Order**.
- Select the **OK** button to add the action to the condition.


![SimpleMACrossoverBuilderStep12-13](https://cdn.sanity.io/images/1hlwceal/production/dd9471d397d290898ae452f9e86ee66da334c33e-303x500.png)
- Right click on the **Set 1** tab and select **Duplicate in New Tab** to make a copy of this condition and action set.


![SimpleMACrossoverBuilderStep14](https://cdn.sanity.io/images/1hlwceal/production/73451711c9b207f06c0533c95d01f2b53071d05d-825x551.png)
- We will automatically be moved to the **Set 2** tab. From here, select the condition and click **edit**.


![SimpleMACrossoverBuilderStep15](https://cdn.sanity.io/images/1hlwceal/production/7a63d98fa990b7862724d9aabbc72d720e84cc40-825x550.png)
- Change this Condition to use **Cross Below** so we can create a condition that triggers when the moving averages switch sides, then click **OK**.


![SimpleMACrossoverBuilderStep16](https://cdn.sanity.io/images/1hlwceal/production/47fd5e6e2cc281728c7cf445b08c5a6928ad5691-700x500.png)
- Click the action in the **Condition Builder**, and then select **edit** to edit the action. We will want to change this action so we sell instead of buy for the reversed condition.


![SimpleMACrossoverBuilderStep17](https://cdn.sanity.io/images/1hlwceal/production/a70acd3ff57fd3bde4d00fc6e9ee77d1b786885e-825x550.png)
- Under **Order Management**, select **Enter short position** to have the strategy submit a **Sell Market order**, then click **OK**.


![SimpleMACrossoverBuilderStep18](https://cdn.sanity.io/images/1hlwceal/production/46877811b9af6fa6572f78ee0f01aa19cd5afe2a-303x500.png)


Once finished, we will have condition sets that look like the following:


![SimpleMACrossoverBuilderStep19](https://cdn.sanity.io/images/1hlwceal/production/c6e28c4e0ca3960687f05d185403dce774020b35-825x550.png)


![SimpleMACrossoverBuilderStep20](https://cdn.sanity.io/images/1hlwceal/production/6598cf0d785be9850342c5cb20a49547ffc809ba-825x550.png)
