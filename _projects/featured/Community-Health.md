---
title: "Community Asset Framework"
description: "Conceived by Dr. David Dubois, the community asset framework provides a snapshot of county health along three dimensions: Nature, Society, and Economy."
category: featured
github_link: 
technologies:
  - R
  - PowerBI
  - Database
  - Web Scrapping
image: /assets/images/community-dashboard.png
---

# Project Overview
The primary objective is to provide a dashboard for each County in every state of the United States that shows the health of the county in comparison to every other county in the state. 

## Features
- Data Sources: Multiple sources including [census data](https://data.census.gov/), [county health rankings](https://www.countyhealthrankings.org/health-data), [bureau of labor statistics](https://www.bls.gov/), [bureau of economic analysis](https://www.bea.gov/), and other public databases providing health inforamation.
- Modeling: Web scrapping, API calls, Data Wrangling, Database, Dashboards
- Analysis: R, PowerBI

## Technologies Used
The analysis currently uses R, PowerBI, and web scrapping.

## Implementation
Data is currently being gathered from multiple sources through API calls, direct downloads, and web scrapping. We then perform data wrangling that includes cleaning, imputing, and organization of the data for further analysis. Next, we intend to create an automatic flow to compile the data, update a database, and create the metrics along the three dimensions of Nature, Society, and Economy. These will then be used to create a dashboard that will be presented to users in each County. 

## Results

A sample dashboard is shown below, along with a sample code book detailing the construction of the metrics.

![Sample Health Index](https://github.com/user-attachments/assets/c583c8de-20ca-45ef-b52f-e99206298f26)

![Sample Metric](https://github.com/user-attachments/assets/ad5fd718-bd5f-4ea8-8b41-0fe3ef13d40e)


## Future Improvements

We are currently in the process of Data Wrangling, and hope to complete this project my February of 2025.

