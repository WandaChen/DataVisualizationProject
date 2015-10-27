# DataVisualizationProject
#### Background 
Recently I heard a news regarding equal pay for both male and female, which made me more interested in this issue. I wondered if culture or other issues caused the gender wage gap.   

### Summary
Gender Wage Gap Project  - Using Data visualization to see different countries' median gender wage gap in the 21st Century.  1) The top 2 countries that have the largest gender wage gap (Korea and Japan) might be due to culture issues - Male chauvinism for example.  
2) New Zealand seems to have the lowest percentage across the years.  Although Hungry had the lowest percentage for a few years,  it also had a few years that were more than 10%.
3) Most of the countries' gender wage gap between male and female was between 10% and 25%.

### Design
1.	Data Selection – I decided to pick the data that is from OECD Data about Gender Wage gap https://data.oecd.org/earnwage/gender-wage-gap.htm.  When I saw the map, it looked similar to the D3 lesson that about World Cup.  But it also made me interested and wanted to answer the question - “Will gender wage gap depend on the country that is labeled as first World, developing country, or will other cultural background affect the gender wage gap?”  Especially recently I heard on the news about the equal pay for both male and female.  It maked me even more interested in this issue.
2.	Map Data – I used the files (world_countries.json) and codes that was supplied during lesson 4 to draw the map for my visualization.
3.	After creating the map, I realized that my original data set (GenderWageGap_00_12.csv) only has a field of country codes.  If I wanted to indicate the location on the map, I needed to add the location information to the data set.  After some online research, I decided to add 3 fields to the updated data file (GenderWageGap_00_12_geo.csv)  – country name, longitude and latitude for the capital city of the country.  So later on if I want to add a bubble indicator, it will be located on the capital city for that country.
4.	I was having difficulties to figure out how to use D3 to combine the map and data to create the visualization.  SO I decided to go with easier graphs.  I was wondering if I can recreate the line chart that the web site provided.  The reason I selected line chart is because I can use this data set which can be groupped in 2 ways – either by Years then Country, or Countries then by Years.  I would like to show the first method.  It can tell the difference how each country gender wage gap changed throughout each year.  And it also can show the difference of how countries changed for each year.
5.	After creating the multi-line charts, I added different colors to each country in the data set.  There were 36 countries, and 334 lines of data.  I saw one of the multi-lines examples showing both animation and interaction through the legend.  I decided to use this idea as my interactive with user.
6.	Legend - Since there was 36 countries in the dataset, if I list all of them in one row or column, it would be really confusing.  So I turned them into the 3 rows of legend that is below the main graph.  It also acted as keys for user to interact.
7.	Interact -  I saw one example use bootstrap to show to 2 graphs on the same screen, so I decided to use this idea to show my interactive graph.
     * User can hover the scatter plot point to see the information.  However, since there was more than 300 points on the graph, and it is difficult to see one country's data.  
     * User can click on the country code legend to see more detail for that country:
          - show the bar graph with each individual value (below the main graph)
          - the line that belongs to the selected country will be enhanced (thicker than other)

### Feedback
Questions for feed back response:
  * What do you notice in the visualization?
  * WHat questions do you have about the data?
  * What relationships do you notice?
  * What do you think is the main takeaway from this visualization?
  * Is there something you don't understand in the graph?
  
#### Version 1 
1. 17 years old high school girl:
    - (Q1) The gender wage gap between men and women is increaseing for some countries and decreasing for others.
    - (Q2) Why does every country have a similiar trend of going up/down?
    - (Q3) They all have a similar trend.
    - (Q4) Not enough knowledge to make statement
    - (Q5) I don't know why this topic is significant to the people of today.
2. My spouse:
    - (Q1) band of items are similar, result of common background, contrast?
    - (Q2) missing data points, important? outlier?
    - (Q3) a few are close to 0%, then drift up.
    - (Q4) wide spread of gaps ,median unknow.
    - (Q5) How does the difference show the women's earnings gap? What is the mathematics formula to calculate the percentage?

### Resources
1.	OECD (2015), Gender wage gap (indicator). doi: 10.1787/7cee77aa-en (Accessed on 10 October 2015)
http://www.oecd-ilibrary.org/employment/gender-wage-gap/indicator/english_7cee77aa-en?isPartOf=/content/indicatorgroup/4ead40c7-en
2.	D3 Lesson – World Cup Example Codes.
3.	D3noob’s blocks http://bl.ocks.org/d3noob
4.	Multi-Series Line Chart http://bl.ocks.org/mbostock/3884955
5.	Building a Multi-Line Chart Using D3.js: Part 2 http://code.tutsplus.com/tutorials/building-a-multi-line-chart-using-d3js-part-2--cms-22973
6.	https://en.wikipedia.org/wiki/Developing_country
7.	http://www.delimited.io/blog/2014/3/3/creating-multi-series-charts-in-d3-lines-bars-area-and-streamgraphs
8.	http://bl.ocks.org/phoebebright/raw/3176159/
9.	Small Multiples mbostock’s block #1157787 August 19, 2011 http://bl.ocks.org/mbostock/1157787
10.	saadkhan321’s block #3afb4229b42e81dfcace July 29, 2015 http://bl.ocks.org/saadkhan321/3afb4229b42e81dfcace
11.	Multi-line graph with automatic legend and toggling show / hide lines.
 http://www.d3noob.org/2014/07/d3js-multi-line-graph-with-automatic.html
