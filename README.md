# Loud Numbers sample datasets

A collection of time-series datasets suitable for practising data sonification techniques.

## Temperature anomalies

- **temps_y:** Yearly means, 1880-2021 (ascending trend, some noise)
- **temps_m:** Monthly means, Jan 1880-Dec 2021 (ascending trend, noisy)

Land-surface average anomaly results produced by the Berkeley Earth averaging method. Temperatures are in Celsius and reported as anomalies relative to the Jan 1951-Dec 1980 average: 8.59°C +/- 0.06°C.

**Source:** Yearly and monthly means of [Berkeley Earth daily TAVG](http://berkeleyearth.lbl.gov/auto/Global/Complete_TAVG_daily.txt) full dataset.

## Sunspots

### sunspots_y

Yearly mean total sunspot number, 1700-2021 (trend cyclical every 11 years with some noise)

**Data description:**
Yearly mean total sunspot number obtained by taking a simple arithmetic mean of the daily total sunspot number over all days of each year. (NB: in early years in particular before 1749, the means are computed on only a fraction of the days in each year because on many days, no observation is available).
A value of -1 indicates that no number is available (missing value).

**Error values:**
The yearly standard deviation of individual data is derived from the daily values by the same formula as the monthly means:
sigma(m)=sqrt(SUM(N(d)*sigma(d)^2)/SUM(N(d)))
where sigma(d) is the standard deviation for a single day and N(d) is the
number of observations for that day.

The standard error on the yearly mean values can be computed by:
sigma/sqrt(N) where sigma is the listed standard deviation and N the total number of observations in the year.
NB: this standard error gives a measure of the precision, i.e. the sensitivity of the yearly value to different samples of daily values with random errors. The uncertainty on the mean (absolute accuracy) is only determined on longer time scales, and is thus not given here for individual yearly values.

**Contents:**

- Column 1: Gregorian calendar year (mid-year date)
- Column 2: Yearly mean total sunspot number.
- Column 3: Yearly mean standard deviation of the input sunspot numbers from individual stations.
- Column 4: Number of observations used to compute the yearly mean total sunspot number.
- Column 5: Definitive/provisional marker. A blank indicates that the value is definitive. A '*' symbol indicates that the yearly average still contains provisional daily values and is subject to a possible revision.

### sunspots_m

Monthly mean total sunspot number, January 1749-June 2022 (trend cyclical every 11 years, noisy)

<https://github.com/loudnumbers/sonification-data>
Monthly mean total sunspot number obtained by taking a simple arithmetic mean of the daily total sunspot number over all days of each calendar month. Monthly means are available only since 1749 because the original observations compiled by Rudolph Wolf were too sparse before that year. (Only yearly means are available back to 1700)
A value of -1 indicates that no number is available (missing value).

**Error values:**
The monthly standard deviation of individual data is derived from the daily values by: sigma(m)=sqrt(SUM(N(d)*sigma(d)^2)/SUM(N(d)))
where sigma(d) is the standard deviation for a single day and N(d) is the
number of observations for that day.
The standard error on the monthly mean values can be computed by:
sigma/sqrt(N) where sigma is the listed standard deviation and N the total number of observations in the month.

NB: February 1824 does not contain any daily value. As it is the only month without data after 1749, the monthly mean value was interpolated by R. Wolf between the adjacent months.

**Contents:**

- Column 1-2: Gregorian calendar date (Year, Month)
- Column 3: Date in fraction of year for the middle of the corresponding month
- Column 4: Monthly mean total sunspot number.
- Column 5: Monthly mean standard deviation of the input sunspot numbers from individual stations.
- Column 6: Number of observations used to compute the monthly mean total sunspot number.
- Column 7: Definitive/provisional marker. A blank indicates that the value is definitive. A '*' symbol indicates that the monthly value is still provisional and is subject to a possible revision (Usually the last 3 to 6 months)

**Source:** [WDC-SILSO, Royal Observatory of Belgium, Brussels](https://www.sidc.be/silso/datafiles). Accessed 4 July 2022.

## Same-sex marriage

- **marriage:** % of US adults who support / oppose same-sex marriage, by year 2001-2019 (two opposing trends: support increases while opposition decreases)

**Source:** [Pew Research Center](https://www.pewresearch.org/religion/fact-sheet/changing-attitudes-on-gay-marriage/). Published May 14 2019. Accessed 4 July 2022.

## US recessions

- **recessions:** Various US economic data from Q1 1968 to Q1 2020 (various trends: binary on/off (recessions), spiky (indexes), rising (dow jones)). See [`recessions_about.csv`](https://github.com/loudnumbers/sonification-data/blob/main/recessions_about.csv) for details and sources of different variables.

## Brexit

**brexit:** Support and opposition to Brexit among the British public over time.

**Source:** [YouGov](https://yougov.co.uk/topics/politics/articles-reports/2022/11/17/one-five-who-voted-brexit-now-think-it-was-wrong-d), Published and accessed 17 November 2022.
