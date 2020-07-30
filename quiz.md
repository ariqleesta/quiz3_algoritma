# Graded Assignment

**To answer the question below, refer to all the tasks listed in `3. Quiz_Data_Wrangling_and_Visualization.ipynb`**

## Task 1
1. When creating a bar chart, we should also consider what order in which we will plot the bars. Sorting the bars by the right order reduce the burden on the reader to make the comparisons. What ordering do you think the bars within the *Task 1* barchart should be presented?
    - [ ] by Country: `sort_values('Country', ascending = False).plot(kind='bar')`
    - [ ] by Country: `sort_values('Country').plot(kind='barh')`
    - [ ] by Value: `sort_values('TotalPrice', ascending=False).plot(kind='bar')`
    - [ ] by Value: `sort_values('TotalPrice').plot()` 

2. From the chart you just created in *Task 1*, which of the following is **not** among the top 5 largest market outside the United Kingdom?
    - [ ] Netherland
    - [ ] EIRE
    - [ ] Germany
    - [ ] Spain
    
## Task 2
3. From the boxplot shown in *Task 2*, which of the following statements is **TRUE**?
    - [ ] The highest market revenue in January 2011 was around 18,000 USD
    - [ ] In 2011, the total monthly revenue in February was higher than March
    - [ ] The median revenue appeared to be highest in May 2011.
    - [ ] In 2011, there were more countries that happen to be outliers in April than June.
    
4. Which one of the following is the correct code to fill in the blank codes in *Task 2*:
   - [ ] `['Country']`, `'TotalPrice'`, `'Country'`
   - [ ] `['InvoiceMonth']`, `'TotalPrice'`, `'InvoiceMonth'`
   - [ ] `['Country','InvoiceMonth']`, `'TotalPrice'`, `'InvoiceMonth'`
   - [ ] `['InvoiceMonth','Country']`, `'InvoiceMonth'`, `'TotalPrice'`

## Task 3
5. Which countries are **NOT** included in `june_outliers` table/dataframe?
   - [ ] Germany
   - [ ] France
   - [ ] Australia
   - [ ] EIRE

6. Which of the following code shows the *most efficient* **grouped bar chart** to compare **quarterly revenue growth** in `invoice_topq`?    
    - [ ] `invoice_topq.plot(kind='bar')`
    - [ ] `invoice_topq.unstack().plot(kind = 'bar',stacked=True)`
    - [ ] `invoice_topq.unstack(level = 'Country').plot(kind='barh')`
    - [ ] `invoice_topq.unstack(level = 'Country').plot(kind='bar')`