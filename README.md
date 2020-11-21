Mateo Chapatte  
Guillaume Vray  
Guillaume Parchet  

We chose to propose an additional research questions that can be answered using the dataset used in the paper.

1. Title:

Impact of wealth on eating habits in Greater London

2. Abstract:

**TODO**
 
3. Research questions:

Are there significant correlations between eating habits and wealth in Greater London ? 
 
More precisely we will try to answer some of the following hypothesis:
  - Are there correlations between lower revenue ward populations and the amount of soft drinks, sweets and ready-made food products.
  - Is the amount of certain nutricients (like saturated fats, free sugars, fibers) significatively different in certain ward populations.
  - ( Is food entropy a relevant factor of wealth ? )
  - ( others ? **TODO** )
   
These hypothesis might help us to bring elements of answer to the more general question: "Do wealthier ward areas buy food that could be judged healthier ?"
 
4. Proposed Datasets:
 - ["Area-level grocery purchases"](https://figshare.com/collections/Tesco_Grocery_1_0/4769354/2) datasets from the Tesco paper "Tesco Grocery 1.0, a large-scale dataset of grocery purchases in London". We will especially use the dataset given in milestone P2 (year_osward_grocery.csv), the aggregation at ward levels. This dataset will give all the informations related to bought products, their categories and associated nutrients (food informations).
 - ["ward-profiles-excel-version.csv"](https://data.london.gov.uk/dataset/ward-profiles-and-atlas) dataset issued by Greater London Authority and shared by London Datastore. It contains a wide range of statistial informations on wards' population, this will help us to find an estimate of the ealth level of each ward.  
The main advantage of these two datasets is that they are both indexed by the same wardsIDs, making the merging task much easier. The two datasets can be found online (see the refered linked above) and come from credible sources (replication of Tesco paper was succesful and the second dataset contain official statistics). The two datasets are pretty small in size (1537Ko and  830Ko respectively), they contain **X** and **Y** datapoints (number of wards) each and **Z** column informations (**TODO, check numbers**), they have standard comma separated values format. We will only use a few of the columns contained in ward profile (probably 'Employement Rate', 'Median House price', Median Household income estimate' and other wealth estimates). 
 
5. Methods:

The main methods we might use are:
 - Linear regression
 - K-means (unsupervised Machine Learning)
 - Cross-validation (on K-means)
 - Statistical tests (statmodels)
 - **(TODO : others ? Ca serait pas mal d'en trouver d'autres)**
 
6. Organization within the team:
In order to answer our different hypothesis we will probably follow the following procedure:
 - Import the different datasets and apply cleaning methods if required
 - Find an estimate of the wealth level of each ward
 - Categorize these wealth levels into clusters (probably using K-means)
 - Study the different food informations at each ward level (mainly nutrients, food category, entropy)
 - Determine if there exists significant correlations answering our hypothesis
 - Create a short video summarizing our approach and findings
 
7. Questions for TAs:
 - Our work requires more statistical effort (like statmodels) rather than heavy Machine Learning methods, is it a problem ? **(TO REMOVE ? vous en pensez quoi ?)**
 
 
 
 
 
 
