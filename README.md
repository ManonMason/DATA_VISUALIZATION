<h3 align="center"> Airline On-Time Performance Data for Summer 2022 </h3>
<h4 align="center">By Manon Mason</h4>

## Table of Contents
- [Installation](#installation)
- [Project Motivation](#motivation)
- [Project Details](#pd)
- [Dataset](#dataset)
- [Summary of Findings](#summary)
  - [Univariate Analysis](#univariate)
  - [Bivariate Analysis](#bivariate)
  - [Multivariate Analysis](#multivariate) 
- [Key Insights for Explanatory Analysis](#key)
- [Acknowledgements](#acknowledgements)

## Installation<a name="installation"></a>
This project was completed on Jupyter Notebook IDE, using Python 3. The libraries used were:


- Numpy
- Pandas
- Matplotlib
- Seaborn
- Glob
- Csv
- Datetime

We used Anaconda to install those libraries and to use as our environment manager.
## Project Motivation<a name="motivation"></a>

This project is the last project of the Data Analyst Udacity Nanodegree, and for this project I decided to work with The Airline On-Time Performance Data.

This dataset covers flight data from as early as 1987 to the present, but for analysis, I've decided to focus solely on flights from June 2022 to September 2022. 
Although four months may seem a short period of time to analyze, this is a conscious decision. I have excluded all data from 2020 and 2021 due to the unprecedented impact of COVID-19 on the travel industry during this period. It also seemed unfair to compare 2022 with 2019 or any years pre-covid. It cannot be denied that the pandemic significantly impacted airline performance and travel patterns and that the travel industry still feels its effect to this day.

I also wanted to focus on the peak summer months only, as this data can be helpful in the tourism industry and the individual who wishes to know more about certain airlines' performance before their summer vacation. The Airline On-Time Performance Data analysis from June 2022 to September 2022 can still be used as a valuable steppingstone or template for the analysis of future years or to compare the years before 2020 with those after 2020.

My main goal is to study the delays and cancellations and their causes.
  


### Project Details<a name="pd"></a>
This project is divided into two major parts.

Exploratory Data Analysis: After gathering, assessing, and cleaning the dataset, we used Python data science and data visualization libraries to explore the dataset's variables and understand the data's structure, oddities, patterns, and relationships. The goal was to keep the analysis structured, going from simple univariate to multivariate relationships,  using the "Question-Visualization-Observations" framework (asking a question from the data, creating a visualization to find answers, and then recording observations). 

Explanatory Data Analysis: Using findings from our exploration, we created a slide deck with polished visualizations to communicate and explain the project. This is the storytelling part of the project, making heavy use of the exploratory analysis.




### Dataset<a name="dataset"></a>

Airline On-Time Performance Data is a comprehensive dataset that provides valuable insights into US domestic airline performance, including carrier information, arrival and departure delays, and reasons for delays or cancellations. The data set is a valuable resource for anyone looking to understand airline performance and trends over time.

The airlines report the causes of delay in broad categories that were created by the Air Carrier On-Time Reporting Advisory Committee. 
The categories are Air Carrier, National Aviation System, Weather, Late-Arriving Aircraft, and Security. The causes of cancellation are the same, except there is no late-arriving aircraft category.
The categories are defined as follows:

- Air Carrier: The cause of the cancellation or delay was due to circumstances within the airline’s control (e.g. maintenance or crew problems, aircraft cleaning, baggage loading, fueling, etc.).

- Extreme Weather: Significant meteorological conditions (actual or forecasted) that, in the judgment of the carrier, delays or prevents the operation of a flight such as tornado, blizzard or hurricane.

- National Aviation System (NAS): Delays and cancellations attributable to the national aviation system that refer to a broad set of conditions, such as non-extreme weather conditions, airport operations, heavy traffic volume, and air traffic control.

- Late-arriving aircraft: A previous flight with the same aircraft arrived late, causing the present flight to depart late.

- Security: Delays or cancellations caused by evacuation of a terminal or concourse, re-boarding of aircraft because of security breach, inoperative screening equipment and/or long lines in excess of 29 minutes at screening checkpoints.


## Summary of Findings<a name="summary"></a>

### Univariate Analysis<a name="univariate"></a>

- Most flights have been canceled due to extreme weather (actual or forecasted). Very few flights were canceled because of security reasons (D).  
- Plotting a histogram of the delays, it shows that the distribution peaks just before 0, meaning that many flights were, in fact, early. Most of the early flights were early by 20 minutes or less. There are some outliers - some flights have arrived over 90 minutes early. Most of the flights were delayed by an hour or less, but some flights have been delayed by a day or more.  
- The most frequent delay is carrier delay, followed by late aircraft. Security delays happen rarely. Delays due to weather are also infrequent. However, since weather is the main cause of cancellations, we can deduce that if the weather looks bad, the airline tends to cancel flights instead of merely delaying them.

### Bivariate Analysis<a name="bivariate"></a>

- Republic, Endeavor, and American are the three airlines with the highest cancellation percentage. 
- Weather is the main reason for cancellation, followed by Carrier.
- Flights were more likely to be canceled on Thursdays, with fewer cancellations on Tuesdays and Saturdays.
- June had the most cancellations, followed by August, July, and September.
- When rating the state on cancellation percentage, New Jersey, Maine, New York, and Rhode Island are all in the top five, New Jersey being number 1 with a 6% cancellation rate.
- Looking at the delay percentage per state, Rhode Island is the only origin state that appears both in the top cancellation and the top delay, with an average delay of 80 minutes. Delaware is number one with a delay average of almost 3 hours.
- There is a slight correlation between delay and distance but a counter-intuitive one. Flights under 4000 miles suffered longer delays than flights over 4000 miles.
- The flights that were between 2000 and 3000 miles long were the flights that were most likely to be early by over an hour. There is also a small peak on the '30 to 60  minutes early' bin for those same flights. Long-haul flights, specifically those over 4500 miles, were never more than 24 hours late.
- Even though weather delays didn't happen frequently, they tended to create longer delays, with a mean of over 60 minutes.
- The airlines with the longest delays (on average) are Mesa Airlines, Endeavor Air, SkyWest, JetBlue, and American Airlines.  Alaska Airlines, Horizon Air and Hawaiian Airlines were performing the best.
- Distance in miles does not correlate with whether a flight will be canceled.

### Multivariate Analysis<a name="multivariate"></a>

-	Almost 50% of the flights leaving in the Evening got delayed, and the Evening also had the highest rate of cancellation, with over 3% of its flights being canceled.
-	The flights that have been delayed by 4 hours or less and by 12 to 24 hours late happened more frequently in the afternoon and evening. Less than 0.1% of flights are delayed by over 24 hours; however, it happens slightly more often in the Morning.
-	The cancellation percentage is between 1.6% and 3%, and the delay percentage is between 34% and 41% throughout the week. Tuesday has the smallest cancellation and delay percentage compared to the rest of the week, but no other pattern is emerging.
-	Hawaiian Airlines is doing great on cancellations, but over 50% of their flights were delayed. Even though Republic Airlines and Endeavor fare the worst regarding cancellation with 5%, their delay percentage is only about 30%.
-	Little to no correlation exists between the state of origin and the cancellation percentage.
-	We do not see any other pattern indicating that an airline is performing better or worse depending on the state it's flying from.






## Key Insights for Presentation<a name="key"></a>

Working with the Airline On-Time Performance dataset, my main goal was to study the canceled and delayed flights over the summer of 2022 and to dig out any patterns or relationships between variables that could help predict those delays and cancellations.

The exploration led to some dead ends or unsatisfactory answers. The correlation between distance in miles and delay was slim and non-existent between distance and cancellation. 

Although some states (like Delaware or New Jersey, for example) tend to have a higher percentage of delays and cancellations than others, we couldn't see any strong relationship between the state and the cancellation or delay variable.

However, we came away with two key insights:
-	Weather is one of the most disruptive issues when it comes to flying. Not only does it cause the most cancellations, but it also causes the longest delays.
- The timing of the flight does correlate with flight performance. Even though more flights happen in the Morning (between 6 am and noon), cancellations and delays happen more frequently and last longer in the Evening and the Afternoon.

Some slight changes will be made to the visualizations for the explanatory analysis. Those changes are mainly to diversify the plots and to make the presentation more fluid. Instead of a count plot to show the average delay per delay type, we will use a boxplot with a log transformation on the y-axis. The point plot for the delay bins and the time of day will be displayed side by side instead of one after another. We also picked more pleasant colors and updated the plot title, label, and axis.

## Acknowledgements<a name="acknowledgements"></a>


This project was completed as part of Udacity's Data Analyst Nanodegree.
The source for the data is the Bureau of Transportation Statistics.



