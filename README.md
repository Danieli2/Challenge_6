**Challenge_6**


**Background**

I am an analyst at a proptech company that wants me to offer an instant, one-click service for people to buy properties and then rent them. The company wants to have a trial of this offering in the San Francisco real-estate market. If the service proves popular, they can then expand to other markets.
My job is to use my data visualization superpowers, including aggregation, interactive visualizations, and geospatial analysis, to find properties in the San Francisco market that are viable investment opportunities.

**What I am Creating**
For this Challenge assignment,I need to create and submit the following deliverable:

1. A Jupyter notebook that contains my analysis of the housing rental market data for San Francisco. 
2. The analysis will be complete with professionally styled and formatted interactive visualizations.


**Instructions**

I used the san_francisco_housing.ipynb notebook to visualize and analyze the real-estate data.

Additionally, I read the sfo_neighborhoods_census_data.csv file from the Resources folder into the notebook and then I created the DataFrame that I used in the analysis.

The main task in this Challenge is to visualize and analyze the real-estate data in your Jupyter notebook. Use the san_francisco_housing.ipynb notebook to complete the following tasks:

1. Calculate and plot the housing units per year.

2. Calculate and plot the average prices per square foot.

3. Compare the average prices by neighborhood.

4. Build an interactive neighborhood map.

5. Compose your data story.

**Calculate and Plot the Housing Units per Year**


For this part of the assignment, I used numerical and visual aggregation to calculate the number of housing units per year, and then I visualized the results as a bar chart. To do so, I completed the following steps:

I used the groupby function to group the data by year. Then I aggregated the results by the mean of the groups.

I used the hvplot function to plot the housing_units_by_year DataFrame as a bar chart. I made the x-axis represent the year and the y-axis represent the housing_units.

I styled and formatted the line plot to ensure a professionally styled visualization.


**Calculate and Plot the Average Sale Prices per Square Foot**

For this part of the assignment, I used numerical and visual aggregation to calculate the average prices per square foot, I then visualized the results as a bar chart. To do so,I complete the following steps:

I grouped the data by year, and then averaged the results. 
I created a new DataFrame named prices_square_foot_by_year by filtering out the “housing_units” column. 

I used hvPlot to plot the prices_square_foot_by_year DataFrame as a line plot.

**Compare the Average Sale Prices by Neighborhood**
For this part of the assignment, I used interactive visualizations and widgets to explore the average sale price per square foot by neighborhood. To do so, I complete the following steps:

1. I created a new DataFrame that groups the original DataFrame by year and neighborhood. I aggregated the results by the mean of the groups.

2. I Filter out the “housing_units” column to create a DataFrame that includes only the sale_price_sqr_foot and gross_rent averages per year.

3. created an interactive line plot with hvPlot that visualizes both sale_price_sqr_foot and gross_rent. I then set the x-axis parameter to the year (x="year"). Use the groupby parameter to create an interactive widget for neighborhood.

4. I styled and formatted the line plot to ensure a professionally styled visualization.


**Build an Interactive Neighborhood Map**
For this part of the assignment, I explored the geospatial relationships in the data by using interactive visualizations with Plotly and the Mapbox API. To build my map, I used the sfo_data_df DataFrame, which includes the neighborhood location data with the average prices. To do all this, I complete the following steps:

1. I Read the neighborhood_coordinates.csv file from the Resources folder into the notebook, and create a DataFrame named neighborhood_locations_df. 

2. I used the original sfo_data_df Dataframe, then created a DataFrame named all_neighborhood_info_df that groups the data by neighborhood. I aggregated the results by the mean of the group.

3. I reviewed the two code cells that concatenate the neighborhood_locations_df DataFrame with the all_neighborhood_info_df DataFrame.

I used Plotly Express, to create a scatter_mapbox for the all_neighborhoods_df DataFrame. I did the following:

I then set the size parameter to “sale_price_sqr_foot”.

I then set the color parameter to “gross_rent”.

following I set the size_max parameter to “25”.

then I set the zoom parameter to “11”.

I styled and formatted the line plot to ensure a professionally styled visualization.

**Compose Your Data Story**
I based on the visualizations that I created, to answer the following questions:

1. How does the trend in rental income growth compare to the trend in sales prices? 
2. Does this same trend hold true for all the neighborhoods across San Francisco?
3. What insights can you share with your company about the potential one-click, buy-and-rent strategy that they're pursuing? Do neighborhoods exist that you        would suggest for investment, and why?
