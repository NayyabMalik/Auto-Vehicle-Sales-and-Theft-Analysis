# Auto Vehicle Sales and Theft Analysis

## Overview

This project performs exploratory data analysis (EDA) on a dataset of auto vehicle production and sales, with a focus on motorcycle sales and theft trends. Using Python, Pandas, NumPy, Matplotlib, and Seaborn, the project analyzes sales and production data for various vehicle types (e.g., motorcycles, cars, trucks) and visualizes motorcycle theft trends over time. It showcases skills in data preprocessing, time-series analysis, and data visualization for data science applications.

## Dataset

The dataset (`dataset.csv`) contains 3,248 records of auto vehicle production and sales from 2018 to 2023, with the following key columns:

- **Observation Date**: Date of the record (e.g., 31-Oct-2023).
- **Series Display Name**: Type of vehicle and metric (e.g., Sales of Motor cycles, Production of Cars and Jeeps).
- **Observation Value**: Number of vehicles sold or produced (e.g., 101,976 for motorcycle sales in October 2023).
- **Series name**: Simplified category name (e.g., Sales of Motor cycles).
- **Unit**: Measurement unit (Number).
- **Sequence No.**: Identifier for data organization.

Additional derived columns include:

- **year**, **day**, **week**, **quarter**, **hour**: Extracted from the `Observation Date` for time-based analysis.

A subset of the data (`motor_theft_df`) is used to analyze motorcycle theft trends, with columns:

- **Year**: Year of theft data.
- **Normalised/100000**: Theft rate per 100,000 population.

## Features

- **Data Preprocessing**:
  - Loads the dataset using Pandas (`pd.read_csv`).
  - Converts `Observation Date` to datetime format and extracts `year`, `day`, `week`, `quarter`, and `hour` for time-series analysis.
  - Drops irrelevant columns (e.g., `Unit`, `Observation Status Comment`) to streamline the dataset.
  - Checks dataset structure (`df.info()`) and unique categories (`Series Display Name`).
- **Exploratory Data Analysis**:
  - Inspects dataset with `df.head()` and `df.info()` to confirm 3,248 non-null entries and data types.
  - Identifies unique vehicle categories (e.g., Sales of Motor cycles, Production of Trucks).
  - Analyzes motorcycle sales, noting high sales volumes (e.g., 101,976 units in October 2023).
  - Visualizes motorcycle theft trends using a Seaborn histogram (`sns.histplot`), plotting theft rates (`Normalised/100000`) by year.
- **Tools and Libraries**:
  - Python: Pandas, NumPy, Matplotlib, Seaborn
  - Jupyter Notebook for interactive analysis and visualization

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/auto-vehicle-sales-theft-analysis.git
   cd auto-vehicle-sales-theft-analysis
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Place the `dataset.csv` file in the `data/` directory. Note: The `motor_theft_df` dataset (for theft analysis) is assumed to be derived or provided separately.

## Usage

1. Open the Jupyter Notebook:

   ```bash
   jupyter notebook Auto_Vehicle_Sales_Theft_Analysis.ipynb
   ```

2. Update the file path in the notebook to point to your `data/dataset.csv` file (e.g., `./data/dataset.csv`).

3. Run all cells to:

   - Load and preprocess the dataset.
   - Extract time-based features (year, quarter, etc.).
   - Generate a histogram of motorcycle theft rates by year.

## Repository Structure

```
auto-vehicle-sales-theft-analysis/
├── data/
│   └── dataset.csv          # Auto vehicle sales and production dataset
├── README.md               # Project documentation
├── LICENSE                 # MIT License
```

## Requirements

Install the required libraries using:

```bash
pip install pandas numpy matplotlib seaborn
```

## Notes

- The dataset has no missing values in key columns, ensuring reliable analysis.
- The histogram of motorcycle theft rates (`Normalised/100000` by `Year`) highlights trends in theft over time, useful for understanding security or market dynamics.
- Motorcycle sales dominate the dataset (e.g., 101,976 units in October 2023) compared to other vehicle types (e.g., 26 buses).
- Future enhancements could include:
  - Time-series plots of sales by vehicle type (e.g., motorcycles vs. cars) over years or quarters.
  - Statistical analysis of sales trends (e.g., mean, median sales per category).
  - Merging theft and sales data to explore correlations between sales volumes and theft rates.
- The notebook uses a local file path (`C:\\Users\\PMLS\\Downloads\\dataset.csv`). Update to a relative path (e.g., `./data/dataset.csv`) for portability.
- The `motor_theft_df` dataset is not fully defined in the notebook. Ensure it is available or derived for theft visualization.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Contact

For questions, contact nayyabm16@gmail.com or open an issue on GitHub.