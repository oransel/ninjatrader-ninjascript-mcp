# BarsAgo

Source: https://developer.ninjatrader.com/docs/desktop/barsago

---

# BarsAgo


## [Definition](https://developer.ninjatrader.com/docs/desktop/barsago#definition)


Gets the number of bars back (x-axis coordinate) the chart anchor is drawn by a NinjaScript object. This value is the direct value which was passed to a NinjaScript Draw method. Please see the [Drawing](https://developer.ninjatrader.com/docs/desktop/drawing) section for more information.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This value will NOT work on manually drawn objects. This property is reserved for chart anchors which were drawn by another NinjaScript object (e.g, using a Draw method in an indicator). For manually drawn objects, please see the [SlotIndex](https://developer.ninjatrader.com/docs/desktop/barindex) property.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/barsago#property-value)


A **int** value that value representing the **barsAgo** value used to drawn the anchor. This property is read-only.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/barsago#syntax)


`<chartanchor>.BarsAgo`
