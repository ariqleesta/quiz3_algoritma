The data we're going to use is the invoice summary of a transaction data of an online retail shop provided from UCI Machine Learning [repository](https://archive.ics.uci.edu/ml/datasets/online+retail). All the transactions occurring between end of 2010 to end of 2011 for a UK-based and registered non-store online retail. We have provided the data, so you don't have to re-download it.

Before you go any further, check the data `dtypes` and make sure all of our columns have stored in the correct data type!

Create a barchart which compares the **total** revenue (`TotalPrice`) from international markets (all countries except UK).

*Hint*:
- You may start by creating a new dataframe which stores all the invoices data from all countries except UK (`invoice.Country != 'United Kingdom'`).
- Perform a group by aggregation to get the total(`sum`) revenue (`TotalPrice`) by each country
- Pair the dataframe with `.plot(kind=bar)` to get the barchart!

1. Take a look at the `x` axis of your plot. Does the `Country` arranged by its alphabetical order or based on its revenue (`TotalPrice` value)? Which order do you think suits our plot the most and how to achieve it?
    - [ ] by alphabetical order: `df.sort_values('Country', ascending = False).plot(kind='bar')`
    - [ ] by alphabetical order: `df.plot(kind='bar', ascending = False)`
    - [ ] by revenue: `df.sort_values('TotalPrice', ascending=False).plot(kind='bar')`
    - [ ] by revenue: `df.plot(kind='bar', ascending = False)` 
    

2. Which of the following are **not** among the top 5 largest market by revenue (has highest `Total Price`)?
    - [ ] Netherland
    - [ ] EIRE
    - [ ] Germany
    - [ ] Spain

**Note: Save the data that exclue UK country as new `DataFrame` named `invoice_int`**

A common way to statistically inspecting a data is using box plot, a handy visualization tools that provide a five number summary for your data.

Say, we want to create a boxplot that shows different distribution shape for each monthly revenue within each country by the following code: 

```python
invoice_int['InvoiceMonth'] = invoice_int['InvoiceDate'].____

invoice_monthly = invoice_int.\
groupby(____).\
agg({'TotalPrice': 'sum'})

invoice_monthly.\
boxplot(column = ____, by=____)
```

3. Select the right answer to complete above code to create the desired boxplot:
 - [ ] `.dt.month()`, `['Country', 'InvoiceMonth']`, `TotalPrice`, `InvoiceMonth`
 - [ ] `.dt.to_period('M')`, `['Country', 'InvoiceMonth']`, `TotalPrice`, `InvoiceMonth`
 - [ ] `.dt.month()`, `InvoiceMonth`, `TotalPrice`, `InvoiceMonth`
 - [ ] `.dt.to_period('M')`, `InvoiceMonth`, `InvoiceMonth`, `TotalPrice`

**You need to answer this correctly in order to answer question 4 and 5**

From the previous box plot (question 3), pay attention on month June 2011. We've captured several outliers above our top whisker line. Now, try to subset the outlier by completing code below.

```python
invoice_june = invoice_monthly.xs(key = ___ ,  level= ___ )

invoice_june[invoice_june['TotalPrice'] > ___ ]

```
4. Select the right answer to fill the code:
- [ ] `2011-06`, 0, 13000
- [ ] `2011-06`,`InvoiceMonth`, 24000
- [ ] `2011-06`, 1, 13000
- [ ] `2011-06`, `InvoiceMonth`, 24000


5. Which countries are **NOT** among the outliers shown by the result above?
- [ ] Germany
- [ ] France
- [ ] Australia
- [ ] EIRE