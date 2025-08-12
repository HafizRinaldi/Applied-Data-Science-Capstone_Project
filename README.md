Predicting SpaceX Falcon 9 First-Stage Landing Success
A comprehensive data science project to analyze and predict the success of SpaceX's reusable rocket landings. This repository contains the notebooks, data, and analysis for the IBM Data Science Professional Certificate capstone.
Table of Contents
Project Overview
Key Questions Addressed
Methodology Workflow
Key Findings & Conclusions
Technologies Used
Project Overview
This repository contains the complete end-to-end data science capstone project focused on predicting the success of SpaceX Falcon 9 first-stage landings. SpaceX advertises Falcon 9 launches at a significantly lower cost than its competitors, largely due to its ability to reuse the first stage. Therefore, accurately predicting landing outcomes is crucial for determining launch costs, assessing mission risk, and maintaining a competitive edge in the commercial space industry.
This project walks through every step of the data science workflow, from data acquisition and cleaning to exploratory analysis, interactive visualization, and predictive modeling.
Key Questions Addressed
What are the primary factors that influence the success or failure of a Falcon 9 first-stage landing?
How can we build a reliable machine learning model to predict these outcomes based on historical launch data?
Which classification model provides the best performance and is most suitable for this prediction task?
Methodology Workflow
The project follows a comprehensive data science workflow, broken down into five key stages:
Data Collection: Historical launch data was gathered from two distinct sources. The SpaceX REST API provided detailed, structured data for each mission. This was supplemented by web scraping the List of Falcon 9 and Falcon Heavy launches Wikipedia page using BeautifulSoup to capture a broader historical record. These sources were then merged into a single dataset.
Data Wrangling: The raw, combined data was rigorously cleaned and prepared for analysis. This involved handling missing values (e.g., imputing the mean for PayloadMass), filtering the dataset to include only Falcon 9 launches, and engineering the primary target variable, Class, where 1 signifies a successful landing and 0 signifies a failure. Categorical features like Orbit and LaunchSite were converted into a numerical format using one-hot encoding.
Exploratory Data Analysis (EDA): Initial patterns and insights were uncovered using SQL queries for targeted data aggregation and analysis. This was complemented by data visualization using Python libraries like Matplotlib and Seaborn to create scatter plots, bar charts, and line charts that revealed relationships between variables such as payload mass, orbit type, and launch success over time.
Interactive Visual Analytics: To allow for deeper, user-driven exploration, two interactive components were developed:
An interactive map using Folium to visualize the geographic locations of all launch sites, their proximity to coastlines, and the success/failure outcomes for each site.
A dynamic dashboard built with Plotly Dash featuring dropdowns and range sliders. This allows users to filter data by launch site and payload mass to see how these factors affect success rates in real-time.
Predictive Modeling: Several machine learning classification models (Logistic Regression, SVM, Decision Tree, KNN) were developed to predict landing success. The process included standardizing the feature data, splitting it into training and test sets, and using GridSearchCV to systematically tune hyperparameters for optimal performance. Each model was then evaluated on the unseen test data to determine its accuracy and reliability.
Key Findings & Conclusions
Based on the analysis, the following key conclusions were drawn:
Point 1: The success rate of Falcon 9 first-stage landings has steadily increased over time, demonstrating a clear learning curve and the positive impact of iterative technological improvements.
Point 2: Key determinants of landing success include the mission's orbit type (with high-energy orbits like GTO proving more challenging), the mass of the payload, and the launch site used.
Point 3: Machine learning models can predict landing outcomes with high accuracy. The most robust models achieved an accuracy of ~83.3%, providing a valuable tool for quantitative risk assessment and cost estimation.
Point 4: Interactive tools like the Folium maps and Plotly Dash dashboard are highly effective for exploring complex datasets and communicating findings to a broader, non-technical audience.
Technologies Used
Programming Language: Python
Data Manipulation & Analysis: Pandas, NumPy
Machine Learning: Scikit-learn
Data Querying: SQL
Web Scraping: BeautifulSoup
Data Visualization: Matplotlib, Seaborn
Interactive Visualizations: Folium, Plotly Dash
