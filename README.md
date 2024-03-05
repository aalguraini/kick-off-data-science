# kick-off-data-science
Airbnb Data Analysis
This project provides a comprehensive analysis of Airbnb listings in Boston. It uses data from the Airbnb dataset, which includes listings, calendars, and reviews, to perform a detailed exploration and visualization. The analysis focuses on understanding the most common words in reviews and visualizing the distribution of Airbnb properties in Boston based on their location, property type, and price.

Prerequisites
Before you run this script, make sure you have the following packages installed:

NumPy
pandas
NLTK
Plotly
re (Regular Expression, included with Python)
You can install these packages using pip:


pip install numpy pandas nltk plotly
Additionally, you need to have the NLTK stopwords dataset downloaded. This script will attempt to download it if it's not already present.

Running the Script
To run the script, simply execute it in your Python environment. Ensure that the Airbnb dataset (calendar.csv, listings.csv, reviews.csv) is located in an archive directory within the same directory as the script.

python airbnb_analysis.py
Description of the Code
The code performs the following operations:

Data Loading: Reads the Airbnb calendar, listings, and reviews CSV files into pandas DataFrames.

Data Preprocessing and Analysis:

Combines all review comments into a single string.
Preprocesses this string by lowercasing, removing punctuation, and splitting into words.
Filters out English stopwords.
Counts the frequency of each remaining word and identifies the most common words.
Data Visualization:

Uses Plotly to create a scatter mapbox visualization of the Airbnb listings.
Plots listings based on their longitude and latitude, colored by property type and sized by price.
The map is styled using the 'open-street-map' style and is interactive.
Make sure to replace geo_df in the plotting section with the appropriate DataFrame that contains longitude, latitude, property_type, and price columns. This portion of the code may require modification depending on the structure of your listings.csv file or if geo_df is not defined elsewhere in the provided code snippet.

Note
This README assumes that geo_df is a DataFrame created from the listings.csv file or through some other means not shown in the provided code snippet. You will need to preprocess or prepare listings_df to create geo_df with the necessary columns (longitude, latitude, property_type, price) for the visualization part of the code to work correctly.
