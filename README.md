# Elo Merchant Category Recommendaton (ongoing...)

Elo, an Brazilian paymenet company, helps mechants to promote their business to card holders with promotions and discounts. 
How did card holders respond to these promotions ?  The competition is to set up machine learning mdoels to predict how customers would repond to promotions (with "loyalty numerical score" as prediction "target").  "loyalty numerical score" appears to be normalized with normal distribution with the mean near zero.   
  
![alt text](https://github.com/Jun-depo/Merchant-Category-Recommendaton/blob/master/target.png)

### The data

The data contain several tables:
(1) training.csv, 
(2) testing.csv, 
(3) historical_transactions.csv, 
(4) new_merchant_transactions.csv, 
(5)merchants.csv.  

### Features: 
(1) training.csv, testing.csv contains informations about card holder and "target" (only in training.csv, unknown in testing.csv). 
(2) "historical_transactions.csv" contains transaction data up to "2018-02", linking card holders and mercahnts in transactions, also includes (a) "purchase_amount", (b) "installment" (payment installment),(c) "month_lag" (transaction time relative to 2018-02),  (d) "category_1", (e) "category_2", (f)  "category_3" and other features. 

### Basic model (neural network)

The basic model only contains some of features.  Other features will be added into the model in the future.  The following screenshot shows the features used in the model.   
![alt text](https://github.com/Jun-depo/Merchant-Category-Recommendaton/blob/master/basic_features.png)

The basic model has RMSE score at 3.941 (The leader has it at 3.637, smaller is better). 

### Adding more features (ongoing...)

Transactions for each card ("card_id") contains amounts, time and merchants.  More recent transactions are likely to be more informative for predictions than transactions happened long time ago.  Also, if transactions occurs at good/bad merchants would also affect card holder attitude towards the future promotions/discounts.  I will reorganize the data as shown in the following diagram.  


