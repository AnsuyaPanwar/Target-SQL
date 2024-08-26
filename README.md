# Target-SQL
## Context:
Target is a globally renowned brand and a prominent retailer in the United States. Target makes itself a preferred shopping destination by offering outstanding value, inspiration, innovation and an exceptional guest experience that no other retailer can deliver.
This particular business case focuses on the operations of Target in Brazil and provides insightful information about 100,000 orders placed between 2016 and 2018.The dataset offers a comprehensive view of various dimensions including the order status, price, payment and freight performance, customer location, product attributes, and customer reviews.
## Problem Statement
Assuming you are a data analyst/ scientist at Target, you have been assigned the task of analyzing the given dataset to extract valuable insights and provide actionable recommendations.

### 1. ASK
## Questions:
* Data type of all columns in the "customers" table. Get the time range between which the orders were placed.
* Count the Cities & States of customers who ordered during the given period.
* Is there a growing trend in the no. of orders placed over the past years?
* Can we see some kind of monthly seasonality in terms of the no. of orders being placed?
* During what time of the day, do the Brazilian customers mostly place their orders? (Dawn, Morning, Afternoon or Night)
* Get the month on month no. of orders placed in each state.
* How are the customers distributed across all the states?
* Get the % increase in the cost of orders from year 2017 to 2018 (include months between Jan to Aug only).
* You can use the "payment_value" column in the payments table to get the cost of orders.
* Calculate the Total & Average value of order price for each state.
* Calculate the Total & Average value of order freight for each state.
* Find the no. of days taken to deliver each order from the order’s purchase date as delivery time.Also, calculate the difference (in days) between the estimated & actual delivery date of an order.Do this in a single query.
* Find out the top 5 states with the highest & lowest average freight value.
* Find out the top 5 states with the highest & lowest average delivery time.
* Find out the top 5 states where the order delivery is really fast as compared to the estimated date of delivery.You can use the difference between the averages of actual & estimated delivery date to figure out how fast the delivery was for each state.
* Find the month on month no. of orders placed using different payment types.
* Find the no. of orders placed on the basis of the payment installments that have been paid.

## 2. PREPARE
### Data Storage:
The public dataset is completely available on the google drive platform where it stores and consolidates all available datasets for analysis. The specific individual datasets at hand can be obtained at this link below: https://drive.google.com/drive/folders/1TGEc66YKbD443nslRi1bWgVd238gJCnb

## 3. PROCESS
## Tools Used:
1. My SQL
2. Big Query
## Data Used: 
customers.csv,sellers.csv,order_items.csv,geolocation.csv,payments.csv,reviews.csv,orders.csv,products.csv
## About Data:
This file provides a comprehensive overview of the tables found in the dataset. It includes information for eight main tables:
1. customers.csv:  contains customer-related data
2. sellers.csv: contains sellers-related data
3. order_items.csc: contains order_items-related data
4. geolocation.csv: contains geolocation-related data
5. payments.csv: contains payments-related data
6. reviews.csv: contains geolocation-related data for each products
7. orders.csv: contains orders-related data
8. products.csv: contains products-related data

### Column Description for customers table:

The customers.csv contain following features:

1 . customer_id :ID of the consumer who made the purchase

2 . customer_unique_id :Unique ID of the consumer

3 . customer_zip_code_prefix :Zip Code of consumer’s location

4 . customer_city :Name of the City from where order is made

5 . customer_state :State Code from where order is made (Eg. são paulo - SP)

### Column Description for sellers table:
The sellers.csv contains following features:

1 . seller_id :Unique ID of the seller registered

2 . seller_zip_code_prefix :Zip Code of the seller’s location

3 . seller_city :Name of the City of the seller

4 . seller_state :State Code (Eg. são paulo - SP)

### Column Description for order_items table:
The order_items.csv contain following features:


1 . order_id : A Unique ID of order made by the consumers

2 . order_item_id : A Unique ID given to each item ordered in the order

3 . product_id : A Unique ID given to each product available on the site

4 . seller_id : Unique ID of the seller registered in Target

5 . shipping_limit_date : The date before which the ordered product must be shipped

6 . price : Actual price of the products ordered

7 . freight_value : Price rate at which a product is delivered from one point to another

### Column Description for order_items table:
The geolocations.csv contain following features:

1 . geolocation_zip_code_prefix : First 5 digits of Zip Code

2 . geolocation_lat : Latitude

3 . geolocation_lng : Longitude

4 . geolocation_city : City

5 . geolocation_state : State

### Column Description for payments table:
The payments.csv contain following features:

1 . order_id : A Unique ID of order made by the consumers

2 . payment_sequential : Sequences of the payments made in case of EMI

3 . payment_type : Mode of payment used (Eg. Credit Card)

4 . payment_installments : Number of installments in case of EMI purchase

5 . payment_value : Total amount paid for the purchase order

### Column Description for orders table:
The orders.csv contain following features:

1 . order_id : A Unique ID of order made by the consumers

2 . customer_id : ID of the consumer who made the purchase

3 . order_status : Status of the order made i.e. delivered, shipped, etc.

4 . order_purchase_timestamp : Timestamp of the purchase

5 . order_delivered_carrier_date : Delivery date at which carrier made the delivery

6 . order_delivered_customer_date : Date at which customer got the product

7 . order_estimated_delivery_date : Estimated delivery date of the products

### Column Description for reviews table:
The reviews.csv contain following features:

1 . review_id : ID of the review given on the product ordered by the order id

2 . order_id : A Unique ID of order made by the consumers

3 . review_score : Review score given by the customer for each order on a scale of 1-5

4 . review_comment_title : Title of the review

5 . review_comment_message : Review comments posted by the consumer for each order

6 .review_creation_date : Timestamp of the review when it is created

7 . review_answer_timestamp : Timestamp of the review answered

### Column Description for products table:
The products.csv contain following features:


1 . product_id : A Unique identifier for the proposed project.

2 . product_category_name : Name of the product category

3 . product_name_lenght : Length of the string which specifies the name given to the products ordered

4 . product_description_lenght : Length of the description written for each product ordered on the site

5 . product_photos_qty : Number of photos of each product ordered available on the shopping portal

6 . product_weight_g : Weight of the products ordered in grams

7 . product_length_cm : Length of the products ordered in centimeters

8 . product_height_cm : Height of the products ordered in centimeters

9 . product_width_cm : Width of the product ordered in centimeters






















