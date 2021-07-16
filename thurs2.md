## Thursday (7/15) Response 

(1) Using the relevant parts from the entirety of the example script as a guide, fit a CNN model to your training 
data and validate using the beans dataset from Tensorflow datasets and then again train and validate using the 
eurosat dataset. Present your results and discuss the accuracy of each of model.

- Bean:

    -The bean model finished with ok accuracy, if more epochs were to be tested I'm sure it would be higher but at
    its current state it is nothing impressive. The third and final epoch sees the model reaching a .74 accuracy with
      a validation accuracy of .64. This means that the model was fairly overfit, which is not ideal.
      The loss did see a solid loss from each epoch to the next insinuating increases
      in accuracy could have been seen with further epochs.
      

        Epoch 1/3
        26/26 [==============================] - 98s 4s/step - loss: 1.3429 - accuracy: 0.5345 - val_loss: 1.1093 - val_accuracy: 0.4519
    
        Epoch 2/3
        26/26 [==============================] - 98s 4s/step - loss: 0.8009 - accuracy: 0.6663 - val_loss: 0.7481 - val_accuracy: 0.6442
        
        Epoch 3/3
        26/26 [==============================] - 94s 4s/step - loss: 0.6058 - accuracy: 0.7376 - val_loss: 0.7370 - val_accuracy: 0.6442
    
- Eurosat:
  
    -This dataset had similar results to the bean data, with an accuracy around .75. The validation accuracy was a lot
better in this model though, reaching about .75 as well. This means that this model was much less overfit and that
  overall it performed much better than the bean data.
    

        Epoch 1/3
        675/675 [==============================] - 38s 56ms/step - loss: 1.3041 - accuracy: 0.4993 - val_loss: 0.9666 - val_accuracy: 0.6367
        
        Epoch 2/3
        675/675 [==============================] - 44s 65ms/step - loss: 0.8708 - accuracy: 0.6849 - val_loss: 0.7133 - val_accuracy: 0.7311
    
        Epoch 3/3
        675/675 [==============================] - 47s 69ms/step - loss: 0.7023 - accuracy: 0.7474 - val_loss: 0.7139 - val_accuracy: 0.7467

(2)  Apply augmentation to a dataset example, that illustrates a resize and rescale image augmentation 
implementation to the tf_flowers dataset. Apply this same method to both the beans and eurosat datasets. 
Did your model performance improve? How many epochs were you able to run and how much time did it take?
    
- Bean:
  
    -Compared to the previous models, the epochs here oddly ran very quickly. The first time I ran it during class
they took much longer, I find this quick change interesting but welcome. With the quicker epochs I ran 10 of them, 
  which is much greater than the three I ran for the previous models. Looking at the third epoch, which where I 
  stopped for the non-augmented model, this version preformed much worse. It was much less overfit, but also had
  a lower accuracy at around .65. Looking at all the epochs, it appears accuracy stopped increasing at around epoch 7,
  where it hit exactly .74. This means the augmented model at its best, was just as good as the original CNN model 
  with room to improve. It should be noted that this model was, overall, much better fit than the previous.
      

        Epoch 1/10
        26/26 [==============================] - 10s 338ms/step - loss: 1.2110 - accuracy: 0.3809 - val_loss: 0.9305 - val_accuracy: 0.6250
    
        Epoch 2/10
        26/26 [==============================] - 10s 383ms/step - loss: 0.9120 - accuracy: 0.5683 - val_loss: 0.7619 - val_accuracy: 0.6538
    
        Epoch 3/10
        26/26 [==============================] - 11s 398ms/step - loss: 0.7977 - accuracy: 0.6566 - val_loss: 0.7151 - val_accuracy: 0.7019
    
        Epoch 4/10
        26/26 [==============================] - 11s 405ms/step - loss: 0.7344 - accuracy: 0.6832 - val_loss: 0.7365 - val_accuracy: 0.6635
    
        Epoch 5/10
        26/26 [==============================] - 11s 402ms/step - loss: 0.6722 - accuracy: 0.7183 - val_loss: 0.6058 - val_accuracy: 0.7404
    
        Epoch 6/10
        26/26 [==============================] - 12s 437ms/step - loss: 0.7251 - accuracy: 0.6856 - val_loss: 0.6460 - val_accuracy: 0.7404
    
        Epoch 7/10
        26/26 [==============================] - 11s 411ms/step - loss: 0.6545 - accuracy: 0.7400 - val_loss: 0.7643 - val_accuracy: 0.6635
    
        Epoch 8/10
        26/26 [==============================] - 12s 446ms/step - loss: 0.6224 - accuracy: 0.7352 - val_loss: 0.6354 - val_accuracy: 0.7308
    
        Epoch 9/10
        26/26 [==============================] - 13s 473ms/step - loss: 0.6109 - accuracy: 0.7485 - val_loss: 0.5538 - val_accuracy: 0.7404
    
        Epoch 10/10
        26/26 [==============================] - 13s 476ms/step - loss: 0.6005 - accuracy: 0.7388 - val_loss: 0.6200 - val_accuracy: 0.7308

- Eurosat:

  -Unlike the augmented bean data, the augmented eurosat dataset took much longer to load so only three epochs 
      were used. Comparing this model to the non-augmented version, this one performed much worse. It has an accuracy 
      around .68, and oddly a higher validation accuracy at .71. Looking at both these datasets, it appears that augmentation c
      onsistently decreases the accuracy of a model.
      
      
        Epoch 1/3
        675/675 [==============================] - 221s 327ms/step - loss: 1.5202 - accuracy: 0.4253 - val_loss: 1.0136 - val_accuracy: 0.6244

        Epoch 2/3
        675/675 [==============================] - 246s 365ms/step - loss: 1.0778 - accuracy: 0.6030 - val_loss: 0.8014 - val_accuracy: 0.6837
   
        Epoch 3/3
        675/675 [==============================] - 247s 365ms/step - loss: 0.8811 - accuracy: 0.6784 - val_loss: 0.8080 - val_accuracy: 0.7093