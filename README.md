# ETL

The notebook with the whole project is "ETL Project"

Extract:
We extracted information from two supermarket: Chedraui and Soriana. We did this by scraping the data from the fruits department 
and obtaining the products and prices. 

Transform:
We used the library fuzzywuzzy to get a match of the products from both supermarkets and then compare the prices. After the function,
we added the matches to a dictionary. We passed al the data to a structured table to insert it to SQL.

Load:
We uploaded the table of the matching products to postgres. We decided to use SQl because it is a stuctured database, and thinking that
a lot of users will consult the data, this is the most efficient and reliable way. 

Challenges:
The first challenge we encounter were the web pages of the supermarkets. We first tried Cornershop but Chedraui appeared to be offline. We decided to use the separate webpages of the supermarkets. The web page of Chedraui had no problem, but the Walmart's page was really difficult to scrape, so we moved on to Soriana. When scraping we used the wait time fuction for the extraction to work.

We took some time to decide and figure out a way to match the products of Chedraui and Soriana so we could compare prices. It was hard because sometimes it was the same product, but it didn't have the exact same name. We discovered the fuzzywuzzy library that matches strings and worked with that designing a function to get the matches. This library uses a similarity ratio to define the accuracy of the string matches. The one we used was a ratio of 80.

The challenge we encounter in SQL was passing the data to numeric values and the objects to string values.







