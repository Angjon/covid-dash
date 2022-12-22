

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
- Create virtual environment;
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
In order for further analysis and data treatment, it is required to have all dataframes in a specific format, having the dates as indexes and countries/states as headers. Using pandas and encapsulating each step into a function, we're able to store once again into a dictionary the cleaned data.

## Learning Process

### Theory Applied
- [x] Numpy
- [x] Pytorch
- [x] Neural Nets
- [x] Flask

### Challenges
- Training the bot to understand the words was challenging, especially because Portuguese have some special characters like (^~`´).

### Improvements
 - The JSON file does not have much info, we could improve this in order to get better responses from the bot.
 

## Authors
Jonas Angulski <br>

  
  sources: https://chatbotsmagazine.com/contextual-chat-bots-with-tensorflow-4391749d0077
  
  Huge thanks to <a href="https://www.youtube.com/channel/UCbXgNpp0jedKWcQiULLbDTA" target='_blank'>Python Engineer </a> for providing an awesome Pytorch tutorial.
  

  
  

