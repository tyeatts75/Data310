## Monday (8/2) Response (Abstract)

(1) Presentation Title:

- Features most Correlated to Happiness within a Nation 

(2) Abstract First Draft

- The research question I have chosen to pursue is to figure out what traits contribute to making a country the 
  happiest. To explore this I found a dataset on Kaggle that has information on 156 different countries. Each country 
  has a target variable, which is their World Happiness Report Score, and then features such as economic production, 
  social support, life expectancy, freedom, absence of corruption, and generosity. Kaggle had the data sets for several 
  different years, I choose the 2019 dataset due to it being the most recent. I used this data to then train a model 
  that can predict a nation’s happiness based on the various features. The goal of this was to then experiment with 
  the features to determine which combination of features creates the most accurate model. This then allowed me to 
  determine what factors are most indicative of determining how happy someone will be within a particular country. 
  
- Breakdown of Data

    - 146 Countries
    
    - 6 Features:
      
        - GDP per capita
        - Social support
        - Healthy life expectancy
        - Freedom to make life choices
        - Generosity
        - Perceptions of corruption
        - Each of the features presented, aside from GDP per capita, taken from the Gallup World Poll. This poll surveyed
    citizens from each country and asked them to rank its country on each feature on a scale of 0 to 10. The data was
      made representative by using Gallup's weights, which explains the specific numbers each country has for their
      various features.
          
    - Target is Happiness Report Score
    
    - 2 Removable Columns 
    
        - Country Name
        - Overall Happiness Rank
