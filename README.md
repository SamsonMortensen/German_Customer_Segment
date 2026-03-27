
# Customer Segmentation for Arvato Financial Solutions #

## Project Overview ##

In this project, I applied unsupervised learning techniques to identify segments of the population that form the core customer base for a mail-order sales company in Germany. By clustering the general population and comparing it to the company's existing customer data, these segments can be used to direct marketing campaigns towards audiences that will have the highest expected rate of returns. The dataset was provided by Bertelsmann Arvato Analytics.

## Data Sources ##

There are four primary files utilized in this project:

Udacity_AZDIAS_Subset.csv: Demographics data for the general population of Germany (891,211 persons x 85 features).

Udacity_CUSTOMERS_Subset.csv: Demographics data for customers of a mail-order company (191,652 persons x 85 features).

Data_Dictionary.md: Detailed information file about the features.

AZDIAS_Feature_Summary.csv: Summary of feature attributes.

## Tools & Technologies ##

* **Language:** Python
* **Libraries:** Pandas, Scikit-learn
* **Methodology:** Supervised Machine Learning, Parameter Optimization
* **Environment:** Jupyter Notebook


## The Problem ##

Applying a one-size-fits-all approach to diverse populations results in massive inefficiencies. In a logistics or supply chain context, treating an entire country as a single block results in misallocated inventory and higher transportation costs. The objective of this analysis is to:

1. Process and scale complex demographic data to prepare it for machine learning algorithms.
2. Apply unsupervised clustering techniques to identify hidden groupings within the population.
3. Translate those mathematical clusters into actionable operational profiles.


**Data Preprocessing & Cleaning Process**

To prepare the raw demographics data for the unsupervised learning model, several rigorous cleaning steps were executed:

Parsed the feature attributes summary to map and convert custom missing value codes into standard NaN values.

Assessed the distribution of missing data across all 85 columns. Dropped 6 outlier columns (TITEL_KZ, AGER_TYP, KK_KUNDENTYP, KBA05_BAUMAX, GEBURTSJAHR, ALTER_HH) that were missing more than 30% of their values to prevent introducing noise into the downstream modeling.

Row-Level Cleaning: Calculated missing values per row and divided the data into two subsets (high missing data vs. low missing data) to ensure only high-quality data was fed into the clustering algorithm.

## Core Insights & Conclusion ##

By mapping the core customer segments against the general population, the model provided clear, actionable guidance for future marketing strategies:

Target Audience (Cluster 5): The primary customers of the mail-order company are older adults with moderate wealth who tend to be cautious with their finances and show little interest in complex financial products. Marketing efforts aimed at acquiring new customers should focus heavily on this demographic.

Low-Return Audience (Cluster 0): Younger people who are more actively involved in managing their finances are largely missing from the customer base. It would be wise to avoid spending resources targeting this group, as they are unlikely to respond well to the company’s current approach.
