# Market Basket Analysis using Apriori Algorithm

This project performs Market Basket Analysis on e-commerce transaction records to discover frequent itemsets and generate association rules that reveal which products are frequently purchased together.

## Project Overview
* Dataset: Online Retail dataset (Online Retail.xlsx) containing 541,909 transactions across 38 countries, filtered specifically to analyze 9,495 transactions from Germany (603 unique invoices across 1,703 products).
* Data Preparation:
  * Filtered records by country (Germany) and checked for missing values.
  * Constructed a transaction-product pivot table mapping InvoiceNo to item Description quantities.
  * Applied one-hot encoding (0/1 binary matrix) to represent item presence per invoice.
* Association Rule Mining:
  * Extracted 497 frequent itemsets using the Apriori algorithm with a minimum support threshold of 0.02 (2%).
  * Generated 919 association rules evaluated by support, confidence (minimum threshold 0.05), and lift metrics.
  * Exported the resulting antecedents and consequents table to best_anticedents_consequents_germany.csv.

## Tools Used
* Language: Python
* Libraries: Pandas, MLxtend (apriori, association_rules), OpenPyXL

