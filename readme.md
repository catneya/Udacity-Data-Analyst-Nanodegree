# Exploratory Analysis of Ford GoBike Data
## by Adam Catney


## Dataset
This dataset consists of information for the Ford GoBike Program run in San Francisco throughout February 2019. For this month alone we see 183,412 trips.
Some of these columns can be discarded such as the latitude and longitude. 
Others will need cleaning and tidying such as the timings which will be converted to datetime format and the user_type column which I will change to a category data type.
There are also a number of blanks, 8265 under the Birth Year and Gender columns. These are to be removed.
I will also add new columns for breaking down the start time of the trips into Hour of the Day(1-24), Day of the Month (1-28) and Weekday (Mon-Sun). These will be useful later.
The Dataset I used can be found [here](https://video.udacity-data.com/topher/2021/May/6090815e_201902-fordgobike-tripdata/201902-fordgobike-tripdata.csv)


## Summary of Findings

### Subscribers vs Customers
Most of those who take part in the scheme are Subscribers with the Customers making up less than 10% of them. 
Overall there are also far more men than women taking part in the scheme. 
When looking more closely at this we also see men make up majority for both Subscribers & Customers. 
However despite this large disparity in volume we also see that proportionately both genders tend to be subscribers by about the same amount. 

Male members, in particular subscribers, are the oldest group while females have the lowest median age. 
Males across both user types have the broadest range between their 1st and 3rd quartile.

Consumers tend to take longer trips which seems to indicate that while Subscribers use the bikes for day to day commuting while consumers are using them for more ad hoc needs, likely including leisure or perhaps even visitors to the City.

### Trips throughout the Day & Month
Day-to-Day the Customers don't tend to see much variance throughout the week. Meanwhile Subscribers use the bikes for trips mostly throughout the weeks with a significant drop-off during the weekend.

Throughout the month we see peaks and troughs however most of the drop-offs seem to coincide with the weekend which aligns with what we saw elsewhere. There are some other days where trips aren't common but we don't have enough data to say how, these could simply be days when the weather is too poor for going out on the bike.

Gender appears to be insignificant when it comes to Male & Female members throughout the weekday and month day data, with them sharing the same peaks and troughs but with Males 
being obviously more numerous due to the earlier mentioned difference in membership between the two genders.

The busiest time of day is around 08:00, likely when people are commutting to work or school, with the slowest time being in the early AM around 02:00 which makes a lot of logical sense.

### Ages of Users
The most significant group of members are those who where born in the latter half of the 80's to the mid-90's. Men, on average, tended to be older with the Male Subscribers having the oldest members.

We also see that the majority of trips are undertaken by members in their 20's & 30's with the overall mean age of members being 34.

The elderly members tend to go on shorter trips.

### Bike Share For All Program
The Bike Share Program is in the majority when it comes to users with only 9.9% of trips being part of this scheme. We also see that there are 0 Customers that take part of this scheme which may indicate that it is not open to non-Subscribers.


## Key Insights for Presentation

### Bike Trips over Time
I will be using two visualisations to show the Bike Trips and how their volume varies over time. The two I will use will show the trend over the month and the other throughout 24 hours.
These graphs are very easy to read and I think they make for a good addition to the Explanatory detail, however I will be removing the "Other" gender option from the data used in the graph.
This is because the "Other" volumes are so low that all we see is a line which does not offer any insight beyond the Other volumes being low which we already know and will show later.

### Typical Duration of Bike Trips
I will use a simple histogram, which I have put through a Log Transformation, to make it very easy to read and understand for someone coming new to the slideshow.
The only addition I plan to make to this visual is a line to show the overall mean/average Trip Duration. This is because otherwise a viewer might mistake the peak of the distribution curve as the mean.


## Resources/References Used
Drop Duplicates - https://note.nkmk.me/en/python-pandas-duplicated-drop-duplicates/
Unique Values from Column - https://cmdlinetips.com/2018/01/how-to-get-unique-values-from-a-column-in-pandas-data-frame/
Setting Graph Colours as a Variable - https://julienbeaulieu.gitbook.io/wiki/sciences/programming/data-analysis/data-visualization/univariate-exploration-of-data/bar-chart
Extracting Hour from DateTime Column - https://stackoverflow.com/questions/53045867/extracting-the-hour-from-a-time-column-in-pandas
Pie Charts - https://matplotlib.org/3.1.1/gallery/pie_and_polar_charts/pie_features.html
Boxplots (Seaborn) - https://seaborn.pydata.org/generated/seaborn.catplot.html
Labels & Titles - https://stackoverflow.com/questions/55767312/how-to-position-suptitle and https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.suptitle.html
Day Order for Graph - https://stackoverflow.com/questions/47255746/change-order-on-x-axis-for-matplotlib-chart