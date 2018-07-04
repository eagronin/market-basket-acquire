# Data Acquisition

## Overview
This section describes the data from a UK-based online retailer which are used in the subsequent sections to discover co-occurrence relationships among customers’ purchase activities. This analysis is called market basket analysis or association analysis.  It is commonly used in marketing to increase the chance of cross-selling, provide recommendations to customers based, for example, on their browsing history and deliver targeted marketing (e.g., offer coupons to customers for products that are frequently purchased together with items that the customers recently bought).

Data exploration and cleaning are discussed in the [next section](https://eagronin.github.io/market-basket-prepare/).

The analysis for this project was performed in R.

## Description of the Online Retail Dataset
The dataset was downloaded from [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/online+retail).  It is a transactional data set that contains 541909 purchases representing all the transactions that occured between December 1, 2010 and December 9, 2011 for a UK-based online retailer.  The customers of this online retailer are mainly wholesalers.  The retailer mainly sells unique all-occasion gifts.

As reported on the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/online+retail) website, the attributes information is as follows:

Attribute Name | Description
| --- | --- |
InvoiceNo| Invoice number. Nominal, a 6-digit integral number uniquely assigned to each transaction. If this code starts with letter 'c', it indicates a cancellation. 
StockCode| Product (item) code. Nominal, a 5-digit integral number uniquely assigned to each distinct product. 
Description| Product (item) name. Nominal. 
Quantity| The quantities of each product (item) per transaction. Numeric.	
InvoiceDate| Invice Date and time. Numeric, the day and time when each transaction was generated. 
UnitPrice| Unit price. Numeric, Product price per unit in sterling. 
CustomerID| Customer number. Nominal, a 5-digit integral number uniquely assigned to each customer. 
Country| Country name. Nominal, the name of the country where each customer resides.

The code below imports the data:

```R
setwd("/Users/eagronin/Documents/Data Science/Association Analysis")
rm(list = ls())

# read retail data item by item and create additional features
items = read.csv("Online Retail.csv", header = TRUE, sep = ",")
```

Next step: [Data Preparation](https://eagronin.github.io/market-basket-prepare/)
