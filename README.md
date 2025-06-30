# Energy-Consumption-Predictor
Energy Consumption Predictor is a data science project built to help the South Carolina electric utility company eSC forecast and manage residential energy consumption during peak summer months. It combines hourly energy usage, weather data, and building metadata from 5,700+ homes to predict high-demand scenarios and recommend energy-saving strategies.

## Objectives
- Identify variables influencing residential energy consumption.
- Forecast July energy demand using time-series models.
- Visualize insights through an interactive Shiny dashboard.

## Analytical Approach
We consolidated three datasets—hourly energy usage, hourly weather conditions, and static house attributes—by iterating through each building ID and aggregating monthly averages. A **time-series linear regression model** was then developed using key predictors like appliance type, temperature, and cooling setpoints.

### Accuracy and Evaluation
The model was trained on 80% of the data and tested on the remaining 20%. Accuracy was evaluated based on whether predictions fell within a **±30% range of the actual energy consumption**. For example, if actual usage was 1000 kWh, predictions between 700–1300 kWh were considered accurate. Using this threshold, the linear regression model achieved an **accuracy of 75–85%** across the test set.

## Dashboard Features
An interactive Shiny dashboard was built with three key tabs:
1. **Static House Data Review** – Explore energy consumption by demographic, appliance type, and usage patterns.
2. **Energy Usage Hotspot** – Visualize county-level consumption using gradient heatmaps.
3. **Future Prediction** – Simulate energy use based on user-defined temperature and appliance settings.

## Technologies Used
R, Shiny, ggplot2, plotly, tidyverse, caret, kernlab, usmap, DT, dplyr

## Live Dashboard
View the project here: [Energy Predictor Dashboard](https://pisin.shinyapps.io/energyPredApp/)
