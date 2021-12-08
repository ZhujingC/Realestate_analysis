# Project1_Realestate_Analysis
Property price analysis for Melbourne

# Material

Price Factor influencing property development and purchases (real estate) - melbourne
 
Questions in details

1.Do purchase price and sell number and rent number impact by bank interest rate (base on quartly data and bank interest rate, line chart) -Echo

2.Have purchases increased/decreased between 2019 - 2021 (quartly, median sell price, listing, sold) - Echo

3.The outliners of 2019-2021 in Highest sell price, median sold price (boxplot, maybe highlight the outliner) - Echo

4.In three different years, compare whole number of list and sold (use sum up value, bar chart) -therese

*5.What has caused the increase or decrease? (covid, loan interests, schools)

6.Does the median price of the rent has relationships with price of sold?(scatter plot, linear regression) - Anjali

7.Does the list of rent has relationships with price of sold?(scatter plot, linear regression) - Anjali

8.Does the quantity of the schools has anything do with the property price? Or just the quality of the schools? (heatmap of schools and heatmaps of price, heatmps of median price with markers of top ranking schools) - Rachel

9.What is the most popular suburb, does it appear to have relationship with locations of top ranking shcools? (heatmap-googlemap geo module, marker about school (government, private) - Rachel
 
# Hypothesis

 Covid Effect
1.Null Hypothesis - If there was no covid then the sales number and price of property would be high
2.Alternative Hypothesis - If there is covid the sales number and price of property would be low

 Bank Interests
1.Null Hypothesis - If the bank interests is drop and then the sell price of the property will go high
2.Alternative Hypothesis - If the bank interests is drop and then the rent of the property will go low

 School Ranking/Number of Schools
1.Null Hypothesis - If the school ranking is not high then sales the price of property  will be median
2.Alternative Hypothesis - If the school ranking is high then then sales the price of property  will be high

# Datasets

https://developer.domain.com.au
https://onproperty.com.au/free-sites-for-property-research/
https://developers.google.com/chart/interactive/docs/gallery/geochart
https://www.greatschools.org/api/
https://developer.domain.com.au
https://www.land.vic.gov.au/valuations/resources-and-reports/revaluation-2020-outcomes
https://www.rba.gov.au/chart-pack/interest-rates.html

Using the GET /v1/addressLocators and GET /v1/suburbPerformanceStatistics/ from Domain, to find the price as follow:

MedianSoldPrice, AuctionNumberAuctioned, AuctionNumberSold, AuctionNumberWithdrawn, NumberSold, LowestSoldPrice, HighestSoldPrice, 5thPercentileSoldPrice, 25thPercentileSoldPrice, 75thPercentileSoldPrice, 95thPercentileSoldPrice, DaysOnMarket, DiscountPercentage, MedianRentListingPrice, NumberRentListing, HighestRentListingPrice, LowestRentListingPrice, MedianSaleListingPrice, NumberSaleListing, HighestSaleListingPrice, LowestSaleListingPrice

![Screen Shot 2021-06-20 at 3 37 42 pm](https://user-images.githubusercontent.com/75764401/122663398-838d8680-d1dd-11eb-944a-75ec6944c2be.png)
Clean the dataset, and save to the main branch for everyone to use.

# Technical Requirements

Use Pandas to clean and format your data sets - (DOWN!)
Create a Jupyter Notebook describing the data exploration and cleanup process(https://github.com/22OVERSooN/Project1_Realestate_Analysis/blob/main/Acquire_data.ipynb) - (DOWN!)
Create a Jupyter Notebook illustrating the final data analysis - (DOWN!)
Use Matplotlib to create a total of 6-8 visualizations of your data (ideally, at least 2 per "question" you ask of your data) - (DOWN!)
Save PNG images of your visualizations to distribute to the class and instructional team, and for inclusion in your presentation(https://github.com/22OVERSooN/Project1_Realestate_Analysis/tree/main/Savefig） - (DOWN!)
Optionally, use at least one API, if you can find an API with data pertinent to your primary research questions （ Domain API and google API) - (DOWN!)

Summarizing major findings:

## Foundamental Analysis

Questions: How does property market change during 2019-2021?

Method: Use yearly and quarterly data and create line chart/scatter plot/bar plot to find if there is any changes on the property market.

Conclusions: If we only look at the yearly data there should not be much of the change, but base on what we here during the covid, the propery market should have a significant drop, so we dig a little deep to the quarterly data.

![Top 10 Median Sold Price - 2021](https://user-images.githubusercontent.com/75764401/123532242-ed161380-d74e-11eb-814f-45fce03abd55.png)

![Median Sell Price (2019-2021)](https://user-images.githubusercontent.com/75764401/123532245-f7381200-d74e-11eb-83c6-d5ee877d5194.png)

When we try to dig a little bit more on qurterly data, we will find that during the Jan_Mar 2020 and Sep_Oct 2020, there is significant drop during that period, so we try to use covid, bank interests and school ranking as an factor to figure out which element will triger the property change.

![Median Sell Price (2019-2021 Quarterly)](https://user-images.githubusercontent.com/75764401/123532282-3cf4da80-d74f-11eb-86e9-032040ae8ec8.png)
![Sold Price Increase Rate(2020-2021)](https://user-images.githubusercontent.com/75764401/123532286-454d1580-d74f-11eb-9281-86ca7c5fc446.png)

The correlation between Median Sold Price and Median Rent Price is 0.92, 0.91 and 0.89 for 2019, 2020 and 2021 respectively. Indicates a strong positive correlation.

![Median Price Sold Vs Median Rent Price](https://github.com/22OVERSooN/Project1_Realestate_Analysis/blob/34f9560dbc0f8074191dc3aafce4883df75dda23/Savefig/Median%20Sold%20Price%20vs.%20Median%20Rent%20Price(2019).png)
![Median Price Sold Vs Median Rent Price](https://github.com/22OVERSooN/Project1_Realestate_Analysis/blob/34f9560dbc0f8074191dc3aafce4883df75dda23/Savefig/Median%20Sold%20Price%20vs.%20Median%20Rent%20Price(2020).png) 
![Median Price Sold Vs Median Rent Price](https://github.com/22OVERSooN/Project1_Realestate_Analysis/blob/34f9560dbc0f8074191dc3aafce4883df75dda23/Savefig/Median%20Sold%20Price%20vs.%20Median%20Rent%20Price(2021).png)

The correlation between Median Sold Price and No of Rent Listing is -0.08, -0.09 and -0.08 for 2019, 2020 and 2021 respectively. Indicates a weak negative correlation

![Median Price Sold Vs No of Rent Listing](https://github.com/22OVERSooN/Project1_Realestate_Analysis/blob/34f9560dbc0f8074191dc3aafce4883df75dda23/Savefig/Median%20Sold%20Price%20vs.%20No%20of%20Rent%20Listing(2019).png)
![Median Price Sold Vs No of Rent Listing](https://github.com/22OVERSooN/Project1_Realestate_Analysis/blob/34f9560dbc0f8074191dc3aafce4883df75dda23/Savefig/Median%20Sold%20Price%20vs.%20No%20of%20Rent%20Listing(2020).png) 
![Median Price Sold Vs No of Rent Listing](https://github.com/22OVERSooN/Project1_Realestate_Analysis/blob/34f9560dbc0f8074191dc3aafce4883df75dda23/Savefig/Median%20Sold%20Price%20vs.%20No%20of%20Rent%20Listing(2021).png)

Method Use yearly data to compare from domain using pandas to see if there was a difference between number sold and list. Used a bar chart

conclusion:During the Comparison of list vs sold properties for 2019, 2020 & 2021
Number listed has far out weight the number sold
In saying that the number listed and sold have only increased marginally
Covid hasn’t really had an impact in number of sales as covid started late 2019 into 2020
While cash rate peaked in 2019 and decreased 2020 to 2021. The sold price increased and rent price  spiked in April and has now stayed consistent but have showed not major impact on sold and listed. Analysis of the quarterly data may reveal more insights



## Covid Impact

Questions: Does Covid_19 has any impact on realestate market?

Method: Use yearly and quarterly data and create scattor plot of increase of median sold price, median rent price and median listing price.

Conclusions: If we only look at the yearly data, there are not much of the changes happen, even we can see slightly increase, but once we dig a little bit more, the final results shows that during the covid, even the median of the median sell price has not been impacted, but the IQR and the 25th of the quartile have been impact, which means the property market does has some impact by Covid.
![The median sold price increase versus decrease - 2020 to 2021](https://user-images.githubusercontent.com/75764401/123532290-4ed67d80-d74f-11eb-99a5-777c14e5ef96.png)
![The median sold price increase versus decrease - 2019 to 2020](https://user-images.githubusercontent.com/75764401/123532291-50a04100-d74f-11eb-9fdb-6b23bbe964c2.png)


## Bank Interests Impact

Questions: Does Bank Cash Rate has any impact on realestate market?

Method: Use quarterly data and calculate the percentage of increase of median sold price, median rent price and numbers of listing rent/listing sold and actual sold.
Conclusions: The Covid trully has impact on property market and it impact immedieatly during Jan-Mar/2020 and Jul-Sep/2020, and the rent market basically has the same trend with sold market but the covid makes it goes in an opposite way, more people are likely to rent and not buy. Bank interests rate drop stimulate the property market and makes it increase eventually, but bank interests has laybacks.
![Cash Rate vs Sold Price Increase Rate Rend Price Increase Rate](https://user-images.githubusercontent.com/75764401/123532293-57c74f00-d74f-11eb-94da-3f9a9df3bb42.png)
![Cash Rate vs Average Sell Listing Rent Listing Sold](https://user-images.githubusercontent.com/75764401/123532294-59911280-d74f-11eb-8d0f-64578dbfb678.png)


# Schools analysis
Questions to answer:
1. Does number of schools (in a suburb) and rankings of schools impact on: 
--property sale price 
--property sale activities (number of houses sold in a suburb) 
2. Is there relationship between suburbs where the property get sold the most and suburbs where the top ranking schools locate.

Method: --Scatterplot to show case the relationship between the schools spread (locations) and the School count under each postcode --Scatterplot to show case the relationship between the schools spread (locations) and the house median sold price under each postcode --Gamps heatmap to indicate the median sale price among greater Melbourne regions --Gamps symbol to indicate suburbs which has the most houses sell activities --Gamps symbol to indicate suburbs which has the most houses sell activities --Gamps marker to indicate top ranking schools among greater Melbourne regions

Conclusions: 
![2021 Melbourne schools spread vs School count under under postcodes](https://user-images.githubusercontent.com/82508049/123543922-30df3c00-d794-11eb-8569-fcb8b650859e.png)
![2021 Melbourne schools vs MedianSold price for houses](https://user-images.githubusercontent.com/82508049/123543932-3ccafe00-d794-11eb-94e3-4e81b7495ac2.png)

From the scatter plots, we can see the median sale price is lower around the outer part of Melbourne region, and gradually increase towards the centre part of Melbourne . We can also see from the map that the majorities of the top ranking schools are located towards the centre part of the Melbourne. Hence we believe there is correlation between schools’ ranking and the property sale price. Where there are high ranking schools, the property sale price would be boosted. 

However, from the scatterplot the numbers of schools in a suburb does not appear to have a positive impact on suburbs, we can see from the plot, where there are the most schools, the suburbs have rather low median sale price. 

From the heatmap we can tell how the sale price spread cross the greater Melbourne region. On top of the heatmap, the symbol layer indicates the suburbs appear to have most sold properties. And the makers flag the top ranking schools. However, we can see there is not much overlapping between the suburbs has most sale activities and the suburbs has highest ranking schools. Saying that, it might also due to the fact that majorities of top ranking schools are located in the area that too expensive to purchase, and people opt to rent instead. However, to determine that, we need to analyse further and combine other factors as well.
![map (2)](https://user-images.githubusercontent.com/82508049/123532263-19319480-d74f-11eb-82bd-fe5a6dd00088.png)




