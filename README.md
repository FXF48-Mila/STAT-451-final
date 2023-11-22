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
This is a huge dataset that we cannot upload it to GitHub. To download the dataset, please use the link below. 

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

We selected a bar plot to represent the average obesity rates across different races nationwide from 2011 to 2021. From this bar plot, we can see that the national average obesity rate does vary by race between 2011 and 2021. With Diagonalization, overall, we see that the ranking of the average nationwide obesity rate for each race, from lowest to highest, is "Asian," "Other," "2 or more races," "Non-Hispanic White," "Hawaiian/Pacific Islander," "American Indian/Alaska Native," "Hispanic," and "Non-Hispanic Black." More specifically, the graph shows that Asians have the lowest average nationwide obesity rate (below 15%) relative to other racial groups, with a considerable gap. All other racial categories show national average obesity rates exceeding 25%, with other races and non-Hispanic whites in the 25-30 percent range; 2 or more races, Hispanic, and Native Hawaiian/Pacific Islander in the 30-35 percent range; and American Indian/Alaska Native and non-Hispanic blacks in the 35-40 percent range. Of these, the Non-Hispanic Black population registering the highest average rate. We also added a red dashed line to represent the average obesity rate over all races. We know from the graph that the average nationwide obesity rate for all race is very close to 30% (the true average nationwide obesity rate stands at 29.92%). As illustrated by the plot, with the exception of Asians, Others, and Non-Hispanic Whites, all other groups exceed this average.

### Analysis for Plot 2: Map of Average Obesity Rate by State, 2011-2021

### Analysis for Plot 3: Trend of Obesity Rate by Race/Ethnicity, 2011-2021
We used a line plot to show the trend in obesity rates between 2011 and 2021. Different colors of lines represent different races, such as Asian, Non-Hispanic White, Non-Hispanic Black, Hispanic, Hawaiian/Pacific Islander, American Indian/Alaska Native, 2 or more races, and Others. The legend on the right side of the figure helps in interpreting each line with a different color. The x-axis indicates the year (2011-2021) and the y-axis indicates the obesity rate. 
As a result, we can see that obesity rates for all races have a slight upward trend from 2011 to 2021. Comparing the obesity rates of all races, the obesity rate of Asians has been around 10% which is significantly lower than other races. Other races also have relatively low obesity rates except for Asians. Meanwhile, we can see that the obesity rate of Hawaiian/Pacific Islanders is increasing the fastest, from about 25 percent in 2011 to over 40 percent in 2021. Non-Hispanic Blacks also have a consistently high obesity rate. The increasing obesity rate year after year warrants more attention to physical health as well as obesity management.

