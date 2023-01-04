

<p align="center"><img src="https://cdn-icons-png.flaticon.com/512/2782/2782066.png" alt="Dash" width="25%" border="0"><br /></p>


<h1 align="center"> 🧮 Dashboard with Python | Covid dashboard </h1>

## Project Status
<p>:heavy_check_mark: Complete<p>

<p> Dashboard available at: <a href="http://jonasangulski.pythonanywhere.com/" target="blank">Corona Dashboard </a> <p>

## Table of Contents 
- [Objective](#objective)
- [Process](#Process)
- [Results](#Results)
- [Learning Process](#Learning-Process)
- [Authors](#Authors)

## Objective

The objective of this project is to build an interactive USA, Brazil and worldwide corona virus dashboard using the Dash library and setting it up in a remote server for anyone to see.

## Process
- Get the data from repositories and websites;
- Data cleaning and transformation;
- Smooth the data via LOWESS method;
- Prediction modeling;
- Encapsulate into classes;
- Build dashboard with Dash;
- Deploy dashboard via Python Anywhere;

## Getting the data
The data for USA and world can be found in the <a href="https://github.com/CSSEGISandData/COVID-19" target="blank"> John Hopkins COVID-19 GitHub repository. </a> While for Brazil the data is available in CSV format at <a href="https://covid.saude.gov.br/" target="blank"> Ministry of Health website.</a> The data keeps track of all cases and deaths sorted by either country or state, therefor, containing all information needed for the project. After getting the data and storing it locally, a dictionary of dataframes is created.

## Data cleaning
In order for further analysis and data treatment, it is required to have all dataframes in a specific format, having the dates as indexes and countries/states as headers. Removing bad data and encapsulating each step into a function, we're able to store once again into a dictionary the cleaned data.

## Data Smoothing
The reported data presents a massive variation due delay factors, like weekends or holidays for example. To counter that, the smoothing method LOWESS (locally weighted scatterplot smoothing) is applied. From the statsmodel package, we import the lowess function, fixing the window size to 15 observations.

## Modeling prediction function
The covid wave curves resembles itself to a logistic function, presenting an upper and lower asymptotes. With that in mind, we use <a href="https://docs.scipy.org/doc/scipy/reference/generated/scipy.optimize.least_squares.html" target="blank"> scipy least_squared </a> function to stipulate the parameters of the function that would best fit the wave curve. Therefor, being able to predict future values.

## Encapsulate into classes
In this step it's brought together all the tasks done previously. From getting the data and smoothing to training and predicting it. Two classes are created to summarize the job done, the CasesModel and DeathsModel, since all the previous code was executed as methods, putting them together was simple.

## Build dashboard with Dash
Now using a combination of two libraries, <a href="https://plotly.com/python/" target="blank"> Plotly </a> and <a href="https://dash.plotly.com/" target="blank"> Dash </a> we are able to build the dashboard. Using Plotly to create the interactive visualizations and Dash to properly build the dashboard using its tools such as data tables, dropdowns, tabs and radio buttons.

## Deploy dashboard
In order to make the dashboard available to the public, it was used <a href="https://www.pythonanywhere.com/" target="blank"> Python Anywhere </a> as a remote server.Moving all the code files previously encapsulated into classes to Python Anywhere alongside with the csv dataset files, the server was deployed sucessfully, making it available <a href="https://www.pythonanywhere.com/" target="blank"> here </a>

### Challenges
-The data wrangling for Brazil required special attention since it had to be shaped exactly like the USA and Global data so it could be futher developed.
-First contact with HTML and CSS proved to be quite the struggle.

### Improvements
 - Originally the data was suposed to be updated every single day, as long as the server was online. However, after adding Brazil data set, this idea had to be descarted, it would be required web scraping for it to be applied.
 - Add cloropeth map for Brazil (currently only USA and global maps are available).
 
## Authors
<p>Jonas Angulski <p>

<p> Source: <a href="https://www.dunderdata.com/build-an-interactive-data-analytics-dashboard-with-python" target="blank"></a>

<p> Massive thanks to <a href="https://www.dunderdata.com/build-an-interactive-data-analytics-dashboard-with-python" target="blank"> Teddy Petrou </a> for creating this incredible course.
  

  
  

