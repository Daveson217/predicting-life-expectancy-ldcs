# predicting-life-expectancy-ldcs
**Predicting Life Expectancy in Less Developed Countries**

This research work was for my undergraduate thesis at Joseph Ayo Babalola University. It was based on selected Less Developed countries in Africa, Asia, and South America. The machine learning model used was Linear Regression. The countries were selected based on their Human Development Index value. The initial indicators selected were based on previous research works.

**This repository contains the Jupyter notebook files, python files, and datasets used for this research work.**
Machine Learning algorithm used: Linear Regression
Libraries used: Pandas, NumPy, Scikit-learn, statsmodel

## Notebook files
- **data_extracter.ipynb**: This file contains code that work on the `WDIEXCEL` dataset and exports other Excel datasets based on it.
These are the datasets that it produces, in order.
  1. `WDI_EXCEL_TRIMMED.xlsx`: This file trims the `WDIEXCEL` dataset to the following columns: *Country Name*, *Indicator Name*, *Indicator Code*, *2017*, *2018*, *2019*
  2. `WDI_EXCEL_TRIMMED_WITH_CONTINENT.xlsx`: This file has the same contents as `WDI_EXCEL_TRIMMED.xlsx`, but with a new column, Continent.
  3. `AFRICA_ASIA_SOUTHAME_CONTRIES.xlsx`: This lists all the countries in Africa, Asia, and South America
  4. `SELECTED_COUNTRIES_WITH_HDI`: The code that produces this file appends to each country in `AFRICA_ASIA_SOUTHAME_CONTRIES.xlsx`, the corresponding Human Development Index (HDI) value.
- **wdi_trim_to_selected_countries.ipynb**: This notebook contains code that filters the `WDI_EXCEL_TRIMMED_WITH_CONTINENT.xlsx` file to only contain the countries in the `SELECTED_COUNTRIES_WITH_HDI.xlsx` file. It exports this data into `WDI_EXCEL_TRIMMED_SELECTED_COUNTRIES.xlsx`.
- **filter_wdi_dataset_selected_variables.ipynb**: This notebook produces a new Excel file, `FINAL_FILTERED_WDI_DATASET.xlsx`. This file contains the data in `WDI_EXCEL_TRIMMED_SELECTED_COUNTRIES.xlsx` filtered based on the initially selected indicators in the `MAIN DATASET.xlsx`, the *Variables List* worksheet.
- **fill_dataset.ipynb**: This notebook populates the `FINAL_MAIN_TEST.xlsx`, although I already made changes to the file by adding some new worksheets. 
- **linear_regression.ipynb**: This notebook performs the Linear regression training and testing, and prints out the Model score, and evaluation metrics such as MAE, MSE, and R-squared. It uses the `FINAL_DATASEST_CORRELATION.xlsx` file which is a copy of `Sheet 3` of the `FINAL_MAIN_TEST.xlsx` file. It uses the `TrimmedIndicators` work sheet. It also has other worksheets that shows the correlation analysis performed on the initially selected variables.
- **regression_script.ipynb**: This file performs the trains the linear regression model and prints out metrics using the `statsmodel` library.
