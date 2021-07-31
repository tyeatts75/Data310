## Thursday (7/29) Response

(1) Generated Text

- The goal of this script is to create a model that imputs a script and then creates its own script from that imported
text. This example used Romeo and Juliet, here are the results of my model:

    - ROMEO: With cainus.
      
      VOMFETIS:Nome! No, we man thou sirraty, Bediging yet on yet, orh proscesp traitand, With were him. with a vollitamed. 
      Sorray, like the ackon'd king and 
      love of dive and lise; As king one our arucument of lord I have ne'll gord, You frieve that vilet lequet on fears.
      
      Sitone: I collmenter now, Unllaght fromor, perculander: I hone copprarabll:Boy'd thy first what fetly contuer is 
      hones, therefore lard in a moumpy was my ictur again;
      And sard I devere as exer, withough lay's
      To charbs frient to fleat.
      SCpeacens arains, thisp forizes:
      Anf trinoc: Pratue thou will are marry countling with flie.
      
      AMENII:
      You knee or the catuly. Sage issed, do your ford wither;
      Aight gond thou masteres beckin be comitunal,; I am not thou nord
      Woll! why, father more
      Meink some amont goon unocked is all;
      Withow your liegh, feering erem outless but.
      
      SICFroRIZA:
      You wellen'd sinter whichs: fran; to how they westing.
      
      SOSPERSIO:
      A will know, I breghty brotherr woulds;
      Ane the duhes of, wenten the


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
      executed. Due to the long runtime only 3 epochs were used for this model. The loss of the third and final epoch
      was 1.7221.
    
- (3)Generating text

    - The final step of this script is to actually generate new text based on the imported Romeo and Juliet script.
    The best way to generate the text it to run the model in a loop which will lead to a continuous output of new
      characters. To do this a class called OneStep is created with various function inside that will assist in the 
      completion of this task. At the conclusion of this step the new text that is pasted above was created.
      
  