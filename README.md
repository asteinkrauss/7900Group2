# ADAN-ADEC7900 Group 2
dataset of average American household income by capita and fruit and vegetables prices from 2013, 2016, 2020

# Research Question

Are healthy fruits and vegetables affordable to Americans in each state? We aim to analyze the affordability of fruits and vegetables based on the average American household income by capita over multiple years. We hope to investigate whether income constraints influence access to fresh produce versus alternative forms (i.e., canned/frozen) and how this impacts adherence to dietary guidelines. The findings could inform policymakers responsible for food pricing regulations and programs like food stamps, helping them understand the challenges individuals and families face in accessing nutritious foods and potentially guiding adjustments to policies or interventions aimed at improving dietary habits, particularly considering potential differences in affordability between fruits and vegetables.

# Decision Maker

We plan to target our research for use by the Congressional Committees on Agriculture because they play a crucial role in shaping legislation and policies related to food and agriculture, including programs like the Supplemental Nutrition Assistance Program (SNAP) and other food assistance initiatives.

# Data sets included:
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
| Fruit/Vegetable  | type of food (apple, oranges, broccoli, etc)  |
| Form  | form of food (fresh, canned, dried, juice, frozen)  |
| RetailPrice  | price of food (in $)  |
| RetailPriceUnit  | type of retail price (per pound, per unit, etc)  |
| Yield  | Preparation yield factor  |
| CupEquivalentSize  | a 1-cup equivalent equals the weight of enough edible food to fill a measuring cup  |
| CupEquivalentUnit  | type of unit (pounds, fluid ounces)  |
| CupEquivalentPrice  | price per edible cup equivalent (the unit of measurement for Federal recommendations for fruit and vegetable consumption) |
| Year  | Years included (2013, 2016, 2020)  |


Annual person income by county.csv

-> *Columns present:*

**GeoFIPS:** increases by 1000 by state (01000 = Alabama)

**GeoName:** region and state, if no region present only state is listed

**Description:** Categorical, (Personal income (thousands of dollars), Population (persons) 1/, Per capita personal income (dollars) 2/	)
1Personal income (thousands of dollars)Consists of the income that persons receive in return for their provision of labor, land, and capital used in current production as well as other income, such as personal current transfer receipts. In the state and local personal income accounts the personal income of an area represents the income received by or on behalf of the persons residing in that area. It is calculated as the sum of wages and salaries, supplements to wages and salaries, proprietors' income with inventory valuation (IVA) and capital consumption adjustments (CCAdj), rental income of persons with capital consumption adjustment (CCAdj), personal dividend income, personal interest income, and personal current transfer receipts, less contributions for government social insurance plus the adjustment for residence.

2Population (persons)The number of individuals (both civilian and military) who reside in a given area.

3Per capita personal income (dollars)The personal income of a given area divided by the resident population of the area. See "personal income." 


**Unit:** Categorical, (Thousands of dollars, Number of persons, Dollars)

**2013:** in $, persons

**2016:** in $, persons

**2020:** in $, persons

**These two datasets should allow us to investigate our research questions regarding the affordability of fruits and vegetables based on the average American household income by capita over multiple years.**

# Briefly propose the tools and methods used to perform the analysis 

We aim to conduct our analysis in R. We will use ggplot2 to visualize the data sets and interpret the data. Using available datasets spanning multiple years, we employ a range of data analysis methods including descriptive statistics, correlation analysis, spatial analysis, and data visualization. By examining trends in fruit and vegetable affordability across the country and their relationship with household income, we aim to provide insights that inform policymaking, particularly within the realm of food assistance programs and regulations overseen by the Congressional Committees on Agriculture.

Descriptive statistics will involve calculating summary statistics for fruit and vegetable prices across different forms (fresh, canned, frozen, etc.) and years. This will help outline the trends in food prices an affordability metrics over time. Statistical tests (e.g., t-tests, ANOVA) will also be used to compare affordability metrics between different income brackets, regions, or years. By examining these metrics, we aim to assess the significance of differences in affordability across demographic groups. Correlation analysis will investigate correlations between affordability metrics and per capita income levels across different regions or states, examining the relationship between affordability of fruits/vegetables and adherence to dietary guidelines. We will also conduct spatial analysis, utilizing geographic data to analyze spatial variations in fruit and vegetable affordability across different regions.
