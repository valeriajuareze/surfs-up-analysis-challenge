# Surfs Up Analysis Challenge
## Project Overview

W. Avy  wants more information about temperature trends before opening the surf shop. Specifically, he wants temperature data for the months of June and December in Oahu, in order to determine if the surf and ice cream shop business is sustainable year-round.

## Results

### Statistics in June 

![image](https://user-images.githubusercontent.com/108365182/187239340-8a9fde72-c989-478a-8fe2-aafa58342e75.png)

### Statistics in December

![image](https://user-images.githubusercontent.com/108365182/187239406-bacb6c47-e5eb-4ff7-b556-24fa99474891.png)

There is no big difference between the temperatures in June and December, but there are three main differences: 

- First, the temperature in December tends to differentiate more than in June, because the standard deviation, which indicates us the data dispersion, is higher. 

- Also, December has lower temperatures, which we can deduce it because of the mean, and min temperatures, but also, because the 50% of the month has lower temperatures than 71.0 F.

- Finally, we can deduce that in June the minimun temperature is almost 10 F higher than December, which is a big climate difference. 

### Summary

According to the previous results, we can conclude that June and December can be a quite difficult months for the surf shop, this, because the temperature tend to differentiate a lot in both months, which can have big consequences, or good benefits, that we will not know until the moment. My first recommendation is prepare for both months. Fortunately, after june, the most important months in the year come, so the surf shop could benefit for that. And, finally my last recommendation is to analize deeper the data temperature for both months. Here are two more queries that can help for the data analysis:

***1.***

december_temperature=session.query(Measurement.date,Measurement.tobs).filter(extract('month', Measurement.date) == 12).order_by(Measurement.date).filter(Measurement.tobs>=70.0).all()

***2.***

june_temperature=session.query(Measurement.date, Measurement.tobs).filter(extract('month', Measurement.date) == 6).order_by(Measurement.date).group_by(Measurement.tobs).all()
