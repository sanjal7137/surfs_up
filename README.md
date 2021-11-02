# surfs_up


							                                                                                  Surfs_Up

> Overview of the statistical analysis
     Performing analysis on weather data to find out how much possibility for new business to succeed. Exploring weather data to analyze temperature and rain in Hawaii month wise and year wise and find out how much it affects it new business “surf and shake”.
> Results
  The three key differences in weather between June and December as follow:-
  
	* We have approximately 200 more counts in our data for June compare to December.
	* Average temperature in June is around 75 with minimum is 64 and maximum is 85 and Average temperature in December is around 71 with minimum is 56 and maximum is 83. so here more variation in minimum temperature compare to variation in maximum temperature.
	* Variation in min temp. is 8 and maximum temp variation is only 2 for month June and December temperature data
	* As per analysis not too much temperature variation in summer (June) and winter (December) 

>Summary:
     As per analysis we can say that climate in summer and winter is almost same but for ice cream business we can say that weather is cool in whole year we can say that surf and shake is will not be 100 % successful. 
     We can analyze based on precipitation for summer and winter as well as previous year using following query.
	
query that filters the Measurement table to retrieve the precipitation for the month of June.
results = session.query(Measurement.date, Measurement.precipitation).filter(extract('month', Measurement.date) == 6).all()

query that filters the Measurement table to retrieve the precipitation for the month of December.
results = session.query(Measurement.date, Measurement.precipitation).filter(extract('month', Measurement.date) == 6).all()

query to retrieve the last 12 months of precipitation data
prev_year = dt.date(2017, 8, 23) - dt.timedelta(days=365)
results = session.query(Measurement.date, Measurement.prcp).filter(Measurement.date >= prev_year).all()



