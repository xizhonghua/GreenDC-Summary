## Solar Energy Prediction

### Estimated Weighted Moving Average (EWMA)
- Solar energy prediction is typically obtained with EWMA models, because of its relative consistency and predic patterns [[Holt-2004]](http://www.sciencedirect.com/science/article/pii/S0169207003001134).
- Comments: As long as the weather conditions remain consistent within a period, the prediction is accurate, but becomes inaccurate, with mean error well over 20%, with frequent weather changes. 

### Weather-conditoned Moving Average (WCMA)
- taking into account the mean value across days and a measured factor of solar conditions in the present day relatie to previous day [[Piorno-2010]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=5172412&tag=1). 
- Comments: while this work provides only a single future interval of prediction, it specifically addresses inconsistent conditions, with a mean error of under 10%.
