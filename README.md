# Summary of the project to study obesity rates and race

## Motivation
Analyzing obesity rates by race is critical to understanding differences in health outcomes across racial and ethnic groups. 
Such analyses can help to identify the underlying sociocultural, economic, and environmental factors that contribute to varying
obesity prevalence rates, thereby drawing attention to addressing health inequities and scaling up more effective public health
initiatives within a given group.

## Our questions
Here, from Centers for Disease Control and Prevention, the obesity rate in our analysis is defined as the proportion 
of adults with a body mass index (BMI) $\geq 30 kg/m^2$.
The question we want to address is "Do obesity rates vary by race?" More specifically, we would like to explore this issue 
in terms of geographical location and year. Therefore, when building the shiny app, our specific question could be, 
"Did the average obesity rate vary by race between years XX and XX?" ; 
"What did obesity rates look like in relation to race between years XX and XX?" ; 
"What did obesity rates look like for specific races in each state in a given year?"; And so on. 

## Dataset
We decided to use the “Nutrition, Physical Activity, and Obesity - Behavioral Risk Factor 
Surveillance System” dataset that we found on data.gov. 

This dataset contains 33 variables and 88629 observations, documenting the obesity rates for eight races in states across the U.S. from 2011 to 2021.

The link to the dataset is: https://catalog.data.gov/dataset/nutrition-physical-activity-and-obesity-behavioral-risk-factor-surveillance-system

The columns we choose to use to solve this question in the dataset are `Race / Ethnicity`
(for race), `Data_Value_Alt` (for the BMI), `Geolocation` (for the geographical location), and `Year End` (for year). We will filter out
the dataset by "Class == 'Obesity / Weight Status'" and "Question == 'Percent of adults aged 18 years and older who have obesity'"
since we only care about the obesity rate in this dataset. Since the dataset contains the
necessary information, it is possible to answer the questions with this dataset. 

## Preliminary Visualization

### Note
In order to make our mapping more aesthetically pleasing, we decided to use abbreviations for the full name of the race/ethnicity.

Below is the Abbreviations Comparison Table:

"AS" = "Asian" 

"OTR" = "Other" 

"2+" = "2 or more races" 

"NHW" = "Non-Hispanic White"

"HPI" = "Hawaiian/Pacific Islander" 

"AI/AN" = "American Indian/Alaska Native" 

"HISP" = "Hispanic" 

"NHB" = "Non-Hispanic Black"



### Analysis for Plot 1: National Average Obesity Rates by Race, 2011-2021

We selected a bar plot to represent the average obesity rates across different races nationwide from 2011 to 2021. The data indicates that Asians report the lowest obesity rates relative to other racial groups, with a considerable gap. All other racial categories show average obesity rates exceeding 25%, with the Non-Hispanic Black population registering the highest average rate. The average nationwide obesity rate stands at 29.92%, and as illustrated by the plot, with the exception of Asians, Others, and Non-Hispanic Whites, all other groups exceed this average.

