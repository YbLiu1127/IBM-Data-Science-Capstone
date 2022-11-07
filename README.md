# IBM-Data-Science-Capstone
* Created a tool that predict rocket landing outcomes to help SpaceY, a virtual company that is a competitor of SpaceX, who want to determine landing outcome and reduce launching cost.
* Scraped hitorical launching data from Wikipedia.
* Optimized K-nearest , Desicion Tree, Logistic using GridSearchC to reach the best model.   


## Code and Resourse Used
Python Version: 3.9   
Packages: BeautifulSoup, pandas, numpy, sklearn, matplotlib, searborn  
Data from Wikipedia: https://en.wikipedia.org/wiki/List_of_Falcon_9_and_Falcon_Heavy_launches  


## Web Scraping
* Used python package beautifulsoup as a web scraper to extract 93 hitorical data of SpaceX Falcon 9 launching.
* With each launch, we got the following:
  * Flight No. 
  * Launch Site     
  * Payload  
  * Payloadmass  
  * Orbit  
  * Customer  
  * Launch outcome  
  * Version Booster
  * Booster landing
  * Date
  * Time


## Data Cleaning and Wringling  
After scraping the data, I needed to clean it up so that it was usable for our model. I made the following changes and created the folowing variables.
* Filter the dataframe to only include Falcon 9 launches  
* Replace the missing payloadmass value with average payloadmass  
* Add a new label "Class" to determine whether each landing was succeeed or not.  


## Feature Engineering
After data cleaning, feature engineering needed to bo done by following changes to obtain preliminary insight about how each important variable would affect success rate. 
* Extract following features into feature dataframe.  
  * FlightNumber 
  * Payloadmass
  * Orbit
  * LaunchSite
  * Flights
  * GridFins
  * Reused
  * Legs
  * LandingPad
  * Block
  * ReuseCount
  * Serial
* Create dummy variables to following categorical columns:  
  *   Orbit
  *   LaunchSite
  *   LandingPad
  *   Serial


## Exploratory Data Analysis
Analysis and finding are discussed in pdf file "Data-Science-Capstone_Yen-Po_Liu"


## Model Building
First, I split the data into train and tests sets with a test size of 20%  

I tried four different model and evaluated the by R squred.  
Four models are:
 * Logistic Regression - Because if the landing outcome label would be perfect pridicted if there were possibility with result respectively. Make the prediction more intuitive.   
 * SVM - The dataframe has totally 83 features after feature engineering, it would be more computed-effeciently to apply SVM building a model.
 * Desicion Tree - Baseline for the model
 * K-nearest 

## Model Performance
The Desicion Tree model outperformed the other approaches on the test and validation sets.

* Logistic Regression: 0.83 
* Support Vectory Machine: 0.83 
* Desicion Tree: 0.89 
* K-nearest neighbors: 0.834 
