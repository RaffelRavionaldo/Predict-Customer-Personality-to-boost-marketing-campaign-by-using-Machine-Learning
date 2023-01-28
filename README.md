# Predict-Customer-Personality-to-boost-marketing-campaign-by-using-Machine-Learning

## overview

“ A company can develop rapidly when it knows the behavior of it’s customer personality, so that it can provide better services and benefits to customers who have the potential to become loyal customers. By processing historical marketing campaign data to improve performance and target the right customers, so they can transcat on the company’s platform, from this data insight our focus is to create a cluster prediction model to make it easir for companies to make decisions.

## Exploratory Data Analysis

### Total Accepted Campaign Analysis

![image](https://user-images.githubusercontent.com/94748637/215256714-984e8406-a8ed-4e79-ad68-f1cdd92e5ac5.png)

Correlation between numeric column and total accepted campaign, we will analyst it only top 5 column, there are : 'Total_amount', 'Response', 'Income', 'Total_Purchases','total_children’

For categories column, we analyst just one column, there are grup_age because it have a lowest p-value at chi-square test between another categories column

![image](https://user-images.githubusercontent.com/94748637/215256729-dd92b5df-e898-4599-93e2-99369da8ad34.png)

From picture above, we can see that the higher total amount and income, then the higher number of total accepted campaign received and if the consumer have more children, then total_accepted_campaign will be lower.

![image](https://user-images.githubusercontent.com/94748637/215256749-f04105f8-0191-4821-8f89-5f4da1e4907b.png)

From picture above, if customer have response our current campaign, the number of total_accepted_campaign will be higher, in total purchases, the higher puchases that the customer do, the higher number of total_accepted_campaign. And we can see Young adult have a tendency to accept the campaign that we provide.

### Conversion Rate Analysis

![image](https://user-images.githubusercontent.com/94748637/215256808-4dad30ba-9444-4d81-b16b-144b2a834e4a.png)

From picture above, we can see at total amount and income have a low positive correlation with cvr, at total children, if the customer have fewer children, the value of cvr will be higher.

![image](https://user-images.githubusercontent.com/94748637/215256824-1c8472ee-78dc-4a81-b186-555a1bf3b277.png)

From picture above, the distribution of data in the response column looks quite even, and at total purchase have a low positive correlation with cvr.

## Data Preprocessing

![image](https://user-images.githubusercontent.com/94748637/215256867-42623f1d-a79f-41de-8718-b466a5ef920b.png)

![image](https://user-images.githubusercontent.com/94748637/215256878-d47cde77-c9b7-49f8-855d-0feac05d4966.png)

![image](https://user-images.githubusercontent.com/94748637/215256890-4961decb-86b2-41ab-bda1-58ec8dd96827.png)

![image](https://user-images.githubusercontent.com/94748637/215256908-f72097ec-85c4-411a-8577-b7a3cda08cbf.png)

![image](https://user-images.githubusercontent.com/94748637/215256913-89fb9967-0d58-43c4-9093-c048e0c912e8.png)


## Modelling K-Means

For segmenting customer, there is a method called RFM Analysis, for you want to know deeply about RFM can read this reference
https://www.barilliance.com/rfm-analysis/#:~:text=RFM%20analysis%20is%20a%20data,much%20they've%20spent%20overall.

![image](https://user-images.githubusercontent.com/94748637/215256927-f9105917-d8e9-4237-8335-590ae2a0da8b.png)

### Elbow Score

![image](https://user-images.githubusercontent.com/94748637/215256931-72357e29-da18-4476-b214-d7f0ccf6871e.png)

### Silhouette Score

![image](https://user-images.githubusercontent.com/94748637/215256957-57d383fe-ce9a-4afc-bfbc-15aa27906276.png)

### Modelling Result

![image](https://user-images.githubusercontent.com/94748637/215256975-43a2920d-ba75-4d97-baaf-b69bd67df3fc.png)

1. High Valued Customer
Customers on this group have low average recency (21 days), high average total purchase (22 times) and high average total amount (1,23 Million Rupiah).
There 18,44 % of our customer fall into this category.
There are 236 customer never accept our campaign, 107 accepted it once, 42 accepted it twice, 20 accepted it three times and 6 accepted it four times.

2. Medium Valued Customer
Customers on this group have high average recency (71 days), high average total purchase (22 times) and high average total amount (1,18 Million Rupiah).
There 24.09 % of our customer fall into this category.
There are 354 customer never accept our campaign, 116 accepted it once, 38 accepted it twice, 24 accepted it th

3. Low Valued Customer
Customers on this group have low average recency (23 days), low average total purchase (10 times) and low average total amount (172K Rupiah).
There 29.03 % of our customer fall into this category.
There are 590 customer never accept our campaign, 54 accepted it once and 3 accepted it twice.

4. Very Low Valued Customer
Customers on this group have high average recency (73 days), low average total purchase (10 times) and low average total amount (151K Rupiah).
There 28,44 % of our customer fall into this category.
There are 587 customer never accept our campaign and 47 accepted it once.

### Potential Impact

If we keep prioritize on customer cluster and they have similar character like in our data, we still have potential GMV Rp 1.34 Billion with details :

High Value Customer : Rp 506 Million
Medium Value Customer : Rp 365 Million
Low Value Customer : Rp 111 Million
Very Low Value Customer : Rp 95 Million

## Business Recommendation

1. Make a membership (Platinum, Gold, Silver and Bronze) depends on customer cluster, Promote the benefits of being a platinum such as have a more discount to increase our GMV.
2. To Decrease a total customer at Very low and low value customer, we can inform them about our limited discount product and make cheap packages (like buy 1 milk get 1 instant noodle free)  since they have a lowest total amount at our shop.
3. To keep our medium and high value customer, we can give them ‘special treatment’ like giving bonuses and gift.
