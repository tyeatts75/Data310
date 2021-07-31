## Thursday (7/29) Response

(1) Generated Text

- The goal of this script is to create a model that imputs a script and then creates its own script from that imported
text. This example used Romeo and Juliet, here are the results of my model:

    - KING RICHARD II:
      Come yor I may believe you post adide;
      And I are come to Plandageous lend
      Their transmen feign that, march'd to this Pedarous!
      Hear me speak for I Clarence, do you think, you here is now.
      
      PROSPERO:
      O heavens! Rale old fear, Signior Gremio.
      Thou hast clean disnior brother Montague?
      As on a cause I have been doged, like lightnoos, if
      Without any furgetted man:
      Clarence, help, though mine enemies;
      I'll follow'd in duty, and as we def ass
      swiftly but a despair of you to't: give thy slave,
      That once point store of this: he delivered using mooth
      As when the searchables wretched hours.
      Here in this coffing turness precass,
      A watchful sprite. Will't plegeate to lose away.
      
      CAMILLO:
      I would he pray,
      That thought these knows leins, your eye-grave for a child.
      
      DUCHESS OF YORK:
      Had muffled here, for mine eyes,--which way
      I will withdraw with us, and let us hear,
      You both, and well Ino


(2) Steps:

- (1) Processing, vectorizing and predicting text

    - The first step, the processing step, actually contains several substeps. The first is that the imported text must
    be vectorized. This means that the text strings must be switched over to numerical features. The 
      preprocessing.StringLookup layer is used to do this conversion. The following step is to create training examples
      and targets to help the model with predicting text. The first aspect of this is to split the text into example
      sequences, which is then followed by making the dataset consists of (input, label) pairs. The last aspect of the
      first step is to create training batches, this model has a batch size of 64.
    
- (2) Building and training the model

    - The following step is to actually build and train the model. To build it keras is used and three layers are
    implemented. The three keras layers are an embedding layer, GRU layer, and the final output layer. Next up is to 
      train the model. Before training can begin standard sparse categorical crossentropy is applied for the loss
      function and adam is used as the optimizer. This model also implements a feature to save various checkpoints
      throughout the model to make sure text is saved during training. Once these steps are complete the model can be
      executed. Due to the long runtime only 20 epochs were used for this model. The loss of the final epoch
      was 0.7284.
    
- (3)Generating text

    - The final step of this script is to actually generate new text based on the imported Romeo and Juliet script.
    The best way to generate the text it to run the model in a loop which will lead to a continuous output of new
      characters. To do this a class called OneStep is created with various function inside that will assist in the 
      completion of this task. At the conclusion of this step the new text that is pasted above was created.
      
  