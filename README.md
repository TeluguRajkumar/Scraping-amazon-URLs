# Scraping-amazon-URLs
scrape a minimum hundred URLs using BS4 

# Features
Extract product data from the search result(by category, by country)
Extract lots of signle product data by using ASIN id
Extract product reviews data by using ASIN id
Extract list of categories
Is supporting all available Amazon Marketplaces
Sort result by sponsored products only
Sorts result by discounted products only
Result can be saved to the JSON/CSV files
You can scrape up to 500 produtcs and 1000 reviews

![image](https://user-images.githubusercontent.com/71225421/153131363-dd38b7eb-9ca9-4140-b730-331e7ae5ef6f.png)

![image](https://user-images.githubusercontent.com/71225421/153131494-1872bc7b-605e-4a72-8c0a-c057fb086f4c.png)

Note:

Empty parameter = empty value
Possible errors

If there will be let me know

#Example
Scrape 40 producs from the amazon search result by using keyword "vacume cleaner" and save result to the CSV file

$ amazon-buddy products -k 'vacume cleaner' -n 40 --filetype csv
Output: 1552945544582_products.csv

Example 2
Scrape 40 producs from the amazon search result by using keyword "vacume cleaner" and display raw result in the terminal

$ amazon-buddy products -k 'vacume cleaner' -n 40 --filetype ''
Example 3
Scrape 40 producs from the amazon search result by using keyword "vacume cleaner" from the Amazon.NL(Netherlands) and display raw result in the terminal

$ amazon-buddy products -k 'vacume cleaner' -n 40 --filetype '' --country NL
Example 4
Scrape 40 producs from the amazon search result from the category "Apps & Games" by using keyword "games" from the Amazon.ES(SPAIN) and display raw result in the terminal

$ amazon-buddy products -k 'games' -n 40 --filetype '' --country ES --category mobile-apps
Example 5
Scrape 100 reviews from a product by using ASIN. NOTE: ASIN is a uniq amazon product ID, it can be found in product URL or if you have scraped product list with our tool you will find it in the CSV/JSON files

$ amazon-buddy reviews B01GW3H3U8 -n 100
Output: reviews(B01GW3H3U8)_1589470878252

Example 6
Scrape 300 producs from the "xbox one" keyword with rating minimum rating 3 and maximum rating 4 and save everything to the CSV file

$ amazon-buddy products -k 'xbox one' -n 300 --min-rating 3 --max-rating 4
Output: 1552945544582_products.csv

Example 7
Show list of all available countries

$ amazon-buddy countries

Output: ![image](https://user-images.githubusercontent.com/71225421/153131984-27b505c7-da27-4562-896a-33dd4515f329.png)


Example 7
Show list of all available categories from the Amazon.CO.UK

$ amazon-buddy categories --country GB
Output:
![image](https://user-images.githubusercontent.com/71225421/153132053-f81b5a95-940a-467e-996d-c15cbae776e2.png)

#Module:
Methods
.products() - product search
.reviews() - reviews search
.asin() - single product details
.categories() - available categories


