# ETL

Extract:
We extracted information from two supermarket: Chedraui and Soriana. We did this by scraping the data from the fruits department 
and obtaining the products and prices. 

Transform:
We used the library fuzzywuzzy to get a match of the products from both supermarkets and then compare the prices. After the function,
we added the matches to a dictionary. We passed al the data to a structured table to insert it to SQL.

Load:
We uploaded the table of the matching products to postgres. We decided to use SQl because it is a stuctured database, and thinking that
a lot of users will consult the data, this is the most efficient and reliable way. 
