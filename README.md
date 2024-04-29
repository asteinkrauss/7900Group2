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
<!--
-- INSERT DESCRIPTION ABOUT MOST/LEAST EXPENSIVE FRUIT 2013 HERE --
<img width="675" alt="Screenshot 2024-04-26 at 6 10 59 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/ab33b48c-2032-4547-9238-76887010d2c5">
<img width="676" alt="Screenshot 2024-04-26 at 6 11 11 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/d8c4dd11-bc33-45e9-bf17-d29ca13de59e">

-- INSERT DESCRIPTION ABOUT MOST/LEAST EXPENSIVE FRUIT 2016 HERE --
<img width="673" alt="Screenshot 2024-04-26 at 6 11 23 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/c698f7ff-a47f-4972-9996-3d225c398f81">
<img width="673" alt="Screenshot 2024-04-26 at 6 11 34 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/1db8ee11-2561-439b-a23f-cbe1f4149d01">

-- INSERT DESCRIPTION ABOUT MOST/LEAST EXPENSIVE FRUIT 2020 HERE --
<img width="674" alt="Screenshot 2024-04-26 at 6 11 46 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/3cc7fbef-4fd0-420a-bc13-ddf9c2186096">
<img width="678" alt="Screenshot 2024-04-26 at 6 11 59 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/fc6682fd-a262-4318-8121-02d5cd9ac267">
-->
<img width="674" alt="Screenshot 2024-04-28 175111" src="https://github.com/asteinkrauss/7900Group2/assets/164543699/767f7317-506f-4377-833f-2ad82e5fd75a">
<img width="674" alt="Screenshot 2024-04-28 175118" src="https://github.com/asteinkrauss/7900Group2/assets/164543699/38fb10fb-b24c-4d15-9143-54e859a7431a">


The analysis of fruit cup equivalent prices from 2013 to 2020 reveals a consistent upward trend, with some exceptions. Most fruits, as illustrated by the top 5 most and least expensive, experienced price increases, reflecting broader economic factors. While occasional stability or even decreases were observed in a few items, they were relatively rare compared to the overall pattern of price increases. The COVID-19 pandemic likely exacerbated this trend due to supply chain disruptions and increased production costs. 

Understanding these dynamics is crucial for stakeholders, as rising fruit prices can challenge affordability and accessibility, especially for vulnerable populations. Addressing these underlying factors is essential for mitigating the impact on consumers and overall affordability of living.

**2. What are the most and least expensive vegetables? How does this change across years?**
*Note: If you would like to see an interactive graph of the ones shown below, please download the .rmd file and run the appropriate code under "Question 2.".*

<img width="674" alt="Screenshot 2024-04-28 175240" src="https://github.com/asteinkrauss/7900Group2/assets/164543699/3f3bc9d5-3892-4a64-b6bc-80d236151aff">
<img width="674" alt="Screenshot 2024-04-28 175247" src="https://github.com/asteinkrauss/7900Group2/assets/164543699/6959c1b6-d947-4a10-9336-4c394984bb73">

Vegetable cup equivalent prices from 2013 to 2020 also reveal a consistent upward trend, akin to observations in the fruit market. Most vegetables showed a consistent rise in prices over this period. While occasional stability or decreases were observed, they were rare compared to the overall trend of price increases.

These rising prices align with broader economic factors, with the COVID-19 pandemic likely accelerating inflationary pressures. Supply chain disruptions and increased production costs associated with the pandemic contributed to this trend. Addressing the underlying factors driving these price movements is essential for mitigating their impact and ensuring the affordability of vegetables for all consumers.

<!--
-- INSERT DESCRIPTION ABOUT MOST/LEAST EXPENSIVE VEGETABLES 2013 HERE --
<img width="672" alt="Screenshot 2024-04-28 154317" src="https://github.com/asteinkrauss/7900Group2/assets/164543699/13ae744e-3e70-402a-87d0-d7d76817ab8e">
<img width="675" alt="Screenshot 2024-04-26 at 6 08 03 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/0e860175-91f4-471c-8b45-ac6c79c8aa37">


-- INSERT DESCRIPTION ABOUT MOST/LEAST EXPENSIVE VEGETABLES 2016 HERE --
<img width="677" alt="Screenshot 2024-04-26 at 6 08 22 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/13aff076-2c9b-488e-990c-be68510662c3">
<img width="677" alt="Screenshot 2024-04-26 at 6 08 37 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/84894665-ac5f-44b2-ae6b-31b8fc136ee3">

-- INSERT DESCRIPTION ABOUT MOST/LEAST EXPENSIVE VEGETABLES 2020 HERE --
<img width="673" alt="Screenshot 2024-04-26 at 6 08 55 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/851f5c1a-3379-4e1d-a487-203aa14d6931">
<img width="673" alt="Screenshot 2024-04-26 at 6 09 08 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/d883dda1-0773-4cc6-a349-8b7c14e75bb0">

-- INSERT CONCLUSION HERE --

-->

**3. How does income per capita differ by state across years?**
*Note: If you would like to see an interactive graph of the ones shown below, please download the .rmd file and run the appropriate code under "Question 3.".*

<img width="658" alt="Screenshot 2024-04-26 at 6 09 35 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/da6c3304-94cd-42e4-b7f3-14c42a906f04">
<img width="658" alt="Screenshot 2024-04-26 at 6 09 52 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/3b08aad7-7fec-44d6-8ddf-d8ac00517276">
<img width="657" alt="Screenshot 2024-04-26 at 6 10 06 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/b752a1a2-bda7-4bfc-bf3b-d04ffb854ff9">
<img width="662" alt="Screenshot 2024-04-26 at 6 10 17 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/576aa2c2-9f42-4a1f-bb9c-a8c935b02218">
<img width="661" alt="Screenshot 2024-04-28 194417" src="https://github.com/asteinkrauss/7900Group2/assets/164543699/f6312bc1-3cd6-4f3b-8ac1-007f86933c99">


The wage growth and income analysis spanning from 2013 to 2020 reveals a systemic affordability crisis across various states. While nominal wages increased in many regions, a significant portion of states faced challenges in maintaining real wage growth above the inflation rate.

Some states, including Alaska, Iowa, Kansas, Louisiana, North Dakota, and Oklahoma, struggled as their wage growth rates fell below the cumulative inflation rate. This indicates a concerning trend where residents experienced a decline in purchasing power, exacerbating challenges in meeting basic needs, including affording food.

Conversely, another group of states managed to keep pace with or slightly exceed inflation. However, their wage growth still underscores the widespread nature of the affordability crisis, with many residents grappling with increasing living costs, including the cost of putting food on the table.

This systemic issue not only affects individual households but also has broader implications for economic stability and social well-being. Addressing this crisis requires comprehensive solutions that address underlying economic disparities and structural barriers.

**4. How do the prices of different forms of fruits and vegetables change by year?**
*Note: If you would like to see an interactive graph of the ones shown below, please download the .rmd file and run the appropriate code under "Question 4.".*

-- INSERT DECRIPTION OF FRUIT PRICE BY FORM --
<img width="666" alt="Screenshot 2024-04-17 at 7 23 30 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/622a70d9-f753-43b5-8594-bbfb4b945933">

-- INSERT DESCRIPTION OF VEGETABLE PRICE BY FORM --
<img width="667" alt="Screenshot 2024-04-17 at 7 23 45 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/4a886ee0-f322-4120-aa89-05d9a83aed59">

-- INSERT CONCLUSION HERE --

**5. How many people can afford the recommended daily serving of fruits and vegetables across years?**

<img width="666" alt="Screenshot 2024-04-26 at 6 22 42 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/ea271b14-911c-46d1-bd23-15b0bf867fac">

-- INSERT CONCLUSION HERE --

**6. EXCURSION ANALYSIS -- How does the affordability of fruits and vegetables differ amongst their different forms?**

-- INSERT DESCRIPTION OF FRUIT AFFORDABILITY BY FORM HERE (HELPFUL TO SAY SOMETHING ABOUT THE UTILITY OF THE SQUARE ROOT SCALE) --
<img width="664" alt="Screenshot 2024-04-27 at 9 42 57 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/1370beb0-4215-4087-af07-bcb4343eb80e">
<img width="664" alt="Screenshot 2024-04-27 at 9 43 13 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/097d1684-cd74-4eb8-9a25-e065bb01205e">
<img width="663" alt="Screenshot 2024-04-27 at 9 43 33 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/b740b2a0-72db-4e5f-b10e-929a18dff6e8">


-- INSERT DESCRIPTION OF VEGETABLE AFFORDABILITY BY FORM HERE (HELPFUL TO SAY SOMETHING ABOUT THE UTILITY OF THE SQUARE ROOT SCALE) --
<img width="665" alt="Screenshot 2024-04-27 at 9 43 48 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/11dc065c-2494-42ba-aeba-8d9c10898194">
<img width="667" alt="Screenshot 2024-04-27 at 9 44 00 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/a089fe4e-9c7c-4008-ba0f-9ac170c4552d">
<img width="666" alt="Screenshot 2024-04-27 at 9 44 17 PM" src="https://github.com/asteinkrauss/7900Group2/assets/164549275/1bee9e67-7ae9-4056-8b87-1e4a602f4d42">


-- INSET CONCLUSION HERE --

# Conclusion
**Summarize the analytical methodology and provide closure to your
analytical story. Succinctly answer the research questions. Highlight the limitations of
your findings and recommend future work. Do not make policy recommendations here.**

# Policy Recommendation
**Introduce a specific policy decision that your decision
maker is facing. Provide a data driven recommendation for their decision. Explain
probable first and second order effects of the recommendation. Explain the benefits and
risks of the recommendation.**
