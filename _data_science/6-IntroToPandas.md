---
layout: page
title:  "Intro to Pandas"
day: 2
---

# Download

Download the notebook file [here](Week1/IntroToPandas.ipynb).
# A small introduction to Pandas

Pandas is a library that allows you to do data anlysis, manipulation and storing very easily in python. It is called using the following command: import pandas as pd


```python
import pandas as pd

#read a file into pandas by using the read_csv function (there are other read function, that you can look up)

df = pd.read_csv('/home/dhruvy/Datasets/GTD/gtd.csv')
```

    /home/dhruvy/anaconda2/lib/python2.7/site-packages/IPython/core/interactiveshell.py:2717: DtypeWarning: Columns (4,61,62,66,116,117,123) have mixed types. Specify dtype option on import or set low_memory=False.
      interactivity=interactivity, compiler=compiler, result=result)



```python
df.dtypes
```


```python
df.head()
```


```python
df.tail()
```


```python
df.index
```


```python
df.shape
```


```python
df.describe()
```


```python
df.sort_values(by='country')
```


```python
df['country_txt']
```




    0               Dominican Republic
    1                           Mexico
    2                      Philippines
    3                           Greece
    4                            Japan
    5                    United States
    6                          Uruguay
    7                    United States
    8                    United States
    9                    United States
    10                   United States
    11                   United States
    12                           Italy
    13                   United States
    14                   United States
    15              East Germany (GDR)
    16                        Ethiopia
    17                   United States
    18                   United States
    19                   United States
    20                   United States
    21                         Uruguay
    22                   United States
    23                   United States
    24                   United States
    25                       Guatemala
    26                     Philippines
    27                       Venezuela
    28                   United States
    29                   United States
                        ...           
    156742                        Iraq
    156743                        Iraq
    156744                        Iraq
    156745                        Iraq
    156746                       Yemen
    156747                       Yemen
    156748                       Yemen
    156749                       Yemen
    156750                Saudi Arabia
    156751                       Egypt
    156752                Saudi Arabia
    156753    West Bank and Gaza Strip
    156754                      Turkey
    156755                     Ukraine
    156756                       India
    156757                     Germany
    156758                    Ethiopia
    156759                 Philippines
    156760                 Afghanistan
    156761                 Philippines
    156762                 Philippines
    156763                        Iraq
    156764                    Pakistan
    156765                    Pakistan
    156766                    Pakistan
    156767                     Burundi
    156768                     Ireland
    156769                 Philippines
    156770                     Somalia
    156771                       Libya
    Name: country_txt, dtype: object




```python
df[0:10]
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>eventid</th>
      <th>iyear</th>
      <th>imonth</th>
      <th>iday</th>
      <th>approxdate</th>
      <th>extended</th>
      <th>resolution</th>
      <th>country</th>
      <th>country_txt</th>
      <th>region</th>
      <th>...</th>
      <th>addnotes</th>
      <th>scite1</th>
      <th>scite2</th>
      <th>scite3</th>
      <th>dbsource</th>
      <th>INT_LOG</th>
      <th>INT_IDEO</th>
      <th>INT_MISC</th>
      <th>INT_ANY</th>
      <th>related</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>197000000001</td>
      <td>1970</td>
      <td>0</td>
      <td>0</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>58</td>
      <td>Dominican Republic</td>
      <td>2</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>197000000002</td>
      <td>1970</td>
      <td>0</td>
      <td>0</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>130</td>
      <td>Mexico</td>
      <td>1</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>197001000001</td>
      <td>1970</td>
      <td>1</td>
      <td>0</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>160</td>
      <td>Philippines</td>
      <td>5</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>1</td>
      <td>1</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>197001000002</td>
      <td>1970</td>
      <td>1</td>
      <td>0</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>78</td>
      <td>Greece</td>
      <td>8</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>1</td>
      <td>1</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>197001000003</td>
      <td>1970</td>
      <td>1</td>
      <td>0</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>101</td>
      <td>Japan</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>1</td>
      <td>1</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5</th>
      <td>197001010002</td>
      <td>1970</td>
      <td>1</td>
      <td>1</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>217</td>
      <td>United States</td>
      <td>1</td>
      <td>...</td>
      <td>The Cairo Chief of Police, William Petersen, r...</td>
      <td>"Police Chief Quits," Washington Post, January...</td>
      <td>"Cairo Police Chief Quits; Decries Local 'Mili...</td>
      <td>Christopher Hewitt, "Political Violence and Te...</td>
      <td>Hewitt Project</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>6</th>
      <td>197001020001</td>
      <td>1970</td>
      <td>1</td>
      <td>2</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>218</td>
      <td>Uruguay</td>
      <td>3</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>7</th>
      <td>197001020002</td>
      <td>1970</td>
      <td>1</td>
      <td>2</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>217</td>
      <td>United States</td>
      <td>1</td>
      <td>...</td>
      <td>Damages were estimated to be between $20,000-$...</td>
      <td>Committee on Government Operations United Stat...</td>
      <td>Christopher Hewitt, "Political Violence and Te...</td>
      <td>NaN</td>
      <td>Hewitt Project</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>8</th>
      <td>197001020003</td>
      <td>1970</td>
      <td>1</td>
      <td>2</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>217</td>
      <td>United States</td>
      <td>1</td>
      <td>...</td>
      <td>The New Years Gang issue a communiqu� to a loc...</td>
      <td>Tom Bates, "Rads: The 1970 Bombing of the Army...</td>
      <td>David Newman, Sandra Sutherland, and Jon Stewa...</td>
      <td>The Wisconsin Cartographers' Guild, "Wisconsin...</td>
      <td>Hewitt Project</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>9</th>
      <td>197001030001</td>
      <td>1970</td>
      <td>1</td>
      <td>3</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>217</td>
      <td>United States</td>
      <td>1</td>
      <td>...</td>
      <td>Karl Armstrong's girlfriend, Lynn Schultz, dro...</td>
      <td>Committee on Government Operations United Stat...</td>
      <td>Tom Bates, "Rads: The 1970 Bombing of the Army...</td>
      <td>David Newman, Sandra Sutherland, and Jon Stewa...</td>
      <td>Hewitt Project</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>10 rows × 137 columns</p>
</div>




```python
df[df.country_txt == 'China']
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>eventid</th>
      <th>iyear</th>
      <th>imonth</th>
      <th>iday</th>
      <th>approxdate</th>
      <th>extended</th>
      <th>resolution</th>
      <th>country</th>
      <th>country_txt</th>
      <th>region</th>
      <th>...</th>
      <th>addnotes</th>
      <th>scite1</th>
      <th>scite2</th>
      <th>scite3</th>
      <th>dbsource</th>
      <th>INT_LOG</th>
      <th>INT_IDEO</th>
      <th>INT_MISC</th>
      <th>INT_ANY</th>
      <th>related</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>37989</th>
      <td>198904240015</td>
      <td>1989</td>
      <td>4</td>
      <td>24</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>38623</th>
      <td>198906260004</td>
      <td>1989</td>
      <td>6</td>
      <td>26</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>40861</th>
      <td>198912160006</td>
      <td>1989</td>
      <td>12</td>
      <td>16</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>44726</th>
      <td>199012070002</td>
      <td>1990</td>
      <td>12</td>
      <td>7</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>45062</th>
      <td>199101150001</td>
      <td>1991</td>
      <td>1</td>
      <td>15</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>49934</th>
      <td>199202010001</td>
      <td>1992</td>
      <td>2</td>
      <td>1</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>49981</th>
      <td>199202050008</td>
      <td>1992</td>
      <td>2</td>
      <td>5</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>51399</th>
      <td>199205170002</td>
      <td>1992</td>
      <td>5</td>
      <td>17</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>1</td>
      <td>1</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>51464</th>
      <td>199205210005</td>
      <td>1992</td>
      <td>5</td>
      <td>21</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>1</td>
      <td>1</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54164</th>
      <td>199211280006</td>
      <td>1992</td>
      <td>11</td>
      <td>28</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>55153</th>
      <td>199402180007</td>
      <td>1994</td>
      <td>2</td>
      <td>18</td>
      <td>NaN</td>
      <td>1</td>
      <td>2/18/94</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>55361</th>
      <td>199403070007</td>
      <td>1994</td>
      <td>3</td>
      <td>7</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>55362</th>
      <td>199403070008</td>
      <td>1994</td>
      <td>3</td>
      <td>7</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>55398</th>
      <td>199403090006</td>
      <td>1994</td>
      <td>3</td>
      <td>9</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>55399</th>
      <td>199403090007</td>
      <td>1994</td>
      <td>3</td>
      <td>9</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>55712</th>
      <td>199404010006</td>
      <td>1994</td>
      <td>4</td>
      <td>1</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>1</td>
      <td>1</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>56423</th>
      <td>199406060004</td>
      <td>1994</td>
      <td>6</td>
      <td>6</td>
      <td>NaN</td>
      <td>1</td>
      <td>6/6/94</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>57240</th>
      <td>199409200003</td>
      <td>1994</td>
      <td>9</td>
      <td>20</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>57341</th>
      <td>199409300009</td>
      <td>1994</td>
      <td>9</td>
      <td>30</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>57893</th>
      <td>199412100009</td>
      <td>1994</td>
      <td>12</td>
      <td>10</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>58026</th>
      <td>199412230004</td>
      <td>1994</td>
      <td>12</td>
      <td>23</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>58027</th>
      <td>199412230005</td>
      <td>1994</td>
      <td>12</td>
      <td>23</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>58095</th>
      <td>199412310010</td>
      <td>1994</td>
      <td>12</td>
      <td>31</td>
      <td>NaN</td>
      <td>1</td>
      <td>1/1/95</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>58194</th>
      <td>199501140006</td>
      <td>1995</td>
      <td>1</td>
      <td>14</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>58253</th>
      <td>199501230002</td>
      <td>1995</td>
      <td>1</td>
      <td>23</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>199501230003, 199501230004, 199501230005, 1995...</td>
    </tr>
    <tr>
      <th>58254</th>
      <td>199501230003</td>
      <td>1995</td>
      <td>1</td>
      <td>23</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>199501230002, 199501230004, 199501230005, 1995...</td>
    </tr>
    <tr>
      <th>58255</th>
      <td>199501230004</td>
      <td>1995</td>
      <td>1</td>
      <td>23</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>59935</th>
      <td>199508020008</td>
      <td>1995</td>
      <td>8</td>
      <td>2</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>-9</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>60574</th>
      <td>199510120017</td>
      <td>1995</td>
      <td>10</td>
      <td>12</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>1</td>
      <td>1</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>60966</th>
      <td>199512030004</td>
      <td>1995</td>
      <td>12</td>
      <td>3</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PGIS</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>133500</th>
      <td>201406210013</td>
      <td>2014</td>
      <td>6</td>
      <td>21</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>"Assailants killed in attack on China police,"...</td>
      <td>"China police 'kill 13 attackers'," BBC, June ...</td>
      <td>"World Briefing: China: Police Kill 13 in Atta...</td>
      <td>START Primary Collection</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>134606</th>
      <td>201407120097</td>
      <td>2014</td>
      <td>7</td>
      <td>12</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>"Uyghur Judicial Official, Five Han Chinese Tr...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>START Primary Collection</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>134763</th>
      <td>201407150021</td>
      <td>2014</td>
      <td>7</td>
      <td>15</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>"Explosion hits airport in China's northwest,"...</td>
      <td>"Bomb Explodes at Airport Parking in Western C...</td>
      <td>"Xinhua: Blast Rocks Northwest China's Airport...</td>
      <td>START Primary Collection</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>134974</th>
      <td>201407180075</td>
      <td>2014</td>
      <td>7</td>
      <td>18</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>"Uyghur Judicial Official, Five Han Chinese Tr...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>START Primary Collection</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>135483</th>
      <td>201407280029</td>
      <td>2014</td>
      <td>7</td>
      <td>28</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>Casualty numbers for this attack represent an ...</td>
      <td>"China: 96 killed last week in Xinjiang," The ...</td>
      <td>"Tight security after Xinjiang unrest," BBC, J...</td>
      <td>"AFP: Uighur Group Says Nearly 100 Casualties ...</td>
      <td>START Primary Collection</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>201407280030</td>
    </tr>
    <tr>
      <th>135484</th>
      <td>201407280030</td>
      <td>2014</td>
      <td>7</td>
      <td>28</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>Casualty numbers for this attack represent an ...</td>
      <td>"China: 96 killed last week in Xinjiang," The ...</td>
      <td>"Tight security after Xinjiang unrest," BBC, J...</td>
      <td>"AFP: Uighur Group Says Nearly 100 Casualties ...</td>
      <td>START Primary Collection</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>201407280029</td>
    </tr>
    <tr>
      <th>135565</th>
      <td>201407300031</td>
      <td>2014</td>
      <td>7</td>
      <td>30</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>"Imam in China Who Defended Party's Policies i...</td>
      <td>"Xinjiang imam dies following clashes," BBC, J...</td>
      <td>"Imam Killed in China's Restive Xinjiang," Out...</td>
      <td>START Primary Collection</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>136509</th>
      <td>201408200036</td>
      <td>2014</td>
      <td>8</td>
      <td>20</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>"Xinhua: Police Offer Rewards In Bus Arson Man...</td>
      <td>"Xinhua: 2nd Ld Writethru: One Dead, 19 Injure...</td>
      <td>"China's latest bus fire in eastern port city ...</td>
      <td>START Primary Collection</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>137831</th>
      <td>201409210037</td>
      <td>2014</td>
      <td>9</td>
      <td>21</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>Casualty numbers for this attack represent an ...</td>
      <td>"Explosions Kill at Least 2 in Restive Region ...</td>
      <td>"Pakistan: Xinjiang unrest: China raises death...</td>
      <td>"China Says 50 Dead in Violence in Xinjiang," ...</td>
      <td>START Primary Collection</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>201409210038, 201409210039, 201409210040</td>
    </tr>
    <tr>
      <th>137832</th>
      <td>201409210038</td>
      <td>2014</td>
      <td>9</td>
      <td>21</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>Casualty numbers for this attack represent an ...</td>
      <td>"Explosions Kill at Least 2 in Restive Region ...</td>
      <td>"Pakistan: Xinjiang unrest: China raises death...</td>
      <td>"China Says 50 Dead in Violence in Xinjiang," ...</td>
      <td>START Primary Collection</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>201409210037, 201409210039, 201409210040</td>
    </tr>
    <tr>
      <th>137833</th>
      <td>201409210039</td>
      <td>2014</td>
      <td>9</td>
      <td>21</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>Casualty numbers for this attack represent an ...</td>
      <td>"Explosions Kill at Least 2 in Restive Region ...</td>
      <td>"Pakistan: Xinjiang unrest: China raises death...</td>
      <td>"China Says 50 Dead in Violence in Xinjiang," ...</td>
      <td>START Primary Collection</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>201409210037, 201409210038, 201409210040</td>
    </tr>
    <tr>
      <th>137834</th>
      <td>201409210040</td>
      <td>2014</td>
      <td>9</td>
      <td>21</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>Casualty numbers for this attack represent an ...</td>
      <td>"Explosions Kill at Least 2 in Restive Region ...</td>
      <td>"Pakistan: Xinjiang unrest: China raises death...</td>
      <td>"China Says 50 Dead in Violence in Xinjiang," ...</td>
      <td>START Primary Collection</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>201409210037, 201409210038, 201409210039</td>
    </tr>
    <tr>
      <th>138784</th>
      <td>201410120039</td>
      <td>2014</td>
      <td>10</td>
      <td>12</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>"At Least 22 People Are Reported Killed in   A...</td>
      <td>"Farmers' market attacked in the East Turkesta...</td>
      <td>"22 dead in attack on Han Chinese market in Xi...</td>
      <td>START Primary Collection</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>140731</th>
      <td>201411280042</td>
      <td>2014</td>
      <td>11</td>
      <td>28</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>"15 dead in   attack   in west China's Xinjian...</td>
      <td>"Attack in Western China Leaves at Least 15 Pe...</td>
      <td>"15 killed in 'terrorist attack' in  Xinjiang,...</td>
      <td>START Primary Collection</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>144120</th>
      <td>201502130016</td>
      <td>2015</td>
      <td>2</td>
      <td>13</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>Casualty numbers for this incident conflict ac...</td>
      <td>"Suicide Bomber Kills Up to 8 in Xinjiang, Rad...</td>
      <td>"Seven killed in China suicide attack: Report,...</td>
      <td>"China: Microblog Censorship Pushes Discussion...</td>
      <td>START Primary Collection</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>144991</th>
      <td>201503060013</td>
      <td>2015</td>
      <td>3</td>
      <td>6</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>"Nine hurt in China station knife   attack," D...</td>
      <td>"Knife   attack   at Guangzhou train station i...</td>
      <td>"Rush-hour knife attack at Chinese rail statio...</td>
      <td>START Primary Collection</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>145091</th>
      <td>201503080071</td>
      <td>2015</td>
      <td>3</td>
      <td>8</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>"Chinese Police Shoot Seven Uyghurs Dead Follo...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>START Primary Collection</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>145131</th>
      <td>201503090064</td>
      <td>2015</td>
      <td>3</td>
      <td>9</td>
      <td>NaN</td>
      <td>1</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>"Police Raids Yield No Clues About Kidnapped U...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>START Primary Collection</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>145274</th>
      <td>201503120065</td>
      <td>2015</td>
      <td>3</td>
      <td>12</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>"Chinese Police Shoot Four Uyghurs Dead After ...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>START Primary Collection</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>147596</th>
      <td>201505110099</td>
      <td>2015</td>
      <td>5</td>
      <td>11</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>"Six Dead, Four Injured in Two Successive Suic...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>START Primary Collection</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>147632</th>
      <td>201505120099</td>
      <td>2015</td>
      <td>5</td>
      <td>12</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>"Six Dead, Four Injured in Two Successive Suic...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>START Primary Collection</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>148255</th>
      <td>201505260100</td>
      <td>2015</td>
      <td>5</td>
      <td>26</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>"Chinese Police Shoot Two Uyghurs Dead in Xinj...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>START Primary Collection</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>149152</th>
      <td>201506170103</td>
      <td>2015</td>
      <td>6</td>
      <td>17</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>"China police   shoot   man dead at train stat...</td>
      <td>"Global Times Online:Police Shoot Dead Brick W...</td>
      <td>"China: Ahead of Ramadan, Police Shoot Dead Ui...</td>
      <td>START Primary Collection</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>149313</th>
      <td>201506220061</td>
      <td>2015</td>
      <td>6</td>
      <td>22</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>Casualty numbers for this incident conflict ac...</td>
      <td>"Bomb attack in restive Xinjiang and police re...</td>
      <td>"China: Uighurs launch deadly knife attack kil...</td>
      <td>"At Least 18 Dead in Ramadan Attack on Police ...</td>
      <td>START Primary Collection</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>150181</th>
      <td>201507130028</td>
      <td>2015</td>
      <td>7</td>
      <td>13</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>"1 killed, 6 injured in axe attack in China," ...</td>
      <td>"Chinese police kill 3 'Xinjiang terrorists' i...</td>
      <td>NaN</td>
      <td>START Primary Collection</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>150436</th>
      <td>201507200026</td>
      <td>2015</td>
      <td>7</td>
      <td>20</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>Casualty numbers for this incident conflict ac...</td>
      <td>"Xinhua: 1st LD: Chinese Park Explosion Kills ...</td>
      <td>"Xinhua: 2nd Ld Writethru: 3 Killed In Chinese...</td>
      <td>"Apparent Suicidal Detonation In Eastern Chine...</td>
      <td>START Primary Collection</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>150801</th>
      <td>201507290043</td>
      <td>2015</td>
      <td>7</td>
      <td>29</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>"1 killed, 6 injured in axe attack in China," ...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>START Primary Collection</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>150810</th>
      <td>201507290059</td>
      <td>2015</td>
      <td>7</td>
      <td>26</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>"Chinese airport closed after arson attack abo...</td>
      <td>"Xinhua: Chinese Officials Sacked After Flight...</td>
      <td>"Arson attack on board Chinese flight, forces ...</td>
      <td>START Primary Collection</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>152869</th>
      <td>201509180067</td>
      <td>2015</td>
      <td>9</td>
      <td>18</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>The victims included Chief Wu Feng, Officer Xi...</td>
      <td>"50 knifed to death in China coal mine, Uighur...</td>
      <td>"Bomb suspect killed in blast, parcel deliveri...</td>
      <td>"China: '40 killed' in deadly knife attack at ...</td>
      <td>START Primary Collection</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>155888</th>
      <td>201512060039</td>
      <td>2015</td>
      <td>12</td>
      <td>6</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>44</td>
      <td>China</td>
      <td>4</td>
      <td>...</td>
      <td>NaN</td>
      <td>"Mob attacks checkpoint in China's Inner Mongo...</td>
      <td>"100+ assailants attack checkpoint in China's ...</td>
      <td>NaN</td>
      <td>START Primary Collection</td>
      <td>-9</td>
      <td>-9</td>
      <td>0</td>
      <td>-9</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>242 rows × 137 columns</p>
</div>




```python
df['nperps'].mean()
```




    -61.50443717888837




```python
pd.merge(left, right, on='key') #For merging datasets
```


```python
pd.merge(left, right, on='key')
```


```python
df.append(s, ignore_index=True)
```


```python
df[] = df[].astype("category")
```
