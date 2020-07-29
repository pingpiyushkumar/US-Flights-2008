### Communicating Data Findings: US Flights (2008)
Author: Piyush Kumar

### Introduction:  

Have you ever been stuck in an airport because your flight was delayed or cancelled and wondered if you could have predicted it if you'd had more data? 

Let's dig into one such dataset that reports flights in the United States, including carriers, arrival and departure delays, and reasons for delays, from October 1987 to April 2008. This is a [large dataset](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/HG7NV7), there are nearly 120 million records in total, and takes up 1.6 gigabytes of space compressed and 12 gigabbytes when uncompressed. <br>
Due to computational resource limitations, I'll be will be using the data for the year 2008 only, which is around 7 million rows.  

[Another Source for this Data](https://www.kaggle.com/vikalpdongre/us-flights-data-2008)

#### The Data: 

- <b>Flights Data:</b>  The data consists of flight arrival and departure details for all commercial flights within the USA, for the year 2008.  
- <b> Airports Data:</b> This describes the locations of US airports, with the fields:the international airport abbreviation code, name of the airport, city and country in which airport is located, and the latitude and longitude of the airport.
- <b> Carriers Data:</b> This contains listing of carrier codes with full names.
- <b> Planes Data:</b> It contains information on plane manufacturers, model, aircraft type, engine type etc.

### Summary of Findings:

- There is clear differentiation of flight quantity among airlines. Most Popular airlines in terms of flight quantity are Southwest Airlines Co, American Airlines Inc, Skywest Airlines Inc, American Eagle Airlines Inc. and so on. And, the Aloha Airlines operates the least no. of flights in the US.
- There is clear differentiation of flight quantity among airports also. Most Popular airports in terms of flight quantity are William B Hartsfield-Atlanta Intl, Chicago O'Hare International, Dallas-Fort Worth International, Denver Intl and so on.
- There is clear difference of flights and airports quantity among US States, with states CA,TX,FL,IL,GA,NY handlinng most of the flight traffic.
- State AK has most no. of airports but a tiny no. of flights are scheduled here.
- There is no difference in the flight quantity over days of the month except at the end of the month, especially on the 31st where the flight quantity is nearly the half of any other day of the month.
- Further, flight quantity is equally distributed over day of the week, though sees a slight dip on Saturday and Sunday.
- Month of July seems to have highest flight quantity and it decreases thereafter in the later months of the year.
- We have a right skewed distribution for flight distance, with mode at around 300 km, mean at around 700 km and median at around 500 km.
- Airtime is right-skewed and the shape of distribution is similar to that of distance, with mode at around 75 minutes, mean at around 120 minutes and median at around 100 minutes.
- Departure delay of flights looks like a right-skewed distribution with mode at around 0 minute, mean at around 10 minutes and median at around 5 minutes.
- We have a nearly a uniform distribution for arrival delay of flights with center at 0 minute.
- Also, the distribution tails towards negative values as well i.e many flights have arrived earlier than scheduled.
- We're again looking at a nearly uniform normal distribution with center at less than 0 minute (which is expected from the airlines).
- Most of the airlines reach most of the states.
- Almost all of the airports have flights scheduled from all of the airlines.

- We have strong positive correlation between Distance and Airtime as expected.
- From the slope of the regression line, it can be inferred that, weather delay adds to the arrival delay more than any other delay factors, this effect is even greater in case of departure delay.

### Insights:

- Almost 60% of the flights run after Mid-day (12:00PM) and 40% before Mid-day.
- 1,37434 flights (1.96%) were cancelled in the year 2008, weather being the highest contributing factor (39.53%), followed by Carrier, NAS (National Airspace System) and Security.
- Day 4 of the month appears to have the most cancellations, while day 24 of the month has least cancellations.
- Also, the second half of the month have lesser cancellations than the first half of the month.
- There is clear differentiation of flight cancellations over months, with month of Feb having the highest cancellations and Oct the least. And the the differnece is big upwards of 15000 flights cancellations.
- In case of day of the week, weekdays has more cancellations that weekends. Friday sees the most cancellations and Saturday the least.
- Airlines with highest cancellations: American EAgle Airlines Inc, American Airlines Inc, Skywest Airlines Inc. and so on.
- As we can see, airports with highest flight cancellations: Chicago O'Hare International, Dallas-Fort Worthe International, LaGaurdia and so on.
- Most flights run after Mid-day, they also get cancelled the most in the same proportion as that of the flights that run before mid-day.
- Security delay has the least frequency of occurence and almost no or weaker effect on other numerical variables of the flight.
- NAS delay add more to delay_elapsed than any other delay factor.
- We might have a simpson's paradox here, as National Airspace System (NAS) delay happens more frequently than weather or security delay.

