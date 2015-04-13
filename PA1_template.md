# Reproducible Research: Peer Assessment 1


## Loading and preprocessing the data

Unzip and load the csv file


```r
unzip(zipfile="activity.zip")
act_data <- read.csv("activity.csv")
```

## What is mean total number of steps taken per day?
Load needed libraries

```r
library(ggplot2)
```

```
## Warning: package 'ggplot2' was built under R version 3.1.3
```
Make a histogram of the total number of steps taken each day

```r
totnum.steps <- tapply(act_data$steps, act_data$date, FUN=sum, na.rm=TRUE)
# qplot(totnum.steps, binwidth=1000, xlab="Total number of steps taken each day")
hist(totnum.steps,main='Total number of steps per day',xlab='Total number of steps per day',col='blue')
```

![](PA1_template_files/figure-html/unnamed-chunk-2-1.png) 

Calculate and report the mean and median of the total number of steps taken per day

```r
mean(totnum.steps, na.rm=TRUE)
```

```
## [1] 9354.23
```

```r
median(totnum.steps, na.rm=TRUE)
```

```
## [1] 10395
```


## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
