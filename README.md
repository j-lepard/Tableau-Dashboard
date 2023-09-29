# Final-Project-Tableau

## Project/Goals
(fill in your description and goals here)

## Data Sources:
1. [Cause of Death - Our World In Data](https://www.kaggle.com/datasets/ivanchvez/causes-of-death-our-world-in-data?resource=download).
2. [World Population review](https://worldpopulationreview.com/countries)

## Process
* Data Aquisition
* Feature Engineering
  * Create the Categories (summary)
### (your step 2)

## Results
(Fill in which Option you chose, either 1 or 2. List the dataset you selected for the project if you selected Option 2. Also, discuss the visualizations you created, and why. For Option 2, also identify what your data question was, and how you went through the prompts.)

## Challenges 
(discuss challenges you faced in the project)

## Future Goals
(what would you do if you had more time?)

## NOtes
- looked at world map first. Selected various measures to see if any signgificatn geographic differences. 
- maternal in sudan, mental health in north. 
- normalized the data against country population. 
- ** Clustering **
- 
- Ivnestigations and hypothesis: 
### Mental Health
  - Hypothesis: related to Density or Latitude?
  - density
  - Latitude (link) https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5302112/

Feature Engineering

   > **Country Density - IQR and outliers:** [Excel]
   > 
   > Determine the percentiles and IQR using  
   >   * QUARTILE.INC(data_range,percentile_desired)  
   > * Categorize country in appropriate group:
   >   * IF(AND(R2>=Lower_outlier,R2<Quartile1),"Quartile 1",  
      IF(AND(R2>Quartile1,R2<Quartile3),"IQR",  
      IF(AND(R2>Quartile3,R2<Upper_outlier),"Quartile 3",  
      IF(OR(R2>Upper_outlier,R2<Lower_outlier),"Outlier",))))'
   > * Refresh Tableau data connection to utilize new column [Density_group]

### Maternal Health
  - Subsarha africa
  - 

### Illness
- Eastern Europe
- Cardiovascular
- Create group of Can/America vs Baltics
- compare trends over time with forecast (unadjuested per pop)