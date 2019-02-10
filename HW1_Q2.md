HW1 Q2
================

Data visualization 2: flights at ABIA
-------------------------------------

In this question, we explore the best time to fly to and depart from Austin-Bergstrom Interational Airport in order to minimize delay.


</br>

##### data-preprocessing

-   new variable 'type': label the flight type as 'Departure' from or 'Arrival' at Austin.
-   new variable 'delaytime': use the departure delay 'DepDelay' as the delay time for departure flights, and arrival delay 'ArrDelay' for arrivals.
-   modify 'delaytime': normalize the delay time to 0 for early departures and arrivals (delay time being negative), assuming that people only care about delays.


</br>

### Seasonality of delays - best time of the year to travel from & to Austin?


</br>

##### data-processing for seasonality

-   new variable 'date': format the month and date into one variable.
-   calculate the average delay time of departure & arrival flights seperately, across all dates of the year.

##### plotting

-   plot the average delay time for two types of flights across all dates.
-   add the trend line for departure and arrival flights (method: lasso)


</br>

![](HW1_Q2_files/figure-markdown_github/unnamed-chunk-4-1.png)



</br> </br>

-   plot the trend line for all flights from and to Austin and zoom in to see the details.


</br>

![](HW1_Q2_files/figure-markdown_github/unnamed-chunk-5-1.png)


</br>


</br>

![](HW1_Q2_files/figure-markdown_github/unnamed-chunk-6-1.png)


</br>

We see that throughout the year, arrival flights at Austin are expected have longer delays than departure flights from Austin. Overall, fall (from September to November) is the best season of the year to minimize delays whereas December is the worst month of the year.


</br>

### Delays in a day - best hour of the day to travel from & to Austin?


</br>

##### data-processing for delays in a day

-   new variable 'time': use the scheduled departure time 'CRSDepTime' as the time for departure flights, and scheduled arrival time 'CRSArrTime' for arrivals.

-   new variable 'hour': round the time to the nearest hour.
-   calculate the average delay time of departure & arrival flights seperately, across all hours of the day.

``` r
summary(ABIA$time)
```

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##       5    1040    1430    1416    1800    2359


</br>

##### plotting

-   plot the average delay time for two types of flights across all hours.
-   add the trend line for flights departed from and arrived at Austin (method: lasso).


</br>

![](HW1_Q2_files/figure-markdown_github/unnamed-chunk-10-1.png)


</br>

We see that average delay time increases from 9:00 to 24:00, and reaches peak at midnight. Morning (5 am - 10 am) might be the best time of the day to minimize delays.

Overall, the best way to minimize delay in Austin-Bergstrom Interational Airport is to depart from Austin in the morning of October!



</br> </br>
