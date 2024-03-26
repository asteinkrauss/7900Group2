# ADAN-ADEC7900 Group 2
dataset of average American household income by capita and fruit and vegetables prices from 2013, 2016, 2020

# Research question & Decision maker

We aim to analyze the affordability of fruits and vegetables based on the average American household income by capita over multiple years. We hope to investigate whether income constraints influence access to fresh produce versus alternative forms (i.e., canned/frozen) and how this impacts adherence to dietary guidelines. The findings could inform policymakers responsible for food pricing regulations and programs like food stamps, helping them understand the challenges individuals and families face in accessing nutritious foods and potentially guiding adjustments to policies or interventions aimed at improving dietary habits, particularly considering potential differences in affordability between fruits and vegetables.

# Data sets included:
Fruit Prices 2013.csv ------- Fruit Prices 2016.csv   -------   Fruit Prices 2020.csv

Vegetable Prices 2013.csv ------- Vegetable Prices 2016.csv ------- Vegetable Prices 2020.csv

-> 
*Columns present:*

**Fruit/Vegetable:** type of food (apple, oranges, broccoli, etc)

**Form:** Categorical (fresh, canned, dried, juice, frozen)

**RetailPrice:** in $

**RetailPriceUnit:** Categorical (per pound, per unit)

**Yield:** Preparation yield factor

**CupEquivalentSize:** For many fruits and vegetables, a 1-cup equivalent equals the weight of enough edible food to fill a measuring cup

**CupEquivalentUnit:** Categorical (pounds, fluid ounces)

**CupEquivalentPrice:** in $; price per edible cup equivalent (the unit of measurement for Federal recommendations for fruit and vegetable consumption)

**Year:** Categorical (2013,2016,2020)

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

We aim to conduct our analysis in R. We will use ggplot2 to visualize the data sets and interpret the data. 
