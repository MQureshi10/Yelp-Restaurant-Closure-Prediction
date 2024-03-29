# pythonML
Yelp Data Project


Introduction

U.S. restaurant industry sales will reach a record high of $863 billion this year, up 3.6% over last year, across more than 1 million businesses. The industry is continuously growing year after year, and Yelp is one of the biggest platforms of fueling the industry’s growth. 
Yelp was founded in 2004 and their main focus is to help connect people with great local businesses. Yelp is an online directory for discovering local businesses ranging from bars, restaurants, gas stations, and all the way to spas or hairdressers. The listings can be filtered by business type, location, price range, and many more. My focus for the project is restaurant oriented data from Yelp. 

Business Objective

Due to limited information on restaurant sustainability, my objective is to build a machine learning model that will predict restaurant success and closure. This will provide lenders or investors with crucial information which would help them make important business decisions when deciding to invest or lend to different restaurants. In order to achieve this, I needed to locate a dataset that would help us identify different factors that would help display accurate data which would then help these investors make valuable business decisions regarding investing or lending. Since Yelp is one of the largest platforms for the restaurant business, I knew I could rely on them for sufficient data to achieve my goal. 

Dataset Information

The dataset used was one found on Kaggle provided by Yelp. 
●	The dataset is a subset of Yelp’s businesses, reviews, and user data 
●	The dataset contains 5,200,000 user reviews, information on 174,000 businesses, and spans 11 metropolitan areas in 4 countries  
●	The dataset contains 7 csv files: business, business attributes, business hours, check ins, review, tip, and user
Data Pre-Processing
Since the dataset was large and included various types of restaurants in multiple countries, I decided that it was best to focus on a specific area to provide accurate information based on the location of the restaurants. The first step taken was loading the dataset into the Pandas dataframe. After loading the dataset, I filtered the data down to the province of Ontario and furthermore to Toronto. Next, I filtered the dataset to restaurants only as Yelp also has several other types of establishments within their dataset. The filtered dataset contained information about restaurants in Toronto. I then matched up the current Yelp Data with Yelp Data that was last updated two years ago. I compared the restaurants that were open then and closed now and updated the data I would be using to reflect that. This would essentially show the change over two years. I added two categories to the Yelp data. I then figured out which restaurants are a part of a chain using Excel functions and put that information into its own column. I also added a column that assigned a number to each category of restaurant. 
The factors included in the data are: 'business_id', 'name', 'neighborhood', 'address', 'city', 'state', 'postal_code', 'latitude', 'longitude', 'stars', 'review_count', 'is_open', 'categories', 'is_chain', and 'category_number'. To use the data in the machine learning models, I had to narrow it down even further to only numerical data. For the models I used 'latitude', 'longitude', 'stars', 'review_count', 'is_open', 'is_chain', and 'category_number'. The data associated with ‘is_open’ and ‘is_chain’ were made binary, with ‘is_open’ being used as my target. As I tweaked my models further, I found that they all actually performed better when not including the ‘stars’ ratings. When looking at the factors individually, they could not provide accurate predictions on success. However when factors were combined, the data was able to give impactful information about the sustainability of restaurants in Toronto.  
