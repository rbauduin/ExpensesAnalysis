# Expenses Analysis

This Jupyter notebook, using F# as code cells language, is meant to analyse expenses provided in a CSV file at the location `/notebooks/expenses.csv`. 
I run it with IFSharp in a docker container. [Having built the docker image](https://github.com/fsprojects/IfSharp#running-inside-a-docker-container) 
(and having named it ifsharp, ie using `-t ifsharp`), I mount my local directory holding the `expenses.csv` file in the container with the command

docker run -v /my/path/to/Documents/ipython:/notebooks -p 8888:8888 ifsharp

The CSV file format handled is the one exported from the Android application [Hello Expense](https://play.google.com/store/apps/details?id=com.helloexpense&hl=en), 
but providing the exact same format from another app should work too. The lines of the csv file have to be of the format:

"date","Category","amount","currency","Note","CommaSeparatedTags"

For example

"21/1/2018","Other","38,72","€","ISP","Home,Internet"
