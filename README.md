# Zillow-Clustering-Project
# Estimating Home Value
(----)                  
## Project Description


### What Is Zillow?
> "As the most-visited real estate website in the United States, Zillow and its affiliates offer customers an on-demand experience for selling, buying, renting and financing with transparency and nearly seamless end-to-end service. Zillow Offers buys and sells homes directly in dozens of markets across the country, allowing sellers control over their timeline. Zillow Home Loans, our affiliate lender, provides our customers with an easy option to get pre-approved and secure financing for their next home purchase. Zillow recently launched Zillow Homes, Inc., a licensed brokerage entity, to streamline Zillow Offers transactions."  [zillow.com] (https://www.zillow.com/z/corp/about/)

### Background
Scenario: You are a junior data scientist on the Zillow data science team and recieve the following email in your inbox:

> We want to be able to predict the property tax assessed values ('taxvaluedollarcnt') of Single Family Properties that had a transaction during 2017.

> We have a model already, but we are hoping your insights can help us improve it. I need recommendations on a way to make a better model. Maybe you will create a new feature out of existing ones that works better, try a non-linear regression algorithm, or try to create a different model for each county. Whatever you find that works (or doesn't work) will be useful. Given you have just joined our team, we are excited to see your outside perspective.

> One last thing, Zach lost the email that told us where these properties were located. Ugh, Zach :-/. Because property taxes are assessed at the county level, we would like to know what states and counties these are located in.

-- The Zillow Data Science Team

### Deliverables
1. Presentation
     -  5 minute presentation
2. Github repository containing all work
     - 1 final jupyter notebook 
     - 1 explore notebook
     - 1 model notebook
3. README.md file

### Data Dictonary
| Feature | Description | Data Type |
|-|-|-|
| bathroomcnt | Number of bathrooms in home including fractional bathrooms | int |
| bedroomcnt | Number of bedrooms in home | int |
| buildingqualitytypeid | Overall assessment of condition of the building from best (lowest) to worst (highest) | int |
| calculatedfinishedsquarefeet | Calculated total finished living area of the home | float  |
| fips | Federal Information Processing Standard code | object |
| parcelid | Unique identifier for parcels (lots) | float |
| regionidneighborhood | Neighborhood in which the property is located | int |
| unitcnt | Number of units the structure is built into (i.e. 2 = duplex, 3 = triplex, etc...) | float |
| yearbuilt | The Year the principal residence was built | int |
| taxvaluedollarcnt | The total tax assessed value of the parcel | float |
| taxamount | The total property tax assessed for that assessment year | float |


## Hypotheses
### Initial Hypotheses (Prepare Phase)
1. Is there a linear correlation between square footage and tax value?
2. Is there a linear correlation between number of bathrooms and tax value?
3. Is there a linear correlation between number of bedrooms and tax value?

## Project Planning
### [Zillow Project Plan Board](https://trello.com/invite/b/BEPFoCDR/2f80bf3ffba0a8c8077dd21b8814bfed/zillow-clustering-project)
### Aquire
* Gather data from Codeup database using SQL 
* Create function with python that gathers data from SQL and reads it into a dataframe
* Create acquire.py file with function to acquire data
### Prepare
* Clean up:  missing values, data integrity issues, data types, invalid data
* Scale: numeric data (if necessary)
* Plot: individual distributions of individual variables
* Split:  split dataset into train, validate, and test
* Create prepare.py file that contains all functions used to prepare data
### Explore
* Perform at least 1 t-test and 1 correlation test 
* Visualize all combinations of variables
* Determine variables that are correlated with each other
* Summarize takeaways and conclusions
### Model
* Establish and evaluate baseline model
* Use various algorithms to develop model that beats baseline
* Create a model.py file that includes functions to fit, predict, and evaluate final model on the test data set
## How to Reproduce
1. Clone or fork this repository
2. Download the following files into the directory you wish to work in: aquire.py, prepare.py, explore.py, and zillow_regression.ipynb
3. Run the zillow_regression jupyter notebook in its entirety
4. Modify features/models/etc how you see fit