Mateo Chapatte  
Guillaume Vray  
Guillaume Parchet  

We chose to propose an additional research questions that can be answered using the dataset used in the paper.

1. Title:

Impact of wealth on eating habits in Greater London

2. Abstract:

While the paper validates its dataset in representativeness and ecologically, we propose use it to study the impact of wealth on eating habits in Greater London at ward level in 2015 and see if there are inequalities at this level. We use official geographically-salient ward indicators which can be found in the official London site to associate to each ward a wealth indicator like the median household income estimate. We represent eating habits by the calories distribution given by each nutrient and their entropy. We observe distribution differences using low dimensional visualization methods and geographic heatmaps. Then we study whether or not those differences are closely related to social class difference with comparative plots and logistic regression. Using these results, we observe if certain nutrients are more related to a class than another and conclude whether or not there is a relationship between wealth and health.
 
3. Research questions:

1) In Greater London, are there differences in eating habits at ward level ?
2) Is there evidence of social class difference in eating habits ?
3) Do wealthier ward areas buy food that could be judged healthier ?
 
"""TO REMOVE"""
More precisely we will try to answer some of the following hypothesis:
  - Are there correlations between lower revenue ward populations and the amount of soft drinks, sweets and ready-made food products.
  - Is the amount of certain nutricients (like saturated fats, free sugars, fibers) significatively different in certain ward populations.
  - ( Is food entropy a relevant factor of wealth ? )
  - ( others ? **TODO** )
   
These hypothesis might help us to bring elements of answer to the more general question: "Do wealthier ward areas buy food that could be judged healthier ?"
 
4. Proposed Datasets:
 - ["Area-level grocery purchases"](https://figshare.com/collections/Tesco_Grocery_1_0/4769354/2) datasets from the Tesco paper "Tesco Grocery 1.0, a large-scale dataset of grocery purchases in London". We will especially use the dataset given in milestone P2 (year_osward_grocery.csv), the aggregation at ward levels. This dataset will give all the informations related to bought products, their categories and associated nutrients (food informations). It also presents the representativeness of each area which will allow us to qualify our results.
 - ["ward-profiles-excel-version.csv"](https://data.london.gov.uk/dataset/ward-profiles-and-atlas) dataset issued by Greater London Authority and shared by London Datastore. It contains a wide range of statistial informations on wards' population, this will help us to find an estimate of the health level of each ward. It contains informations like "Employement rate", "Median house price", "Median household income estimate", % adult with and without qualifications".
The main advantage of these two datasets is that they are both indexed by the same wardsIDs, making the merging task much easier. The two datasets can be found online (see the refered linked above) and come from credible sources (replication of Tesco paper was succesful and the second dataset contain official statistics).

"""TO REMOVE"""
EDIT: NOT RELEVANT TO ME -> The two datasets are pretty small in size (1537Ko and  830Ko respectively), they contain **X** and **Y** datapoints (number of wards) each and **Z** column informations (**TODO, check numbers**), they have standard comma separated values format. We will only use a few of the columns contained in ward profile (probably 'Employement Rate', 'Median House price', Median Household income estimate' and other wealth estimates). 
 
5. Methods:

The main methods we might use are:
 - T-sne visualization
 - Logistic regression
 - K-means
 - Statistical tests (statmodels)
 - **(TODO : others ? Ca serait pas mal d'en trouver d'autres) - pas besoin de rajouter pour rajouter**
 
6. Organization within the team:

1) Data preparation
 - Import the different datasets and apply cleaning methods if required
 - Keep the 80% most representative wards (representativeness > 0.1)
 - Compute a ward population class label using K-means on wealth markers
2) Visualization of eating habits at ward level
 - Visualize eating habits with T-sne using f_aliments and f_nutrients features and answer first question
 - Visualize fraction of each nutrient at ward level on a london map using plotly, geopandas
 - Compare the last visualization with a class visualization using the wealth markers and the class label
 - Hypothetize about question 2 and 3.
3) Verify the hypotheses
 - Within each class, compare distribution of nutrient fraction and entropy and make statistical tests
 - Use logistic regression to predict classes with nutrients and entropy and observe if there are significant relations
 - Analyse if there are significant difference distribution of nutrients within each population class with our results
 - Observe if fats and sugars fractions are more important in lower class population. Make same observations for protein, fibre and entropy
4) 
 - Create a short video summarizing our approach and findings
 
 
7. Questions for TAs:
 - Our work requires more statistical effort (like statmodels) rather than heavy Machine Learning methods, is it a problem ? **(TO REMOVE ? vous en pensez quoi ?) - On peut laisser on a rien à perdre**
 
 
 
 
 
 
