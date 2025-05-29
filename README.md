# Visual Interface Project 1

# Health Trends Visualization: Mapping Risks & Correlations at County Level

## About:

This project aims to visualize and analyse the possible correlations between various health risks across different counties in the United States. Using county-level data, the project explores how factors such as poverty rates, obesity, smoking, and chronic diseases relate to one another. By looking at the data, we can identify trends and patterns that may indicate potential relationships between socioeconomic factors, risk factors and health outcomes.

## Data:

The data was obtained from the official CDC website. It was taken from the Interactive Atlas of Heart Disease and Stroke. The atlas contains various County and State level statistics of various categories, primarily from the medical related categories. Certain categories that contained relevance to my project were selected. The data obtained contained several missing and -1 values, which was preprocessed within the Js file directly. 

Link to the Dataset used: https://github.com/Ironavenger475/VisualInterface1/blob/main/data/dataset.csv

Link to the CDC Atlas: https://nccd.cdc.gov/DHDSPAtlas/Default.aspx

## Sketches:
Initially, I had planned an outline where the dashboard was present in a page and the choropleth map in another page. But when that proved to not be permissible, I had the idea to split the page into halves and made a basic sketch of it. The initial stages of the project were based on this sketch and evolved as I proceeded along the stages.

## Visualization Components:

           i.             Bar chart:
The bar chart was made to show the gradual increase of the selected attribute and to see the general variance between counties
The data is presented in an ascending order of the attribute to show the gradual increase over the counties and shows it in two graphs for each attribute 
The bar chart when interacted with shows a tooltip with the county name and value of the attribute for the county below the cursor
 
        ii.              Scatterplot:
The scatterplot shows the data in a way that the user can see the data of all the counties at the same time and with ease
The data is arranged in a way where the x-axis is based on the socioeconomic or risk factors and y-axis is the health diseases such as stroke, diabetes etc.
The user can interact with the data by hovering over a certain point and a tooltip will appear showing the county name and the values of the two selected attributes.
The regression line for the scatterplot is also shown in a separate chart, which will show the progression of the plot, which shows the data progression.
 
     iii.              Histogram:
The histogram shows the frequency of the attribute
The user can get to know the average of the selected attribute from the county by seeing the highest range.
Like with the other components, hovering over each bar will show a tooltip showing the range and the number of counties that fall within that range.
     iv.               Correlation Gauge:
The correlation gauge shows the correlation between the two selected attributes and if they are related to each other.
The value ranges from –1 to 1. The closer to 1 the correlation is, the more related the two attributes are and conversely, the closer to -1 the correlation is, the more unrelated the two attributes are.
The gauge is presented in a manner like a speedometer with -1 being on the left side of the arc and 1 being on the right.
A needle in the middle shows the correlation value and it is also displayed in number format below it as well.
         v.             Choropleth Maps:
The choropleth maps are used to show the value of the selected attribute for each county on the map format.
It can help the user understand the distribution in a much easier manner.
The colour scale varies for each attribute.
The legend is present below the map to show the spread of the values.

There are two maps present so that the user can compare two attributes easily.

     vi.              Info Boxes:
There is info boxes present at the top right of each map to show the relevant info for each chart and how it works.

## Insights:

The user should be able to find a visible correlation between the attributes easily. By looking at the data, the user can explore the possible correlation between socioeconomic factors and health risks across different counties. They can see how higher poverty rates may be linked to increased obesity, diabetes, and smoking, potentially due to limited access to healthcare and nutritious food. The data also reveals geographic patterns, such as the Southeast having higher stroke and heart disease rates, while the West and Northeast might show lower smoking and obesity rates. Additionally, you can observe how behavioural factors like physical inactivity correlate with increased diabetes and heart disease, and how counties with a larger elderly population tend to have higher rates of chronic conditions. These insights can help the user understand regional health disparities and the need for targeted public health interventions.

## Process:

I used d3, TopoJSON and Math libraries for the application. I structured the code in a simple manner where each part was coded in a separate js file i.e. Charts and map js were in different files. This was done to combat any code brakeage that may occur when changing the code for any specific part. That way, only the intended part of the code would break, and the rest would be safely protected from it and any glitches could easily be isolated and fixed. 

The code can be run easily by either downloading from GitHub directly or cloning it via git. The code could then be run via an IDE such as Visual Code Studio by running the HTML file on a server (This is so that the d3 code will function as intended). Alternatively, the code could be run by visiting the site hosted by GitHub pages.

Github Repository: https://github.com/Ironavenger475/VisualInterface1

Hosted Site: https://ironavenger475.github.io/VisualInterface1/

## Challenges:

Some of the challenges faced were:

* Other parts of the code breaking when a change was made in an unrelated part
* The d3 library not filtering the data properly at times
* There was a scrapped feature where a heatmap would have been generated to show the correlation between the attributes by using cosine similarity. It was sadly hard to implement as the dataset was huge and a small part was not enough to generate good results. There was also an issue where the matrix generated from the data would only have 0 values.
* I had an idea to show the page as zoomed out to accommodate all the charts and two maps within a fully maximised webpage without the need to scroll. But it created issues with the tooltip positioning and had to be greatly altered to make it work as per my vision.
* There were several positioning issues that had occurred that had to be rectified via several changes to the CSS and Js code.

## Future Works:

* There is a plan to add more attributes to the dataset.
* The scrapped heatmap could be added once the matrix issue is fixed.
* Add a brushing feature where the selected components on the scatter map are highlighted on the choropleth map.
* Add a diverging bar graph with values such as urban or rural to see whether that also plays an effect to health risks or other factors.
