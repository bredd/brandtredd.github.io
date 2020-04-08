---
title: COVID-19 (Coronavirus) Data
layout: default
---
Johns Hopkins University posts COVID-19 data daily [2019 Novel Coronavirus COVID-19 (2019-nCoV) Data Repository by Johns Hopkins CSSE](https://github.com/CSSEGISandData/COVID-19) (as of February 2020). I wrote an open source program to download the data, filter and aggregate, and then store in a format that is convenient for analysis using tools like [Microsoft Excel](https://www.microsoft.com/microsoft/excel) or [Tableau](https://www.tableau.com/).

The following data are updated most days. Using the program, you can retrieve the data yourself with different filters and aggregation. See below for details.

* World Data, broken down by country: [COVID-19-Time-Series-World.csv](COVID-19-Time-Series-World.csv)
* US Data, broken down by state and county: [COVID-19-Time-Series-US.csv](COVID-19-Time-Series-US.csv)
* Updated: {% include_relative COVID-19-Updated.txt %}

<hr/>

The program and information are [On Github Here](https://github.com/FileMeta/ReadAndConvertCovid19Data) and you can dowload the executable [Here](https://github.com/FileMeta/ReadAndConvertCovid19Data/releases)

More details on how to use the program will be posted shortly. For now, understand that it's a command-line program and if you run it with the following command-line it will print the help text:

```
ReadAndConvertCovid19Data -h
```


