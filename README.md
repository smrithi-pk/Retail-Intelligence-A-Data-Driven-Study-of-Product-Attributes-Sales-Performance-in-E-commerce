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

**Dress Sales Dataset**: A time-series dataset tracking the sales volume for each Dress_ID across 23 specific dates in 2013.
Key Features: Daily sales counts per item.

These datasets are linked via a common unique identifier, Dress_ID. To perform the analysis, the time-series sales data was aggregated into a single Total_Sales metric and merged with the attribute data to create a comprehensive "Retail Intelligence" master file.

## **Data Cleaning & Preprocessing** :

To ensure high-quality insights, the raw data underwent a rigorous cleaning process:

* Handling Missing values: Handled missing values in critical columns like Material, FabricType, and Price using 'Unknown' because there are more null values and null values in rest column are handled using mode imputation .
* Data Standardization: Corrected inconsistent labeling (e.g., standardizing "low" vs. "Low" in Price categories). Checked all the mispelled words and corrected it. Performed de-duplication to remove redundant entries and ensure data uniqueness.
* Feature Engineering: Created a Total_Sales metric by aggregating time-series sales data across all recorded dates. So, we can understand how much sales happened for each dress
* Data Integration(Merging): Merged the Attribute Dataset and Sales Dataset into a unified master dataframe using common product attributes.

## **EDA & Visualizations** :

I performed Exploratory Data Analysis (EDA) using different visualizations to uncover hidden patterns:

* Distribution Analysis: Histograms and Box Plots to understand price spread and sales outliers.
* Categorical Performance: Bar Charts and Count Plots to identify the most popular Styles and Materials.
* Relationship Mapping: Scatter Plots used to visualize the correlation between Price, Rating, and Total_Sales.
* Violin Plots: To compare sales distribution across different Recommendation statuses.
* Heatmaps: A correlation heatmap was used to identify which numerical features move together (e.g., how Rating affects Recommendation probability).

## **Key Insights & Findings** :

* The "Sweet Spot" Strategy: High sales are not driven by "5-star" ratings alone. The highest volume occurs in Average-Priced items with a 4.0+ Rating.
* Recommendation Power: Products flagged as "Recommended" by the platform's algorithm see a significantly higher sales velocity compared to non-recommended items, regardless of price.
* The Autumn Sales Cliff: The data reveals a sharp decline in sales during the Autumn season. This is linked to a Material Mismatch, where Summer fabrics (Chiffon/Thin Cotton) are overstocked during cooler months.
* Hero Materials: Cotton, Polyester, and Chiffon remain the dominant revenue drivers, but their success is highly dependent on matching the right Neckline and SleeveLength to the current season.
