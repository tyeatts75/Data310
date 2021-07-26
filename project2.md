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

- The model that examines all categorical targets did very poorly. It had a test accuracy of 0.5162795782089233 and 
the training and validation accuracies were both very low as well. To calculate loss for this model I used
  Sparse Categorical Crossentropy; similarly, I used Sparse Categorical Accuracy to get the accuracy. I also needed
  to change the density in the last layer of the model to six to get the model to run and account for all five
  targets.

![img_72.png](img_72.png)

![img_73.png](img_73.png)

- Confusion Matrix and Analysis 

![img_65.png](img_65.png)

  - Examining the confusion matrix this model did much better than the last because it could actually classify some
of the variables. It appears most of the misclassified individuals were typically not too far from their correct class,
    usually being only one over. With some more work, this model has lots of room for improvement. 

(3) Results of structured data with feature columns models

- Initial Model

![img_76.png](img_76.png)

![img_75.png](img_75.png)

![img_74.png](img_74.png)


  - This model is very poor, much worse than the previous categorical model with the preprocessing layers. It has an
abysmal accuracy and pretty much fails to classify all individuals in the second and third wealth classes. In regards
    which features I put in each feature columns I kept it pretty simple. I put weights and units as numeric, I
    bucketized age, size, and education, and then I placed location, cook, car, electric, toilet, potable,
    gender all within indicator columns. With the poor success of this model I feel it may be more worth my time to
    try and improve the previous model.
    

(4) Model Improvement

- With the feature columns model performing so poorly I decided to make some changes to the categorical keras
  preprocessing layers model in an effort to make improvements.
  
- After toying around with dropping various features and combinations of features I found no combination of variables
that improved my model. This is very odd, even when I removed the features that were missing a lot of data points the
  model still seemed to be better off beforehand. 