# IBM-Data-Science-Capstone
* Created a tool that predict rocket landing outcomes to help SpaceY, a virtual company that is a competitor of SpaceX, who want to determine landing outcome and reduce launching cost.
* Scraped hitorical launching data from Wikipedia.
* Optimized K-nearest , Desicion Tree, Logistic using GridSearchC to reach the best model.
**

## Code and Resourse Used
Python Version: 3.9   
Packages: BeautifulSoup, pandas, numpy, sklearn, matplotlib, searborn  
Data from Wikipedia: https://en.wikipedia.org/wiki/List_of_Falcon_9_and_Falcon_Heavy_launches
**

## Web Scraping
* Used python package beautifulsoup as a web scraper to extract 93 hitorical data of SpaceX Falcon 9 launching.
* With each launch, we got the following:
  * Date and time  
  * Version booster   
  * Launch Site  
  * Payload  
  * Payloadmass  
  * Orbit  
  * Customer  
  * Launch outcome  
