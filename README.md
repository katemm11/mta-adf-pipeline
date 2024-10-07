# MTA Sample Pipeline

This pipeline aggregates data from two sources in the MTA Open Data Portal: MTA Wifi Locations (https://data.ny.gov/Transportation/MTA-Wi-Fi-Locations/pwa9-tmie/about_data) and Hourly Ridership Data (https://data.ny.gov/Transportation/MTA-Subway-Hourly-Ridership-Beginning-February-202/wujg-7c2s/about_data).

I stored the Wifi data in a CSV in Azure Data Lake Storage, and then created a Databricks notebook to combine it with the hourly ridership data. I accessed the hourly ridership data directly rom the API endpoint. In my Databricks notebook I joined the two datasets on the common column "station_complex" and used Pandas to manipulate the data in order to create a new colu
