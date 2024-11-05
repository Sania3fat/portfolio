---
title: "KNFC: Sales and Pricing Model Dashboard"
description: "Using POS data, created dashboards using Tableau for Kent Natural Food Cooperative (KNFC) that provided insights on top sellers and
slow-moving items, leading to inventory cost savings, improved sales predictions, and strategic enhancements. Inventory turn-overs were optimized, reducing holding and shortage costs, and achieved a profit of $16,279.88 in Packaged Goods through improved predictive algorithms for sales demand and inventory management."
category: featured
github_link: https://github.com/Sania3fat/portfolio/tree/main/Dashboard
technologies:
  - R
  - Tableau
  - ER diagrams
image: /assets/images/knflogo.png
---

# Project Overview
The primary objective was to analyze POS data to provide insights into Sales, Inventory, and cash flow of goods at KNFC.

## Features
- Data Sources: POS data
- Modeling: Text analysis, Descriptive, Predictive, and Inventory Management
- Analysis: R,  Tableau, ER diagrams, Database

## Technologies Used
The analysis currently uses R, and Tableau.

## Implementation
The primary data was from a point-of-sale system. We collected data for one-year of sales. There were several issues related to data integrity and validity, and few are listed below:

- The data was categorized by departments. Several departments, for example, Produce, did not differentiate between products in the POS system. So, it was difficult to determine which item was indeed selling.
- The current inventory in the POS did not match the physical inventory in the store
- There was no universal key, so we had to map products by product name (text field) across the various data tables. Some data tables had UPC code, but others had none. Some had product ID, but others, like in Produce, had none. So, we used **text analysis** to create a unique key to match items across data tables. 

## Results

Our analysis and results were presented to management in the form of a dashboard that we created in Tableau. The following screenshots show part of our dashboard. Our presentation was **Commended by the KNFC board, and received excellent feedback for timely completion, clear presentation, engaging
storytelling, and effective analysis.**

![Comparitive analysis of Cost versus Selling Price across Departments](https://github.com/user-attachments/assets/322789b3-ae8b-4273-96ef-d55f59fc97a3)


![Inventory Optimization](https://github.com/user-attachments/assets/829a59fc-b2f6-4b8e-a832-1a9eec3f67a8)


![Inventory Optimization - Cont.](https://github.com/user-attachments/assets/58d6ded4-c9fb-4f24-94f1-a64eb0e6b4b3)


## Future Improvements

We are currently in the process of implementing some of our recommendations at KNFC.


