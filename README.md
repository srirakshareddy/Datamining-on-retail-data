# Datamining-on-retail-data

In this code I have conducted Machine Learning on Data Mining related to consumer segmentation using a provided retail dataset. Many retailers have found great value in using consumer segmentation algorithms to suggest products to users. To achieve this goal, I used the basket dataset from UCI and installed necessary APIs such as pandas. I have explored the use of Recency, Frequency and Monetary (R_F_M) analysis on the given retail dataset. The aim of this analysis is to identify the best customers quantitatively by analyzing recency, frequency, and monetary factors, which are based on the marketing axiom that "80% of your business comes from 20% of your customers." R_F_M analysis will be utilized to gain business intelligence on consumer segmentation by answering critical questions such as identifying the best customers, customers at the verge of churning, lost customers that require less attention, loyal customers, and customers who are most likely to respond to the current campaign. 

Additional information on R_F_M analysis metrics can be found in the following link: https://www.putler.com/rfm-analysis/

Dataset:
This is a transnational data set which contains all the transactions occurring
between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store
online retail. The data has 8 features namely, InvoiceNo, StockCode, Description,
Quantity, InvoiceDate, UnitPrice, CustomerID, and Country.
The dataset used in this assignment:
http://archive.ics.uci.edu/ml/datasets/Online+Retail.

Overview:
● First, we discard the cancelled orders and remove the data rows that do not
have a customer.
● Post this recency is calculated where we find the max date and calculate the
difference in days between the max date and other dates.
● We calculate the frequency by counting the number of times a certain
customer appears in a transaction.
● After calculating the frequency we calculate the total expenditure by
multiplying the unit price with quantity.
● Post this the monetary is calculated by summing up the total cost for
individual customers.
● We then combine frequency, recency and monetary in one table by their
customer ID
● Post this we declare quantiles and using that, we calculate R_Quartile,
F_Quartile and M_Quartile.
● Lastly, we combine them together to calculate the final RFM score.

Categories:
We divide customer segments in the following categories:
● Best customers -> RFM score = 444
● Loyal customers -> F_Quartile = 4
● Profitable customers -> M_Quartile = 4
● Verge of churning -> RFM score = 244
● Lost customers -> RFM score = 111
● Customers that must be retained -> RFM score = 444 or M_Quartile = 4
● Customers that are most likely respond to a current campaign -> RFM score
= 444 or F_Quartile = 4
