# Lung Cancer: Death & Demographics

## Team Members
* Abear Awadallah
* Mike Ingram
* Gretel Uptegrove
* Brown Varghese

## Motivation

* Lung cancer is one of the six leading causes of death in the World (according to WHO-World Health Organization), and it is important to understand the relationship between demographics and lung cancer death in order to adequately address prevention and treatment.
* Questions: What demographics are correlated with lung cancer mortality?

## Sources
* [CDC Wonder](https://wonder.cdc.gov/)
    * Lung Cancer Deaths broken down by:
        * Location (State & County Level)
        * Race
        * Age Range (by 5 year increments)
        * Gender
* [FRED Economics Data](https://fred.stlouisfed.org/)
    * Poverty Rate broken down by Location (State & County Level)

## Methods
* Query [CDC Wonder](https://wonder.cdc.gov/) and [FRED Economics Data](https://fred.stlouisfed.org/) databases
* Clean data within a [Jupyter notebook: Data_Cleaning.ipynb](Data_Cleaning.ipynb) using Python and pandas library.
* Create visualizations and perform statistical analysis within a [Jupyter notebook: data_analysis.ipynb](data_analysis.ipynb) using the following Python libraries
  * pandas
  * NumPy
  * Matplotlib
  * SciPy
  * seaborn

## Major Findings

### Race & Lung Cancer Mortality

<img src="Images/Race_Cancer_Pie_Chart.png" alt="Population and Cancer Mortality Breakdown by Race in 2015" height ="450">

* Hypothesis testing:
    * Null Hypothesis(H0): There is no relationship between race and lung cancer mortality in 2015.
    * Alternative Hypothesis(H1): There is a relationship between race and lung cancer mortality in 2015.
* Statistical Testing: Chi-Squared Goodness of Fit Test

<img src="Images/Chi_Squared.png" alt="Chi Squared Goodness of Fit for Race">

* Results of Test: The Chi-Squared value (10042.59) exceeded the critical value (16.27) with a p-value of .001, thus we reject the null hypothesis and accept the alternative hypothesis.
* Conclusion: There is a highly statistically significant relationship between race and lung cancer mortality in the United States in 2015. 

### Poverty & Lung Cancer Mortality

#### By State

<img src="Images/Poverty_v_Cancer_State_Scatter.png" alt="Scatter Plot of Poverty v. Lung Cancer by State in 2015" height ="450">

#### By County

<img src="Images/Poverty_v_Cancer_County_Scatter.png" alt="Scatter Plot of Poverty v. Lung Cancer by County in 2015" height ="450">

* Question: Is there a correlation between poverty and lung cancer mortality by State? by County?
* Statistical Testing: Regression Analysis

#### Regression Analysis by State

<img src="Images/Regression_State.png" alt="Regression Analysis by State">


#### Regression Analysis by County

<img src="Images/Regression_County.png" alt="Regression Analysis by County">


* Results of Analysis: There is a very small R-squared value when you look at poverty and lung cancer mortality across both states (.122) and counties (.110). 
* Conclusion: There is a very weak positive correlation between poverty and lung cancer mortality in the United States in 2015.

## Additional Observations

### Number of Cancer Deaths over time across the United States

<img src="Images/Nationwide_Cancer_Line_Chart.png" alt="Line Chart of Lung Cancer Deaths across the United States from 2006-2015" height ="450">

#### Observations

* There is a steady decline in death rate due to lung cancer in the United States from 2006-2015.

### Cancer Deaths by Sex

<img src="Images/Sex_Cancer_Bar_Chart.png" alt="Bar Chart of Lung Cancer Deaths broken down by sex in the United States from 2006-2015" height ="450">

#### Observations

* Men die of lung cancer at a higher rate than women in the United States from 2006-2015.
* The number of deaths per year is declining for both, but at a slightly higher rate for men.

### Cancer Deaths by Age

<img src="Images/Ages_Cancer_Bar_Chart.png" alt="Bar Chart of Lung Cancer Deaths broken down by age in the United States from 2006-2015" height ="450">

#### Observations

* Most lung cancer deaths occur when people are in their 70’s in the United States from 2006-2015, and no one under the age of 35 has died of lung cancer during that time in the United States.

## Further Questions Raised by Analysis

* Why has lung cancer mortality been decreasing in the United States? Is it new treatment, greater access to healthcare, early testing, or less exposure to carcinogens?
* Why does the greatest incidence of lung cancer deaths occur in people in their 70's? Is it lifestyle, longer exposure to carcinogens, or completely unrelated as the most people die in their 70's regardless of cause?
* Why do women die of lung cancer less than men? Is there a lifestyle difference, a biological difference, or some other factor?
* Why is there a difference in mortality based on race? Is it biological or sociological?
* Why does West Virginia have such a significantly higher rate of lung cancer mortality than the District of Columbia? Is it correlated to the above demographics or other considerations such as lifestyle?
* Would we find correlations with other factors such as education and access to healthcare?
