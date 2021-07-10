## Project 1

(1) How did your model fare?

![img_15.png](img_15.png)
![img_18.png](img_18.png)
-  Using the zillow scraper, I gathered data from an abundance of homes within the City of Charlottesville. Originally, I
had planned to use Chicago, but I noticed too many outliers and variance in the price based on location, so I decided to 
   switch locations. The model for homes in Charlottesville fared pretty well, with many of the lower value homes 
   doing very well. When it came to the higher value homes there was a much higher variance in success, as can be seen
   on the plot. Also, when looking at the loss it has a large drop after the first few epochs, but then a very staticy
   up and down trend can be noticed.

(2) In your estimation is there a particular variable that may improve model performance?

-  Regarding an additional variable that could improve the model, I believe that finding a way to specify where in a
city a home is located could be very helpful. For instance, the reason my initial attempt at using chicago didn't work
   is because there is a significant price difference between southside and downtown Chicago for example. To elaborate
   further, 2 bedrooms, 2 bathrooms, and 2000 square feet will cost much different depending on where it is located. 
   To help the model improve an extra feature such as zip code would be very helpful. This would allow the model to 
   analyze which homes are in which zip and then determine an adequate price. 

(3) Which of the predictions were the most accurate? In which percentile do these most accurate predictions reside?
Did your model trend towards over or under predicting home values?

-  The predictions closer to the lower price ranges tended to be much more accurate. This would equate to homes within
the lower percentiles to be much more accurate. In regards to over and under predicting values, it appears that there is
   about an even mix of both amongst the predictions.

(4) Which feature appears to be the most significant predictor?

- The feature that appears to be most strongly correlated to the price is livingArea. 
 
