# ADAN-ADEC7900 Group 2
Dataset of average American household income per capita and fruit and vegetables prices from 2013, 2016, 2020.

# Research Question

Are healthy fruits and vegetables affordable to Americans in each state? We aim to analyze the affordability of fruits and vegetables based on the average American household income by capita over multiple years. We hope to investigate whether income constraints influence access to fresh produce versus alternative forms (i.e., canned/frozen) and how this impacts adherence to dietary guidelines. The findings could inform policymakers responsible for food pricing regulations and programs like food stamps, helping them understand the challenges individuals and families face in accessing nutritious foods and potentially guiding adjustments to policies or interventions aimed at improving dietary habits, particularly considering potential differences in affordability between fruits and vegetables.

# Decision Maker

We plan to target our research for use by the Congressional Committees on Agriculture because they play a crucial role in shaping legislation and policies related to food and agriculture, including programs like the Supplemental Nutrition Assistance Program (SNAP) and other food assistance initiatives.

# Included Data
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

**These two datasets should allow us to investigate our research questions regarding the affordability of fruits and vegetables based on the average American household income by capita over multiple years.**

# Analytical Tools & Methods 

We will conduct our analyses in R. Using publicly available datasets spanning multiple years, we will look at descriptive statistics and run statistical tests (e.g., t-tests, ANOVA) to investigate the affordability of fruits and vegetables by state across time. Specifically, descriptive statistics will investigate the average, minimum, maximum prices of fruits and vegetables by year.  The ‘ggplot2’ package will be used to visualize the results, including interactive plots of fruit and vegetable prices, income per capita by state, and affordability of fruits and vegetables by state.

We hope to discover important insights by examining trends in fruit and vegetable affordability by state. These insights will inform policymaking, with a particular focus on enhancing food assistance programs and regulations overseen by the Congressional Committees on Agriculture.
