# ADAN-ADEC7900 Group 2

# Introduction
### Research Question

Are healthy fruits and vegetables affordable to Americans in each state? We aim to analyze the affordability of fruits and vegetables based on the average American household income by capita over multiple years. We hope to investigate whether income constraints influence access to fresh produce versus alternative forms (i.e., canned/frozen) and how this impacts adherence to dietary guidelines. The findings could inform policymakers responsible for food pricing regulations and programs like food stamps, helping them understand the challenges individuals and families face in accessing nutritious foods and potentially guiding adjustments to policies or interventions aimed at improving dietary habits, particularly considering potential differences in affordability between fruits and vegetables.

### Decision Maker

We plan to target our research for use by the Congressional Committees on Agriculture because they play a crucial role in shaping legislation and policies related to food and agriculture, including programs like the Supplemental Nutrition Assistance Program (SNAP) and other food assistance initiatives.

# Data Summary
**Provide a short description of the nature of the provided data set
and explain how these characteristics affect your analysis methodology. Summarize the
data set with basic descriptive statistics as applicable.**

The datasets include the average American household income per capita and fruit and vegetables prices from 2013, 2016, 2020. These datasets should allow us to investigate our research questions regarding the affordability of fruits and vegetables based on the average American household income by capita over multiple years. See below for a more in-depth explanation of the variables included in each dataset.

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

# Data Analytics
**Provide data analytics that add clarity to the research question.
Thoroughly discuss insight obtained from your visualizations and analysis of aggregated,
data. Suggest an excursion, and provide supporting analysis. Plots should be well
formatted according to best practices learned in class. Discuss the advantages and
challenges of performing analysis in your chosen software tool.**

### Analytical Tools & Methods 

We will conduct our analyses in R. Using publicly available datasets spanning multiple years, we will look at descriptive statistics and run statistical tests (e.g., t-tests, ANOVA) to investigate the affordability of fruits and vegetables by state across time. Specifically, descriptive statistics will investigate the average, minimum, and maximum prices of fruits and vegetables by year.  The ‘ggplot2’ package will be used to visualize the results, including interactive plots of fruit and vegetable prices, income per capita by state, and affordability of fruits and vegetables by state.

To quantify affordability, we developed an affordability metric based on the U.S. Department of Agriculture's recommended grocery budget of 11% of one's income (https://money.usnews.com/money/personal-finance/saving-and-budgeting/articles/how-much-should-i-spend-on-groceries). We then further subdivided the 11% and allocated 4% of one's income specifically for produce (so, 2% for fruits and 2% for vegetables). Since we're interested in affordability in relation to dietary guidelines, we calculated the price of a cup equivalent of fruits and vegetables (recommended daily serving; https://www.nidirect.gov.uk/articles/fruit-and-vegetables) for an entire year by multiplying the cup equivalent price by 365. Finally, to categorize a fruit or vegetable as affordable or unaffordable, we compared the yearly cup equivalent price (for fruit and vegetables separately) to 2% of per capita income by state. If the yearly cup equivalent price was greater than 2%, that fruit or vegetable was deemed unaffordable. If the yearly cup equivalent price was less than 2%, that fruit or vegetable was deemed affordable.

We hope to discover important insights by examining trends in fruit and vegetable affordability by state. These insights will inform policymaking, with a particular focus on enhancing food assistance programs and regulations overseen by the Congressional Committees on Agriculture.

### Questions of Interest

**1. What are the most and least expensive fruits? How does this change across years?**

![unnamed-chunk-6-1](https://github.com/asteinkrauss/7900Group2/assets/164549275/46a5c31e-2a95-4c5c-9aac-d0d5d5e2ad69)
![unnamed-chunk-6-2](https://github.com/asteinkrauss/7900Group2/assets/164549275/7d61b66e-fd92-4ec8-aeb8-2b441a551179)
![unnamed-chunk-6-3](https://github.com/asteinkrauss/7900Group2/assets/164549275/a20e028a-8d18-4813-9796-e16d5c045517)
![unnamed-chunk-6-4](https://github.com/asteinkrauss/7900Group2/assets/164549275/508edde9-7329-4159-858c-a4e7cf4e279a)
![unnamed-chunk-6-5](https://github.com/asteinkrauss/7900Group2/assets/164549275/f5afc022-5a34-4861-be03-29d0544ec3c6)
![unnamed-chunk-6-6](https://github.com/asteinkrauss/7900Group2/assets/164549275/4aefaa91-3f8f-4ba6-99ca-9932c99748d1)

**2. What are the most and least expensive vegetables? How does this change across years?**
![unnamed-chunk-8-1](https://github.com/asteinkrauss/7900Group2/assets/164549275/2dc2a0e1-4cc9-430a-94f1-ee96097c5b48)
![unnamed-chunk-8-2](https://github.com/asteinkrauss/7900Group2/assets/164549275/450c0374-e928-4dc3-9824-8885828ee66a)
![unnamed-chunk-8-3](https://github.com/asteinkrauss/7900Group2/assets/164549275/3454e858-cd28-427b-b65b-fdd2b710ffad)
![unnamed-chunk-8-4](https://github.com/asteinkrauss/7900Group2/assets/164549275/1548cd63-5e76-40ec-a443-7bc11006b401)
![unnamed-chunk-8-5](https://github.com/asteinkrauss/7900Group2/assets/164549275/f8b6d5e3-7085-452c-a9a1-160847ebd66a)
![unnamed-chunk-8-6](https://github.com/asteinkrauss/7900Group2/assets/164549275/1c55e104-0342-473b-a695-3b734c95fb61)

**3. How does income per capita differ by state across years?**
![unnamed-chunk-10-3](https://github.com/asteinkrauss/7900Group2/assets/164549275/6b56d0e0-323a-409b-8136-1ca72a648cf2)
![unnamed-chunk-10-5](https://github.com/asteinkrauss/7900Group2/assets/164549275/37242604-16fb-4c00-bae5-d2f202f3aec5)
![unnamed-chunk-10-7](https://github.com/asteinkrauss/7900Group2/assets/164549275/9e1baa26-667c-4070-9a51-ca859b04c238)

**4. How do the prices of different forms of fruits and vegetables change by year?**
![FruitForm](https://github.com/asteinkrauss/7900Group2/assets/164543699/8c6d95a4-f311-4f31-a8c1-eef8bb4ff8c8)
![VegForm](https://github.com/asteinkrauss/7900Group2/assets/164543699/3f8f1fe3-e8df-4328-88bd-f6507c3fdff9)

**5. How many people can afford the recommended daily serving of fruits and vegetables across years?**
![AffordBar](https://github.com/asteinkrauss/7900Group2/assets/164543699/38fa6bac-2f54-478e-b1af-6683d3ea6323)

**6. EXCURSION ANALYSIS -- How does the affordability of fruits and vegetables differ amongst their different forms?**
![FruitAff](https://github.com/asteinkrauss/7900Group2/assets/164543699/870ee087-b748-422e-a667-ff55518f3500)
![VegAff](https://github.com/asteinkrauss/7900Group2/assets/164543699/ced81be9-5a77-45fb-a901-41b82ad15a79)



# Conclusion
**Summarize the analytical methodology and provide closure to your
analytical story. Succinctly answer the research questions. Highlight the limitations of
your findings and recommend future work. Do not make policy recommendations here.**

# Policy Recommendation
**Introduce a specific policy decision that your decision
maker is facing. Provide a data driven recommendation for their decision. Explain
probable first and second order effects of the recommendation. Explain the benefits and
risks of the recommendation.**
