# Data-Science-1-Group-Project

Data source: What is the nature of the data you chose? Why is it interesting? 

The dataset used in this analysis is posted on the online data science community Kaggle (https://www.kaggle.com/sobhanmoosavi/us-accidents).  It consists of car accident data in 49 states of the United States collected from February 2016 to December 2019.  There are close to 3 million accident records in this dataset, making it a robust data source to conduct our analysis.  

For each accident record, this dataset includes 49 attributes that can be roughly split into 6 categories:  Administration (ex. Record ID, Source of data); Accident Description (ex. Severity, Start and End times), Location (ex. State, Time zone), Weather (ex. Temperature, Humidity, Visibility), Road Design (ex. Presence of traffic signal, Bump, Roundabout), Time of Day (ex. Sunrise, Sunset). 

The goal of this study is to come up with recommendations on how to improve road safety by exploring the predictive and descriptive factors that affect accident rates and severity.   

 

Analysis: What were the challenges? How did you overcome them? 

Data cleaning – Our first challenge was how to manage and clean such a large dataset (~3 million records).  We decided to transform many of the existing variables with string values (ex. Side of the street is “L” or “R”) to integers (L=0, R=1) in order to simplify the analysis.  In some instances where data is missing, we imputed these values based on other data that is available (ex. if a temperature value was missing, we used the median of that particular week’s temperature to fill in the missing value).   

Narrowing our focus on important features – Since there are so many variables in this dataset, one of our challenges is to narrow down on the attributes that most correlate to accident severity.  To do this, we compared five different predictive models and determined that the Random Forest Classifier model was the most accurate prediction model, hence it was used to generate a ranking of the most important variables that are predictive of accident severity.   

Categorizing numerical scales – Many of the attributes related to weather patterns are on a numerical scale (ex. temperature in degrees Celsius).  Therefore, in order to show the impact of these weather attributes on a bar graph, we “binned” the numerical ranges into categories.  For example, temperature would be categorized as 'Under -20', 'Under -10', 'Under 0’, ‘Under 10’, ‘Normal', 'Over 30'.   

Deciding on how to represent geographic patterns – Another challenge was to determine how to represent the geographical region to be correlated with accident rate and severity.  The dataset provides many different forms of location data, such as address, city, state, time zone, latitude and longitude.  Ultimately, we decided to use State as the geographical location to base our analysis as we were also able to cross-reference this information with the population of each state to compare the number and severity of accidents to each state’s population.  

Time series analysis – Since our dataset spans over the course of several years, we wanted to explore the idea of seasonality, but we had to find a simple method to represent the seasonal patterns in the data.  In the end, we decided to plot a bar graph that aggregates the number of accidents for each month over the course of three years.  This graph is a straightforward way to show both the number of accidents per month each year, as well as the total accidents for each month over the three-year period. 

 

Conclusions: What did you learn about your dataset? 

Through our analysis of the accident data, we came across many interesting and sometimes surprising results:   

Important predictive features:  Our initial exploration of the attributes that are most predictive of accident severity showed that the majority of important features (8/10) are related to weather conditions, such as humidity and temperature.   

Expected results from weather patterns:  A deeper analysis of certain weather conditions shows some patterns that are expected and match our hypotheses, such as an increase in accident severity when the temperature is at its lowest (-20 degrees Celsius) or when the precipitation is most severe (heavy or extreme amounts of rainfall).  

Some surprising observations:  However, we also encountered some unexpected results in the data.  For example, with regard to visibility, the most severe accidents actually occurred on mildly clear or clear days.  We speculate that this might be because drivers are not as cautious on days where visibility is not affected, leading to faster driving speeds that would result in more severe accidents.   

Effect of road and traffic design:  On the other hand, the design of the road and traffic, such as whether a traffic signal is present, is mostly predictive of whether accidents are more likely to occur instead of how severe an accident will be when it does occur. 

Geographic factors:  An exploration of geographic factors shows that states with the highest number of population (ex. California, Texas and Florida) also have the highest number of accidents.  Interestingly, when we looked instead at the severity of the incidents, some states with a comparatively lower population (ex. Georgia, Missouri, Iowa) actually recorded a greater percentage of high severity accidents.   

Seasonal patterns:  Finally, because our data spanned several years (2016-2019), we were able to explore patterns related to seasonality.  The results showed that as expected, there were more accidents when the temperature starts to decrease and daylight is reduced, beginning in October.  However, it was surprising to note that there was also a large increase in the number of accidents in August compared to the previous months – we have provided some speculations, but further study will need to be done to determine what factors are involved in this unexpected observation. 

 
