## The car_price_dataset.csv file is for EDA_1
## The Movie.csv file is for EDA_2 
I've analyzed the provided Jupyter Notebooks and generated a README file for each, summarizing their contents and key findings.

---

## **README for MultipleFiles/EDA_1_.ipynb**

### **Project Title: Car Price Dataset Exploratory Data Analysis (EDA)**

### **Overview**
This Jupyter Notebook (`EDA_1_.ipynb`) performs an exploratory data analysis on a car price dataset. The goal of this analysis is to understand the characteristics of the car market, identify trends, and extract meaningful insights from the data.

### **Dataset**
The analysis uses a CSV file named `car_price_dataset.csv`. This dataset contains various attributes of cars, including:
*   `Brand`
*   `Model`
*   `Year`
*   `Engine_Size`
*   `Fuel_Type`
*   `Transmission`
*   `Mileage`
*   `Doors`
*   `Owner_Count`
*   `Price`

### **Libraries Used**
*   `pandas` for data manipulation and analysis.
*   `numpy` for numerical operations.
*   `matplotlib.pyplot` for basic plotting.
*   `seaborn` for enhanced data visualizations.

### **Key Analysis and Findings**

The notebook addresses several specific questions about the car price dataset:

*   **Average Car Price:** The average price of all cars in the dataset is calculated.
    *   **Finding:** The average price of all cars in the dataset is $8852.96.

*   **Car Brand with Highest Average Price:** Identifies which car brand has the highest average price.
    *   **Finding:** Chevrolet has the highest average price.

*   **Most Common Fuel Type:** Determines the most frequently occurring fuel type.
    *   **Finding:** The most common fuel type is Electric.

*   **Cars with High Mileage:** Counts the number of cars with mileage greater than 200,000.
    *   **Finding:** 3290 cars have a mileage greater than 200,000.

*   **Transmission Type Distribution:** Shows the distribution of cars across different transmission types.
    *   **Finding:** The distribution of cars by transmission type is fairly even, with Manual (3372), Automatic (3317), and Semi-Automatic (3311) transmissions.

*   **Car Model with Highest Price:** Identifies the car model with the maximum price.
    *   **Finding:** The Toyota Corolla has the highest price at $18301.

*   **Average Price by Fuel Type:** Calculates the average price for each fuel type.
    *   **Finding:** Electric cars have the highest average price ($10032.22), followed by Hybrid ($9113.03), Diesel ($8117.34), and Petrol ($8070.56).

*   **Newer Cars Count:** Counts cars from the year 2020 or later.
    *   **Finding:** 1651 cars are from the year 2020 or later.

*   **Average Engine Size by Brand:** Computes the average engine size for each car brand.
    *   **Finding:** Engine sizes vary slightly across brands, with Kia having the largest average engine size (3.05) and Honda/Hyundai having the smallest (2.92/2.93).

*   **Car with Lowest Mileage:** Identifies the car with the minimum mileage.
    *   **Finding:** A Ford Explorer from 2006 has the lowest mileage (25).

*   **Correlation between Mileage and Price:** Calculates the correlation coefficient between mileage and price.
    *   **Finding:** The correlation between mileage and price is approximately -0.55, indicating a moderate negative correlation (as mileage increases, price tends to decrease).

*   **Cars with Multiple Owners:** Counts cars that have had more than 2 owners.
    *   **Finding:** 5944 cars have had more than 2 owners.

*   **Average Price by Year:** Determines the average price of cars for each release year.
    *   **Finding:** The average car price generally increases with newer model years, ranging from $5393.74 in 2000 to $12169.47 in 2023.

*   **Cars with Highest Number of Doors:** Identifies cars with the maximum number of doors.
    *   **Finding:** Many models across various brands have 5 doors, which is the maximum in the dataset.

*   **Average Mileage by Fuel Type:** Calculates the average mileage for each fuel type.
    *   **Finding:** Average mileage is relatively similar across fuel types, ranging from approximately 145,577 for Hybrid to 151,059 for Electric.

*   **Toyota Cars Count:** Counts the number of cars from the 'Toyota' brand.
    *   **Finding:** There are 970 cars from the Toyota brand in the dataset.

*   **Average Price of Automatic Transmission Cars:** Calculates the average price for cars with automatic transmission.
    *   **Finding:** The average price of cars with automatic transmission is approximately $9938.25.

*   **Cars with Highest Owner Count:** Identifies cars with the maximum number of owners.
    *   **Finding:** Many cars across various brands have 5 owners, which is the maximum in the dataset.

*   **Average Engine Size for Diesel Cars:** Computes the average engine size specifically for diesel fuel type cars.
    *   **Finding:** The average engine size for diesel cars is approximately 3.01.

*   **Cars with Price > $10,000:** Counts the number of cars with a price greater than $10,000.
    *   **Finding:** 3651 cars have a price greater than $10,000.

---

## **README for MultipleFiles/EDA_2_.ipynb**

### **Project Title: Movies Dataset Exploratory Data Analysis (EDA)**

### **Overview**
This Jupyter Notebook (`EDA_2_.ipynb`) conducts an exploratory data analysis on a movie dataset. The primary objective is to understand the dataset's structure, identify missing values, and extract basic insights related to movie and show characteristics.

### **Dataset**
The analysis uses a CSV file named `movies.csv`. This dataset contains information about movies and TV shows, including:
*   `title`
*   `type` (MOVIE or SHOW)
*   `release_year`
*   `age_certification`
*   `runtime`
*   `genres`
*   `production_countries`
*   `seasons` (for SHOWs)
*   `imdb_id`
*   `imdb_score`
*   `imdb_votes`

### **Libraries Used**
*   `numpy` for numerical operations.
*   `pandas` for data manipulation and analysis.
*   `matplotlib.pyplot` for plotting.
*   `seaborn` for enhanced data visualizations.

### **Key Analysis and Findings**

The notebook performs several initial data exploration steps and answers specific questions:

*   **Data Loading and Initial Inspection:**
    *   The dataset is loaded and the first few rows are displayed using `df.head(10)`.
    *   `df.info()` is used to check data types, non-null counts, and memory usage.
    *   `df.describe()` provides descriptive statistics for numerical columns.
    *   `df.shape` confirms the number of rows and columns.
    *   `df.isnull().sum()` identifies the count of missing values per column.
    *   `df.duplicated().sum()` checks for duplicate rows.
    *   **Findings:**
        *   The dataset contains 5806 entries and 11 columns.
        *   Columns like `title`, `age_certification`, `seasons`, `imdb_id`, `imdb_score`, and `imdb_votes` have missing values, with `seasons` having the most (3759 missing values).
        *   There are no duplicate rows.

*   **Age Certification Analysis (R vs. PG):**
    *   Filters the DataFrame to create subsets for 'R' and 'PG' age certifications.
    *   Compares the `imdb_score` distribution for 'R' and 'PG' rated content using histograms.
    *   **Findings:**
        *   There are 575 entries with 'R' age certification and 246 with 'PG'.
        *   The histogram visually represents the distribution of IMDB scores for 'R' and 'PG' content, showing their respective score ranges and frequencies.

*   **Unique Content Types:**
    *   Identifies all unique values in the `type` column.
    *   **Finding:** The dataset contains two unique types: 'SHOW' and 'MOVIE'.

*   **Release Year Range:**
    *   Calculates the minimum and maximum release years and the total range.
    *   **Finding:** The release years in the dataset range from 1945 to 2022, covering a span of 77 years.

*   **Movies with Runtime > 100 minutes:**
    *   Counts the number of movies that have a runtime greater than 100 minutes.
    *   **Finding:** There are 1723 movies with a runtime exceeding 100 minutes.

*   **Unique Age Certifications:**
    *   Lists all unique age certifications present in the dataset.
    *   **Finding:** Unique age certifications include 'TV-MA', 'R', 'PG', 'TV-14', 'G', 'PG-13', 'TV-PG', 'TV-Y', 'TV-G', 'TV-Y7', 'NC-17', and NaN (missing values).

*   **TV-14 Certified Shows Count:**
    *   Counts the number of shows specifically certified as 'TV-14'.
    *   **Finding:** There are 470 TV-14 certified shows.

*   **Content with "Comedy" Genre:**
    *   Counts the total number of movies or shows that include "comedy" in their genres.
    *   **Finding:** 2269 entries (movies or shows) have "comedy" as one of their genres.

*   **"Comedy" Movies Count:**
    *   Counts specifically the number of movies that have "comedy" as one of their genres.
    *   **Finding:** There are 1543 comedy movies in the dataset.
