## Thursday (7/15) Response: Tyler & DJ

(1) Overview of Model

- This dataset contains a variety of different features that can be utilized to create a model that can predict an
individual's wealth. Before the model could be put together we made sure to drop hhid and pnmbr from the dataset as we
  felt they were not necessary. From there we imputed the features that were to be used based on what type of variable
  they were. The first step was to input the numeric variables, in this case weights were the lone variable here. The 
  next section was the categorical variables that were encoded as integers. There were an abundance of features here,
  such as: age, gender, size, education, and unit. The final aspect was to input the categorical variables that were
  encoded as strings. These features consisted of location, cook, car, electric, toilet, and potable. Once these steps
  were completed training could begin. Our model didn't alter much from the initial code, as we left the batch size at
  256 and left the optimizer unaltered. We ran the model for each level of wealth and the results are listed below.

(2) Wealth = 1

![img_49.png](img_49.png)

![img_50.png](img_50.png)

(3) Wealth = 2



(4) Wealth = 3

(5) Wealth = 4

(6) Wealth = 5

(7) Final Observations 

- 