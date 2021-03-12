![seattle banner](./images/king_county_overview.jpg)<br><br>

# King County, Washington Housing Prices Predictions
**Author**: [Chaz](https://github.com/Mynusjanai)<br><br>



## Project and EDA Goals

- **Analysis:** Identify features in the data that correlate with the price of homes sold to make accurate pricing predictions of future houses on the market in the county of Kings, WA.<br><br>

- **Feature Engineering:** Create new data insights based on the data and information given to give greater accuracy and predictive power to our predictive models.<br><br>

- **OLS and Sci-kit Learn Models:** Use our substantiated data to build models to predict future housing prices, while continuously tweaking our features and insights to analyze and conclude on the best model to put into production.<br><br>

- **Test Our Optimal Model:** Test the best fit model against the holdout data to predict our housing prices to an accuracy of within 200,000k.<br><br>

 

## Overview of Data and Feature Observations

- **price:** Our target variable which we are looking to predict against.
- **bedrooms:** Bedrooms in relation to square footage is important.
- **bathrooms:** Bathrooms hold even greater significance to the value of the home than bedrooms. Plumbing set up is crucial, and the mean of baths is around 3.3.
- **sqft_living:** Square footage of the entire home. This includes the basement (if present). 
- **sqft_lot:** The overall yard and property size of the home. Nearest neighbors lot size seems to have a stronger correlation to price.
- **floors:** Possible mezzanines, banisters, catwalks, attics, sub-basements, or garage floors.
- **waterfront:** Increases the property value of the home.
- **view:** Same as waterfront properties, but with an even larger correlation to price.
- **condition:** Value unknown if higher = better or reverse.
- **was_reno:** Whether or not the home was renovated. Stronger correlation to price than the actual year a home had work done, or how long its been since the last renovation.
- **zipcode:** Homes to the north of the county come in at a higher sale price than others. Deeper dive into features of these homes and amenities could prove even more fruitful in analysis and pricing predictions.<br><br>



## A Look at Some Features

![age of home built](./images/age_built.png)<br><br>

**Key Takeaways:** <br><br>
- Examining the prices homes have sold for according to their age, shows younger homes and older homes selling for much higher prices than those in the past 30-70 years.<br><br>

- This may be to older homes’ build quality, vintage style and flair, or larger land plots. Younger homes may tend to have newer appliances, integrated technology (ie. smart homes), more outlandish architecture techniques, and resistance against regional natural disasters like earthquakes.<br><br>


![grade vs price](./images/grade_vs_price_rev.png)<br><br>

**Key Takeaways:** <br><br>
- We can clearly see a distinct association between the grade of a property, vs the price it fetched. Initial OLS linear regression models show that the top 3 ratings boost the sale price of properties by an average of $106,000, while lower ratings can depreciate the sale values. ANOVA statistical tests also confirm these insights.<br><br>

- Key takeaways from this is to dive a bit deeper into the grading system, and potentially isolate the best grades from those that perform worse. There may be a relationship to the square footage of the home, number of beds/baths, condition, and other factors that are holding these homes back or making them undesirable <br><br>



## Methodology

- **First Steps:** Models for prediction were first created by analyzing the housing data through EDA, and identifying which features and facets in the data would be good indicators to point to predictive analysis of housing prices.<br><br>

- **Building Features & Further Data:** Feature Engineering of new data from that provided and inferred will help to further identify insights into the data.<br><br>

- **Model Preparation:** Data techniques such as creating dummy variables, OLS summary models, and polynomial data will help serve our interpretation of our data when building our best models.<br><br>

- **Predictive Modeling:** Various modeling techniques are implemented, including: Log, K-Best, Recursive Feature Elimination, and Polynomial modeling to determine the best fit in predicting our housing prices.<br><br>



## Key Takeaways from the Modeling Process

- **Accuracy of Predictive Modeling.** Our log model did the best in terms of predicting the training data in comparison to our test data. We'll take this model also to its low standard deviation of error in regards to the mean of overall housing prices. We will see that this model captures a range of 80% of all predictive housing prices.<br><br>

- **Grade and Location is Crucial.** The grade of a property in relation to its location has shown to be a large determining factor of the property's selling price.<br><br>

![grade ranking](./images/grade_ranking.png)<br><br>

- **Tiny Details Matter.** Things such as the view a property has, its proximity to water, as well as the amount of bathrooms and whether or not they were renovated hold weight. The age of the home has also shown to skew towards older, more classic homes and newer, perhaps more technologically advanced homes with integrated smart systems.<br><br>


## For More Information

See the full analysis in the [Jupyter Notebook](./final_housing_notebook.ipynb) or review this [presentation](./kc_wash_analysis.pptx).

For additional info, contact the author of this project, [Chaz Frazer](https://github.com/Mynusjanai).<br><br>


## Github Repository Structure

```
├── data
├── trials
│   ├── holdout_notebook.ipynb
│   ├── phase_2_project_workbook.ipynb  
├── img
├── final_housing_notebook.ipynb
├── kc_wash_analysis.pptx
├── README.md
```
