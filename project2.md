## Project 3

(1) Binary Target Models

- Best

    - The highest wealth group had had the best binary model by far, reaching accuracy's in the high 90s. There was no 
    issues with being overfit as the test accuracy was 0.9608046412467957, which was right on par with the training
      accuracy. In terms of other modifications I the setting used the other day remained the most effective. The batch
      size was left at 256, the optimizer adam performed the best compared to others I tried, and all the features
      were assigned to the correct Keras Preprocessing Layers. 

![img_66.png](img_66.png)         ![img_67.png](img_67.png)


- Worst 

    - The second wealth group had the worst accuracy, resting in the low 70s. It also was not overfit with a test 
  accuracy of 0.7417047023773193. Although, the accuracy also seems to remain for stagnant across epochs which is 
      very odd.
    
![img_69.png](img_69.png)         ![img_70.png](img_70.png)

- Confusion Matrix and Analysis 

![img_68.png](img_68.png)         ![img_71.png](img_71.png)

   - After examining the confusion matrix's for both models it quickly can be discovered that neither model is really
that good. The only reason the 5th wealth class has such a higher accuracy is because it has less individuals within it
     than any of the other classes. This model has failed to classify any of the target's correctly within the binary
     model. This puts forth the idea that accuracy cannot always be trusted as an accurate measurement, especially within
     a binary model like this.

(2) Categorical Target Models

- 


- Confusion Matrix and Analysis 


(3) Results of structured data with feature columns models
