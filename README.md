# **Exploratory Data Analysis on Vehicle Listings Dataset**

## **Project Overview**
This project performs an **Exploratory Data Analysis (EDA)** on a dataset of vehicle listings. The aim is to clean, analyze, and extract insights about the listings, covering features such as price, year, manufacturer, condition, and more. This analysis can help understand trends in vehicle sales, pricing, and other factors affecting the listings.

---

## **Dataset Description**

The dataset contains **426,880 entries** with **25 columns**. Below is an overview of the dataset:

| Column Name     | Description                                | Non-Null Count | Data Type  |
|-----------------|--------------------------------------------|---------------|------------|
| `url`          | URL of the vehicle listing                 | 426,880       | object     |
| `region`       | Region where the vehicle is listed         | 426,880       | object     |
| `region_url`   | URL of the listing region                  | 426,880       | object     |
| `price`        | Price of the vehicle                       | 426,880       | int64      |
| `year`         | Manufacturing year of the vehicle          | 425,675       | float64    |
| `manufacturer` | Vehicle manufacturer                       | 409,234       | object     |
| `model`        | Model of the vehicle                       | 421,603       | object     |
| `condition`    | Condition of the vehicle                   | 252,776       | object     |
| `cylinders`    | Number of engine cylinders                 | 249,202       | object     |
| `fuel`         | Type of fuel used                          | 423,867       | object     |
| `odometer`     | Odometer reading (mileage)                 | 422,480       | float64    |
| `title_status` | Title status of the vehicle                | 418,638       | object     |
| `transmission` | Transmission type                          | 424,324       | object     |
| `VIN`          | Vehicle Identification Number              | 265,838       | object     |
| `drive`        | Type of drive (e.g., 4wd, fwd)             | 296,313       | object     |
| `size`         | Size category of the vehicle               | 120,519       | object     |
| `type`         | Vehicle type (e.g., SUV, truck)            | 334,022       | object     |
| `paint_color`  | Color of the vehicle paint                 | 296,677       | object     |
| `image_url`    | URL of the vehicle image                   | 426,812       | object     |
| `description`  | Description of the vehicle                 | 426,810       | object     |
| `county`       | County information (all values are null)   | 0             | float64    |
| `state`        | State of the vehicle listing               | 426,880       | object     |
| `lat`          | Latitude of the vehicle location           | 420,331       | float64    |
| `long`         | Longitude of the vehicle location          | 420,331       | float64    |
| `posting_date` | Date of the listing post                   | 426,812       | object     |

---

## **Issues Observed in the Dataset**
- Several columns contain **missing values**:
  - `year`, `manufacturer`, `condition`, `cylinders`, `VIN`, `drive`, `size`, `paint_color`, etc.
- The `county` column contains **no non-null values** (likely irrelevant and can be dropped).
- Some columns like `year` are of type **float64** and may require proper formatting (e.g., converting to integers or strings).

---

## **Data Cleaning Steps**
The following steps were applied to clean the dataset:
1. **Handling Missing Values**:
   - Dropped columns with a high percentage of null values (e.g., `county`).
   - Imputed missing values in relevant columns (`year`, `manufacturer`, etc.) using mean, median, or mode.
2. **Data Type Conversion**:
   - Converted `year` to integer or string format.
=3. **Outlier Detection**:
   - Identified extreme values in `price` and `odometer` columns.
4. **Dropping Duplicates**:
   - Checked for and removed duplicate records if present.

---

## **Exploratory Data Analysis**
Key visualizations and analyses performed include:

1. **Price Distribution**:
   - Visualized using a **histogram** to understand the spread and skewness of vehicle prices.

2. **Year vs Price**:
   - A scatter plot to show the relationship between vehicle manufacturing year and price.

3. **Top Manufacturers**:
   - Bar chart showing the most frequent vehicle manufacturers in the dataset.

4. **Condition Analysis**:
   - Distribution of vehicle condition across various categories.

5. **Fuel Type Analysis**:
   - Pie chart showing the percentage breakdown of vehicles by fuel type.

6. **Odometer Reading Distribution**:
   - Box plot to detect outliers and analyze mileage data.

7. **Geospatial Analysis**:
   - Visualization of vehicle listings on a map using latitude and longitude.

---

## **Tools and Libraries Used**
- **Python**: Data manipulation and analysis
- **Pandas**: Data cleaning and wrangling
- **Matplotlib** and **Seaborn**: Data visualization
- **Jupyter Notebook**: For interactive analysis

---


## **Contributing**
Contributions are welcome! Feel free to fork this repository, create a branch, and submit a pull request.

---

## **License**
This project is licensed under the MIT License.

---

## **Author**
**Mariam Badr**  
- LinkedIn: 
- GitHub: [Your GitHub Profile](#)
