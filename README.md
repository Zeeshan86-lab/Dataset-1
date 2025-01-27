# PF PROJECT
# Summary of Data Analysis Code

## Importing Libraries
- **`import pandas as pd`**: Used for data manipulation and analysis.
- **`import matplotlib as plt`**: Used for data visualization (should be corrected to `import matplotlib.pyplot as plt`).

---

## Reading the CSV File
- **`pd.read_csv("zeeshan.csv")`**: Reads the CSV file into a DataFrame named `data`.

---

## Inspecting the Data
- **`data.info()`**: Displays the structure, data types, and non-null counts of the DataFrame.
- **`data.head(3)`**: Displays the first 3 rows of the DataFrame.
- **`data.tail(6)`**: Displays the last 6 rows of the DataFrame.
- **`data.sample(5)`**: Randomly selects 5 rows from the DataFrame.
- **`data.shape`**: Returns the number of rows and columns in the DataFrame.

---

## Renaming Columns
- **`data.rename(columns={"Thialand": "pakistan", "America": "Scotland"})`**: Renames specified columns.

---

## Summary Statistics
- **`data.describe()`**: Provides summary statistics for numerical columns.

---

## Checking Null Values
- **`data.notnull()`**: Checks for non-null values in the DataFrame.
- **`data.isnull().sum()`**: Counts the number of null values in each column.
- **`data[data["country"].isnull()]`**: Filters rows where the "country" column has null values.

---

## Data Types and Column Names
- **`data.dtypes`**: Displays the data types of all columns.
- **`data.columns`**: Lists the column names.

---

## Slicing and Selecting Rows
- **`data[1:7:2]`**: Selects rows from index 1 to 7 with a step of 2.
- **`data[2:5]`**: Selects rows from index 2 to 5.
- **`data.loc[[2, 5, 7, 11]]`**: Selects rows with specific indices (2, 5, 7, 11).

---

## Handling Missing Data
- **`data.dropna()`**: Removes rows with missing values.
- **`data.fillna(3)`**: Fills missing values with `3`.

---

## Visualizing Data
- **`data["country"].value_counts().plot(kind="bar")`**: Creates a bar plot for the "country" column.
- **`data["country"].value_counts().plot(kind="line")`**: Creates a line plot for the "country" column.
- **`data["country"].value_counts().plot(kind="pie")`**: Creates a pie chart for the "country" column.
- **`data["country"].value_counts().plot(kind="hist")`**: Creates a histogram for the "country" column.
- **`data.plot(color='red')`**: Plots the entire DataFrame with red color (requires numeric data).

---

## Statistical Measures
- **`data["MostVisited_NumOfArrivals_Millions_2023"].mean()`**: Calculates the mean of the column.
- **`data["MostVisited_NumOfArrivals_Millions_2023"].median()`**: Calculates the median of the column.
- **`data["MostVisited_NumOfArrivals_Millions_2023"].mode()`**: Calculates the mode of the column.

---

## Functions Used

| **Function**                     | **Purpose**                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------|
| `pd.read_csv()`                  | Reads a CSV file into a DataFrame.                                                             |
| `.info()`                        | Displays the structure and summary of the DataFrame.                                           |
| `.head(n)`                       | Displays the first `n` rows of the DataFrame.                                                  |
| `.tail(n)`                       | Displays the last `n` rows of the DataFrame.                                                   |
| `.sample(n)`                     | Randomly selects `n` rows from the DataFrame.                                                  |
| `.shape`                         | Returns the number of rows and columns in the DataFrame.                                       |
| `.rename()`                      | Renames columns in the DataFrame.                                                              |
| `.describe()`                    | Provides summary statistics for numerical columns.                                             |
| `.notnull()`                     | Checks for non-null values in the DataFrame.                                                   |
| `.isnull()`                      | Checks for null values in the DataFrame.                                                       |
| `.sum()`                         | Sums values along an axis (used here for null value counts).                                   |
| `.dtypes`                        | Displays the data types of all columns.                                                        |
| `.columns`                       | Lists the column names.                                                                        |
| `.dropna()`                      | Removes rows with missing values.                                                              |
| `.fillna()`                      | Fills missing values with a specified value.                                                   |
| `.loc[]`                         | Selects rows by index labels.                                                                  |
| `.value_counts()`                | Counts unique values in a column.                                                              |
| `.plot(kind=...)`                | Creates various plots (bar, line, pie, histogram).                                             |
| `.mean()`                        | Calculates the mean of a column.                                                               |
| `.median()`                      | Calculates the median of a column.                                                             |
| `.mode()`                        | Calculates the mode of a column.         
