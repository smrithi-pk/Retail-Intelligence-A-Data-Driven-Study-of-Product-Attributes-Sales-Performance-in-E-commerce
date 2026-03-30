# **Retail-Intelligence-A-Data-Driven-Study-of-Product-Attributes-Sales-Performance-in-E-commerce**
This project delivers a data-driven Retail Intelligence & Procurement Roadmap designed to transform raw e-commerce apparel data into actionable business strategy. By analyzing over [Insert Number, e.g., 500+] product records, the analysis identifies the 'Golden Success Formula'—the specific intersection of material, price, and customer sentiment that drives maximum sales volume. The study reveals critical inefficiencies, such as the 'Autumn Sales Cliff,' and provides a precise framework for inventory optimization, helping businesses shift from reactive guessing to proactive profit management. Through diagnostic analytics and seasonal trend mapping, this project offers a scalable methodology to reduce 'Dead Stock' and maximize inventory turnover, paving the way for future predictive machine learning integration.

## **Objective** :

* To identify which physical attributes (Material, Style, Price) drive high sales volume in the e-commerce sector.
* To determine if Customer Ratings and System Recommendations significantly contribute to an increase in sales.
* To identify which types of fabric materials perform best during different seasons and evaluate if a seasonal sales strategy is effective for the business.

## **Dataset Overview** :

Dataset is taken from UCI Machine Learning Repository - https://archive.ics.uci.edu/dataset/289/dresses+attribute+sales
The analysis is based on two primary datasets containing information on retail dress inventory and performance:

**Attribute Dataset**: Contains categorical and descriptive features for 500 unique dress designs.

Key Features: Style, Price, Rating, Size, Season, NeckLine, SleeveLength, and Material composition.
Purpose: To define the physical characteristics and market positioning of each product.

**Dress Sales Dataset**: A time-series dataset tracking the sales volume for each Dress_ID across 23 specific dates in 2013.

Key Features: Daily sales counts per item.
Purpose: To provide the raw performance metrics needed to calculate total sales velocity and identify trends.

These datasets are linked via a common unique identifier, Dress_ID. To perform the analysis, the time-series sales data was aggregated into a single Total_Sales metric and merged with the attribute data to create a comprehensive "Retail Intelligence" master file.
