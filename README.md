# ADAN-ADEC7900 Group 2

# Introduction
### Research Question

Are healthy fruits and vegetables affordable to Americans in each state? We aimed to analyze the affordability of fruits and vegetables based on the average American household income by capita over multiple years. We hoped to investigate whether income constraints influence access to fresh produce versus alternative forms (i.e., canned/frozen) and how this impacts adherence to dietary guidelines. The findings could inform policymakers responsible for food pricing regulations and programs like food stamps, helping them understand the challenges individuals and families face in accessing nutritious foods and potentially guiding adjustments to policies or interventions aimed at improving dietary habits, particularly considering potential differences in affordability between fruits and vegetables. 


### Decision Maker

We planed to target our research for use by the Congressional Committees on Agriculture because they play a crucial role in shaping legislation and policies related to food and agriculture, including programs like the Supplemental Nutrition Assistance Program (SNAP) and other food assistance initiatives.

# Data Summary
**Provide a short description of the nature of the provided data set
and explain how these characteristics affect your analysis methodology. Summarize the
data set with basic descriptive statistics as applicable.**

The datasets included the average American household income per capita and fruits and vegetables prices from 2013, 2016, and 2020. These datasets allowed us to investigate our research questions regarding the affordability of fruits and vegetables based on the average American household income by capita over multiple years. See below for a more in-depth explanation of the variables included in each dataset.

### Included Data

| Data Sets  | 
| ------------- |
| Fruit Prices 2013.csv  | 
| Fruit Prices 2016.csv  | 
| Fruit Prices 2020.csv  | 
| Vegetable Prices 2013.csv  | 
| Vegetable Prices 2016.csv  | 
| Vegetable Prices 2020.csv  | 

| Columns included  | Description of columns |
| ------------- | ------------- |
| Fruit/Vegetable  | Type of food (apple, oranges, broccoli, etc)  |
| Form  | Form of food (fresh, canned, dried, juice, frozen)  |
| RetailPrice  | Price of food (in $)  |
| RetailPriceUnit  | Type of retail price (per pound, per unit, etc)  |
| Yield  | Preparation yield factor  |
| CupEquivalentSize  | A 1-cup equivalent equals the weight of enough edible food to fill a measuring cup  |
| CupEquivalentUnit  | Type of unit (pounds, fluid ounces)  |
| CupEquivalentPrice  | Price per edible cup equivalent (the unit of measurement for Federal recommendations for fruit and vegetable consumption) |
| Year  | Years included (2013, 2016, 2020)  |

| Data Sets  | 
| ------------- |
| Annual person income by county.csv  | 

| Columns included  | Description of columns |
| ------------- | ------------- |
| GeoFIPS  | Geo FIPS of United States states; increases by 1000 by state (01000 = Alabama, etc)  |
| GeoName  | Region and state, if no region present only state is listed  |
| Description  | Type of income; (Personal income (thousands of dollars), Population (persons) 1/, Per capita personal income (dollars) 2/	)  |
| 1Personal income (thousands of dollars)  | Consists of the income that persons receive in return for their provision of labor, land, and capital used in current production as well as other income, such as personal current transfer receipts. In the state and local personal income accounts the personal income of an area represents the income received by or on behalf of the persons residing in that area. It is calculated as the sum of wages and salaries, supplements to wages and salaries, proprietors' income with inventory valuation (IVA) and capital consumption adjustments (CCAdj), rental income of persons with capital consumption adjustment (CCAdj), personal dividend income, personal interest income, and personal current transfer receipts, less contributions for government social insurance plus the adjustment for residence.  |
| 2Population (persons)  | The number of individuals (both civilian and military) who reside in a given area.  |
| 3Per capita personal income (dollars)  | The personal income of a given area divided by the resident population of the area. See "personal income."  |
| Unit  | Type of variable; (Thousands of dollars, Number of persons, Dollars)  |
| 2013  | Price of unit type for 2013  |
| 2016  | Price of unit type for 2016  |
| 2020  | Price of unit type for 2020  |

### Descriptive Statistics
<img width="583" alt="Screenshot 2024-04-17 at 1 04 53 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/00ba954a-9ab7-4e49-a80b-726fe92ad951">
<img width="616" alt="Screenshot 2024-04-17 at 1 07 24 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/75d2f767-1187-4127-88ed-e3161f36ec1a">
<img width="579" alt="MeanPriceTrend" src="https://github.com/asteinkrauss/7900Group2/assets/164543699/cdb27460-1aee-4f48-937d-f0020cf46503">

Figure 1: Food Prices (2013-2020). For both fruits and vegetables, the mean cup equivalent price demonstrated a persistent upward trend from 2013 to 2020.

# Data Analytics
**Provide data analytics that add clarity to the research question.
Thoroughly discuss insight obtained from your visualizations and analysis of aggregated,
data. Suggest an excursion, and provide supporting analysis. Plots should be well
formatted according to best practices learned in class. Discuss the advantages and
challenges of performing analysis in your chosen software tool.**

### Analytical Tools & Methods 

We conducted our analyses in R. Using publicly available datasets spanning multiple years, we looked at descriptive statistics and looked at descriptive graphs (eg. bar, line, map graphs) to investigate the affordability of fruits and vegetables by state across time. Specifically, descriptive statistics investigated the average, minimum, and maximum prices of fruits and vegetables by year. The ‘ggplot2’ package was used to visualize the results, including interactive plots of fruit and vegetable prices, income per capita by state, and affordability of fruits and vegetables by state.

To quantify affordability, we developed an affordability metric based on the U.S. Department of Agriculture's recommended grocery budget of 11% of one's income (https://money.usnews.com/money/personal-finance/saving-and-budgeting/articles/how-much-should-i-spend-on-groceries). We then further subdivided the 11% and allocated 4% of one's income specifically for produce (so, 2% for fruits and 2% for vegetables). Since we're interested in affordability in relation to dietary guidelines, we calculated the price of a cup equivalent of fruits and vegetables (recommended daily serving; https://www.nidirect.gov.uk/articles/fruit-and-vegetables) for an entire year by multiplying the cup equivalent price by 365. Finally, to categorize a fruit or vegetable as affordable or unaffordable, we compared the yearly cup equivalent price (for fruit and vegetables separately) to 2% of per capita income by state. If the yearly cup equivalent price was greater than 2%, that fruit or vegetable was deemed unaffordable. If the yearly cup equivalent price was less than 2%, that fruit or vegetable was deemed affordable.

We aimed to discover important insights by examining trends in fruit and vegetable affordability by state. These insights could inform policymaking, with a particular focus on enhancing food assistance programs and regulations overseen by the Congressional Committees on Agriculture.

### Questions of Interest

**1. What are the most and least expensive fruits? How does this change across years?**
*Note: If you would like to see an interactive graph of the ones shown below, please download the .rmd file and run the appropriate code under "Question 1.".*

<img width="675" alt="Screenshot 2024-04-26 at 6 10 59 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/ab33b48c-2032-4547-9238-76887010d2c5">
<img width="676" alt="Screenshot 2024-04-26 at 6 11 11 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/d8c4dd11-bc33-45e9-bf17-d29ca13de59e">

<img width="673" alt="Screenshot 2024-04-26 at 6 11 23 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/c698f7ff-a47f-4972-9996-3d225c398f81">
<img width="673" alt="Screenshot 2024-04-26 at 6 11 34 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/1db8ee11-2561-439b-a23f-cbe1f4149d01">

<img width="674" alt="Screenshot 2024-04-26 at 6 11 46 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/3cc7fbef-4fd0-420a-bc13-ddf9c2186096">
<img width="678" alt="Screenshot 2024-04-26 at 6 11 59 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/fc6682fd-a262-4318-8121-02d5cd9ac267">


**Figure 1a-f.** Most and least expensive fruits in 2013, 2016, and 2020.

In examining the retail prices of fruits across the years 2013, 2016, and 2020, notable trends emerged in both the highest and lowest ends of the price spectrum. Fruits such as mangoes, figs, raspberries, and apricots consistently ranked amongst the most expensive fruits (when looking at per cup equivalent cost). These prices suggest enduring consumer preferences or supply chain dynamics that contributed to their elevated prices over time.

Conversely, fruits such as watermelon, bananas, and cantaloupe consistently ranked amongst the least expensive fruits (when looking at per cup equivalent cost). Of interest, frozen concentrate versions of fruit typically emerge as the least expensive options due to their cost-efficient production processes and longer shelf life, making them a budget-friendly alternative for consumers.

Though the types of fruits that were found to be most expensive or least expensive tended to remain consistent, the price of all of the fruits seemed to increase from 2013 to 2020.

**2. What are the most and least expensive vegetables? How does this change across years?**
*Note: If you would like to see an interactive graph of the ones shown below, please download the .rmd file and run the appropriate code under "Question 2.".*

<img width="672" alt="Screenshot 2024-04-28 154317" src="https://github.com/asteinkrauss/7900Group2/assets/164543699/13ae744e-3e70-402a-87d0-d7d76817ab8e">
<img width="675" alt="Screenshot 2024-04-26 at 6 08 03 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/0e860175-91f4-471c-8b45-ac6c79c8aa37">

<img width="677" alt="Screenshot 2024-04-26 at 6 08 22 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/13aff076-2c9b-488e-990c-be68510662c3">
<img width="677" alt="Screenshot 2024-04-26 at 6 08 37 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/84894665-ac5f-44b2-ae6b-31b8fc136ee3">

<img width="673" alt="Screenshot 2024-04-26 at 6 08 55 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/851f5c1a-3379-4e1d-a487-203aa14d6931">
<img width="673" alt="Screenshot 2024-04-26 at 6 09 08 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/d883dda1-0773-4cc6-a349-8b7c14e75bb0">

**Figure 2a-f.** Most and least expensive vegetables in 2013, 2016, and 2020.

In examining the retail prices of vegetables across the years 2013, 2016, and 2020, notable trends again emerged in both the highest and lowest ends of the price spectrum. Vegetables such as asparagus, olives, spinach, and mushrooms consistently ranked amongst the most expensive vegetables (when looking at per cup equivalent cost), reflecting their specialized cultivation requirements and often limited availability.

Conversely, vegetables such as potatoes, carrots, and various types of beans consistently ranked amongst the least expensive vegetables (when looking at per cup equivalent cost), owing to their widespread cultivation and high yield potential.

Similarly to fruits, the types of vegetables that were found to be most expensive or least expensive tended to remain constant, but the prices of all of the vegetables seemed to increase from 2013 to 2020.


**3. How does income per capita differ by state across years?**
*Note: If you would like to see an interactive graph of the ones shown below, please download the .rmd file and run the appropriate code under "Question 3.".*

<img width="658" alt="Screenshot 2024-04-26 at 6 09 52 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/3b08aad7-7fec-44d6-8ddf-d8ac00517276">
<img width="657" alt="Screenshot 2024-04-26 at 6 10 06 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/b752a1a2-bda7-4bfc-bf3b-d04ffb854ff9">
<img width="662" alt="Screenshot 2024-04-26 at 6 10 17 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/576aa2c2-9f42-4a1f-bb9c-a8c935b02218">

**Figure 3a-c.** Per capita income in 2013, 2016, 2020.

The series of heat maps were used to visually depict the variation in income per capita across the United States in 2013, 2016, and 2020. The maps offer a comprehensive overview of the economic landscape, illustrating how income levels fluctuate regionally and evolve over time. States such as Massachusetts and Connecticut consistently reported high income per capita (> $60,000) while New Mexico, Mississippi, and West Virginia consistently reported low income per capita (< $40,000). The majority of states reported income per capita between $45,000 and $55,000.

**4. How do the prices of different forms of fruits and vegetables change by year?**
*Note: If you would like to see an interactive graph of the ones shown below, please download the .rmd file and run the appropriate code under "Question 4.".*

<img width="665" alt="Screenshot 2024-04-29 at 1 39 54 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/514783e1-a7da-421c-8529-0f6f7cc9119c">

**Figure 4a.** Fruit prices by form.

In examining the average price (per cup equivalent) of fruit by form in 2013, 2016, and 2020, a noticeable upward trend in average price emerged. Of interest, juiced fruit was significantly cheaper than canned, dried, fresh, and frozen fruit.

<img width="664" alt="Screenshot 2024-04-29 at 1 40 11 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/dc990663-c2d4-40f5-881f-4a6722e3b8eb">

**Figure 4b.** Vegetable prices by form.

In examining the average price (per cup equivalent) of vegetables by form in 2013, 2016, and 2020, a noticeable upward trend in average price emerged. Of interest, dried vegetables were significantly cheaper than canned, fresh, and frozen vegetables.

**5. How many people can afford the recommended daily serving of fruits and vegetables across years?**

<img width="666" alt="Screenshot 2024-04-26 at 6 22 42 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/ea271b14-911c-46d1-bd23-15b0bf867fac">

**Figure 5.** Affordability of fruit and vegetable recommended daily serving.

The bar graph highlights a concerning trend regarding the affordability of meeting daily fruit and vegetable recommendations over time. This analysis is based on allocating 2% of per capita income by state for purchasing produce, with fruits and vegetables considered unaffordable if their yearly cup equivalent price exceeds this threshold, and affordable if it falls below. Regardless of the year, a significant disparity is evident in the proportion of individuals unable to afford the recommended daily servings of fruits and vegetables according to FDA guidelines. Moreover, there is a notable increase in the number of individuals facing affordability challenges for meeting their daily fruit and vegetable intake from 2013 to 2020.

**6. How does the affordability of fruits and vegetables differ amongst their different forms (Excursion Analysis)?**

<img width="666" alt="Screenshot 2024-04-29 at 1 42 26 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/d8da2103-a4ab-488c-9c30-d217529deb70">
<img width="667" alt="Screenshot 2024-04-29 at 1 42 43 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/e109e645-da83-4d4e-b580-57c196442953">

**Figure 6a.** Affordability of fruits by form of food. 
**Figure 6b.** Affordability of vegetables by form of food. 

The bar graphs depict the affordability of fruits and vegetables across various forms, aiming to highlight any disparities in accessibility. While the analysis initially examined each year individually (2013, 2016, and 2020), consistent trends emerged across years, leading to the decision to collapse the data for clarity. You can refer to the .rmd to see individual years. Each bar represents the count of affordable and unaffordable fruits or vegetables categorized by forms such as canned, dried, fresh, frozen, and juice. The y-axis scale is transformed using the square root to better visualize the distribution of counts, providing a more balanced representation of the data. This transformation helps mitigate the skewness often observed in count data, allowing for a clearer comparison of affordability among different fruits and vegetable forms. 

In Figure 6a, focusing on fruit forms, a notable disparity in affordability emerges, particularly for canned and fresh fruits appearing less accessible compared to dried, frozen, or juice forms. Similarly, in Figure 7a, which examines vegetable forms, fresh vegetables appear less accessible compared to other forms. Surprisingly, our data suggests that almost everyone could afford dried vegetables based on our affordability metric. We will note that looking more closely at our data, the dried form of vegetables include types of beans and lentils. Overall, for fruits and vegetables it seems that fresh forms of food is the least accessible option for individuals to buy. 

# Conclusion
**Summarize the analytical methodology and provide closure to your
analytical story. Succinctly answer the research questions. Highlight the limitations of
your findings and recommend future work. Do not make policy recommendations here.**

# Policy Recommendation
**Introduce a specific policy decision that your decision
maker is facing. Provide a data driven recommendation for their decision. Explain
probable first and second order effects of the recommendation. Explain the benefits and
risks of the recommendation.**
