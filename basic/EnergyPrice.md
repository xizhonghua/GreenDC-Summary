Energy Price
---


### Carbon market dynamics
[Le-2010](https://github.com/hxwang/Seminar/blob/master/Paper-Summary/LeB10_Managing-the-cost-energy-consumption-and-carbon-print-of-internet-services.md) make the decision of cap-and-trade policy based on the market price of carbon offsets. Using real futures market data from [PointCarbon](https://github.com/hxwang/Seminar/blob/master/Paper-Summary/traces/PointCarbon.md), they find that
- although there can be periods of variability, the carbon prices exhibit consistent trends even at relatively short time scales
- it takes at least a few hours for price to change appreciably

These observation suggest that market-based decisions will be meaningful; excessive variability or the absence of clear trends could render our decision inadequate in just a short time.In other words, the price is relatively stable in a short time, thus the scheduling scheme can be changed periodically.

### Energy price in distributed data center
"Geographica load balancing" has been suggested to reduce energy cost by exploiting the electricity price differences across regions. However, this reduction of cost can paradoxically increase the total energy use [[Liu-2011]](https://github.com/hxwang/Seminar/blob/master/Paper-Summary/LiuL11_Greening-Geographical-Load-Balancing.md).
