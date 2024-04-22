<p style="text-align:center">
    <a href="https://skills.network/?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMDA0321ENSkillsNetwork928-2022-01-01" target="_blank">
    <img src="https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/assets/logos/SN_web_lightmode.png" width="200" alt="Skills Network Logo"  />
    </a>
</p>


# **Survey Dataset Exploration Lab**


Estimated time needed: **30** minutes


## Objectives


After completing this lab you will be able to:


-   Load the dataset that will used thru the capstone project.
-   Explore the dataset.
-   Get familier with the data types.


## Load the dataset


Import the required libraries.



```python
import pandas as pd
```

The dataset is available on the IBM Cloud at the below url.



```python
dataset_url = "https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-DA0321EN-SkillsNetwork/LargeData/m1_survey_data.csv"
```

Load the data available at dataset_url into a dataframe.



```python
# your code goes here
df = pd.read_csv(dataset_url)
```

## Explore the data set


It is a good idea to print the top 5 rows of the dataset to get a feel of how the dataset will look.


Display the top 5 rows and columns from your dataset.



```python
# your code goes here
df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Respondent</th>
      <th>MainBranch</th>
      <th>Hobbyist</th>
      <th>OpenSourcer</th>
      <th>OpenSource</th>
      <th>Employment</th>
      <th>Country</th>
      <th>Student</th>
      <th>EdLevel</th>
      <th>UndergradMajor</th>
      <th>...</th>
      <th>WelcomeChange</th>
      <th>SONewContent</th>
      <th>Age</th>
      <th>Gender</th>
      <th>Trans</th>
      <th>Sexuality</th>
      <th>Ethnicity</th>
      <th>Dependents</th>
      <th>SurveyLength</th>
      <th>SurveyEase</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>4</td>
      <td>I am a developer by profession</td>
      <td>No</td>
      <td>Never</td>
      <td>The quality of OSS and closed source software ...</td>
      <td>Employed full-time</td>
      <td>United States</td>
      <td>No</td>
      <td>Bachelor’s degree (BA, BS, B.Eng., etc.)</td>
      <td>Computer science, computer engineering, or sof...</td>
      <td>...</td>
      <td>Just as welcome now as I felt last year</td>
      <td>Tech articles written by other developers;Indu...</td>
      <td>22.0</td>
      <td>Man</td>
      <td>No</td>
      <td>Straight / Heterosexual</td>
      <td>White or of European descent</td>
      <td>No</td>
      <td>Appropriate in length</td>
      <td>Easy</td>
    </tr>
    <tr>
      <th>1</th>
      <td>9</td>
      <td>I am a developer by profession</td>
      <td>Yes</td>
      <td>Once a month or more often</td>
      <td>The quality of OSS and closed source software ...</td>
      <td>Employed full-time</td>
      <td>New Zealand</td>
      <td>No</td>
      <td>Some college/university study without earning ...</td>
      <td>Computer science, computer engineering, or sof...</td>
      <td>...</td>
      <td>Just as welcome now as I felt last year</td>
      <td>NaN</td>
      <td>23.0</td>
      <td>Man</td>
      <td>No</td>
      <td>Bisexual</td>
      <td>White or of European descent</td>
      <td>No</td>
      <td>Appropriate in length</td>
      <td>Neither easy nor difficult</td>
    </tr>
    <tr>
      <th>2</th>
      <td>13</td>
      <td>I am a developer by profession</td>
      <td>Yes</td>
      <td>Less than once a month but more than once per ...</td>
      <td>OSS is, on average, of HIGHER quality than pro...</td>
      <td>Employed full-time</td>
      <td>United States</td>
      <td>No</td>
      <td>Master’s degree (MA, MS, M.Eng., MBA, etc.)</td>
      <td>Computer science, computer engineering, or sof...</td>
      <td>...</td>
      <td>Somewhat more welcome now than last year</td>
      <td>Tech articles written by other developers;Cour...</td>
      <td>28.0</td>
      <td>Man</td>
      <td>No</td>
      <td>Straight / Heterosexual</td>
      <td>White or of European descent</td>
      <td>Yes</td>
      <td>Appropriate in length</td>
      <td>Easy</td>
    </tr>
    <tr>
      <th>3</th>
      <td>16</td>
      <td>I am a developer by profession</td>
      <td>Yes</td>
      <td>Never</td>
      <td>The quality of OSS and closed source software ...</td>
      <td>Employed full-time</td>
      <td>United Kingdom</td>
      <td>No</td>
      <td>Master’s degree (MA, MS, M.Eng., MBA, etc.)</td>
      <td>NaN</td>
      <td>...</td>
      <td>Just as welcome now as I felt last year</td>
      <td>Tech articles written by other developers;Indu...</td>
      <td>26.0</td>
      <td>Man</td>
      <td>No</td>
      <td>Straight / Heterosexual</td>
      <td>White or of European descent</td>
      <td>No</td>
      <td>Appropriate in length</td>
      <td>Neither easy nor difficult</td>
    </tr>
    <tr>
      <th>4</th>
      <td>17</td>
      <td>I am a developer by profession</td>
      <td>Yes</td>
      <td>Less than once a month but more than once per ...</td>
      <td>The quality of OSS and closed source software ...</td>
      <td>Employed full-time</td>
      <td>Australia</td>
      <td>No</td>
      <td>Bachelor’s degree (BA, BS, B.Eng., etc.)</td>
      <td>Computer science, computer engineering, or sof...</td>
      <td>...</td>
      <td>Just as welcome now as I felt last year</td>
      <td>Tech articles written by other developers;Indu...</td>
      <td>29.0</td>
      <td>Man</td>
      <td>No</td>
      <td>Straight / Heterosexual</td>
      <td>Hispanic or Latino/Latina;Multiracial</td>
      <td>No</td>
      <td>Appropriate in length</td>
      <td>Easy</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 85 columns</p>
</div>



## Find out the number of rows and columns


Start by exploring the numbers of rows and columns of data in the dataset.


Print the number of rows in the dataset.



```python
# your code goes here
df.shape[0]
```




    11552



Print the number of columns in the dataset.



```python
# your code goes here
len(df.columns)
```




    85



## Identify the data types of each column


Explore the dataset and identify the data types of each column.


Print the datatype of all columns.



```python
# your code goes here
df.dtypes

```




    Respondent       int64
    MainBranch      object
    Hobbyist        object
    OpenSourcer     object
    OpenSource      object
                     ...  
    Sexuality       object
    Ethnicity       object
    Dependents      object
    SurveyLength    object
    SurveyEase      object
    Length: 85, dtype: object



Print the mean age of the survey participants.



```python
# your code goes here
df['Age'].mean()
```




    30.77239449133718



The dataset is the result of a world wide survey. Print how many unique countries are there in the Country column.



```python
# your code goes here
countrydf = df['Country'].unique()
countrydf.shape[0]
```




    135



## Authors


Ramesh Sannareddy


### Other Contributors


Rav Ahuja


## Change Log


| Date (YYYY-MM-DD) | Version | Changed By        | Change Description                 |
| ----------------- | ------- | ----------------- | ---------------------------------- |
| 2020-10-17        | 0.1     | Ramesh Sannareddy | Created initial version of the lab |


 Copyright © 2020 IBM Corporation. This notebook and its source code are released under the terms of the [MIT License](https://cognitiveclass.ai/mit-license?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMDA0321ENSkillsNetwork928-2022-01-01&cm_mmc=Email_Newsletter-_-Developer_Ed%2BTech-_-WW_WW-_-SkillsNetwork-Courses-IBM-DA0321EN-SkillsNetwork-21426264&cm_mmca1=000026UJ&cm_mmca2=10006555&cm_mmca3=M12345678&cvosrc=email.Newsletter.M12345678&cvo_campaign=000026UJ).

