# Vehicle Insurance EDA (Exploratory Data Analysis)

## Project Description

This project focuses on performing Exploratory Data Analysis (EDA) on a dataset related to vehicle insurance. The primary objective is to gain insights into the data and uncover useful information that can aid decision-making for future growth and strategies in the insurance company. The dataset is divided into two main tables: customer_details and customer_policy_details.

## Tasks Performed

### 1. Data Import and Cleaning

#### 1.1 Data Import
We start by importing the necessary Python libraries, such as Pandas and NumPy, to manipulate and analyze the data. Two CSV files, 'customer_details.csv' and 'customer_policy_details.csv', are loaded into dataframes for further analysis.

#### 1.2 Data Cleaning
- We rename the columns in both dataframes for better readability.
- Check for missing values in both dataframes and handle them accordingly.
  - For the 'customer_id' column, we drop rows with missing values because it's not feasible to compute central tendencies for IDs.
  - For numeric columns with missing values in the customer_details dataframe (e.g., 'age', 'driving licence present', 'region code', 'previously insured'), we fill the missing values with the mean of their respective columns.
  - For categorical columns with missing values in the customer_details dataframe (e.g., 'Gender', 'vehicle age', 'vehicle damage'), we fill the missing values with the mode of their respective columns.
  - Similar steps are applied to the customer_policy_details dataframe.

### 2. Outlier Detection and Handling
- We identify outliers in the 'age' column of the customer_details dataframe using the Interquartile Range (IQR) method and find that there are no outliers.
- We also use the IQR method to identify outliers in the 'annual premium (in Rs)' column of the customer_policy_details dataframe and find 10,332 outliers. These outliers are not removed but can be handled as needed.

### 3. Creating a Master Table
- We create a master table by merging the cleaned customer_details and customer_policy_details dataframes using the 'customer_id' column as the key.

### 4. Important Information for Decision-Making
#### 4.1 Gender-wise Average Annual Premium
- We calculate the average annual premium for each gender in the master table.

#### 4.2 Age-wise Average Annual Premium
- We calculate the average annual premium for different age groups in the master table.

#### 4.3 Data Balance Between Genders
- We determine whether the data is balanced between genders by counting the number of records for each gender in the master table.

#### 4.4 Vehicle Age-wise Average Annual Premium
- We calculate the average annual premium for different vehicle age groups in the master table.

### 5. Exploring the Relationship Between Age and Annual Premium
- We calculate the correlation coefficient between 'age' and 'annual premium (in Rs)' to assess the relationship between these two variables.
- The correlation coefficient is found to be 0.067715, indicating a weak positive relationship.

## Conclusion

This EDA project provides valuable insights into the vehicle insurance dataset, allowing the insurance company to make informed decisions for future growth and strategies. It covers data cleaning, outlier detection, merging dataframes, and analyzing important factors such as gender, age, and annual premiums. The weak positive correlation between age and annual premium suggests that age alone may not be a strong predictor of premium amounts. Further analysis and modeling may be needed for a deeper understanding of premium determinants.
