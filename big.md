```python
import pandas as pd
import numpy as np
```


```python
# To import the data into jupyter notebook
data=pd.read_csv('big mart.csv')
data
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
      <th>Item_Identifier</th>
      <th>Item_Weight</th>
      <th>Item_Fat_Content</th>
      <th>Item_Visibility</th>
      <th>Item_Type</th>
      <th>Item_MRP</th>
      <th>Outlet_Identifier</th>
      <th>Outlet_Establishment_Year</th>
      <th>Outlet_Size</th>
      <th>Outlet_Location_Type</th>
      <th>Outlet_Type</th>
      <th>Item_Outlet_Sales</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>FDA15</td>
      <td>9.300</td>
      <td>Low Fat</td>
      <td>0.016047</td>
      <td>Dairy</td>
      <td>249.8092</td>
      <td>OUT049</td>
      <td>1999</td>
      <td>Medium</td>
      <td>Tier 1</td>
      <td>Supermarket Type1</td>
      <td>3735.1380</td>
    </tr>
    <tr>
      <th>1</th>
      <td>DRC01</td>
      <td>5.920</td>
      <td>Regular</td>
      <td>0.019278</td>
      <td>Soft Drinks</td>
      <td>48.2692</td>
      <td>OUT018</td>
      <td>2009</td>
      <td>Medium</td>
      <td>Tier 3</td>
      <td>Supermarket Type2</td>
      <td>443.4228</td>
    </tr>
    <tr>
      <th>2</th>
      <td>FDN15</td>
      <td>17.500</td>
      <td>Low Fat</td>
      <td>0.016760</td>
      <td>Meat</td>
      <td>141.6180</td>
      <td>OUT049</td>
      <td>1999</td>
      <td>Medium</td>
      <td>Tier 1</td>
      <td>Supermarket Type1</td>
      <td>2097.2700</td>
    </tr>
    <tr>
      <th>3</th>
      <td>FDX07</td>
      <td>19.200</td>
      <td>Regular</td>
      <td>0.000000</td>
      <td>Fruits and Vegetables</td>
      <td>182.0950</td>
      <td>OUT010</td>
      <td>1998</td>
      <td>NaN</td>
      <td>Tier 3</td>
      <td>Grocery Store</td>
      <td>732.3800</td>
    </tr>
    <tr>
      <th>4</th>
      <td>NCD19</td>
      <td>8.930</td>
      <td>Low Fat</td>
      <td>0.000000</td>
      <td>Household</td>
      <td>53.8614</td>
      <td>OUT013</td>
      <td>1987</td>
      <td>High</td>
      <td>Tier 3</td>
      <td>Supermarket Type1</td>
      <td>994.7052</td>
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
    </tr>
    <tr>
      <th>8518</th>
      <td>FDF22</td>
      <td>6.865</td>
      <td>Low Fat</td>
      <td>0.056783</td>
      <td>Snack Foods</td>
      <td>214.5218</td>
      <td>OUT013</td>
      <td>1987</td>
      <td>High</td>
      <td>Tier 3</td>
      <td>Supermarket Type1</td>
      <td>2778.3834</td>
    </tr>
    <tr>
      <th>8519</th>
      <td>FDS36</td>
      <td>8.380</td>
      <td>Regular</td>
      <td>0.046982</td>
      <td>Baking Goods</td>
      <td>108.1570</td>
      <td>OUT045</td>
      <td>2002</td>
      <td>NaN</td>
      <td>Tier 2</td>
      <td>Supermarket Type1</td>
      <td>549.2850</td>
    </tr>
    <tr>
      <th>8520</th>
      <td>NCJ29</td>
      <td>10.600</td>
      <td>Low Fat</td>
      <td>0.035186</td>
      <td>Health and Hygiene</td>
      <td>85.1224</td>
      <td>OUT035</td>
      <td>2004</td>
      <td>Small</td>
      <td>Tier 2</td>
      <td>Supermarket Type1</td>
      <td>1193.1136</td>
    </tr>
    <tr>
      <th>8521</th>
      <td>FDN46</td>
      <td>7.210</td>
      <td>Regular</td>
      <td>0.145221</td>
      <td>Snack Foods</td>
      <td>103.1332</td>
      <td>OUT018</td>
      <td>2009</td>
      <td>Medium</td>
      <td>Tier 3</td>
      <td>Supermarket Type2</td>
      <td>1845.5976</td>
    </tr>
    <tr>
      <th>8522</th>
      <td>DRG01</td>
      <td>14.800</td>
      <td>Low Fat</td>
      <td>0.044878</td>
      <td>Soft Drinks</td>
      <td>75.4670</td>
      <td>OUT046</td>
      <td>1997</td>
      <td>Small</td>
      <td>Tier 1</td>
      <td>Supermarket Type1</td>
      <td>765.6700</td>
    </tr>
  </tbody>
</table>
<p>8523 rows × 12 columns</p>
</div>




```python
data.head()
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
      <th>Item_Identifier</th>
      <th>Item_Weight</th>
      <th>Item_Fat_Content</th>
      <th>Item_Visibility</th>
      <th>Item_Type</th>
      <th>Item_MRP</th>
      <th>Outlet_Identifier</th>
      <th>Outlet_Establishment_Year</th>
      <th>Outlet_Size</th>
      <th>Outlet_Location_Type</th>
      <th>Outlet_Type</th>
      <th>Item_Outlet_Sales</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>FDA15</td>
      <td>9.30</td>
      <td>Low Fat</td>
      <td>0.016047</td>
      <td>Dairy</td>
      <td>249.8092</td>
      <td>OUT049</td>
      <td>1999</td>
      <td>Medium</td>
      <td>Tier 1</td>
      <td>Supermarket Type1</td>
      <td>3735.1380</td>
    </tr>
    <tr>
      <th>1</th>
      <td>DRC01</td>
      <td>5.92</td>
      <td>Regular</td>
      <td>0.019278</td>
      <td>Soft Drinks</td>
      <td>48.2692</td>
      <td>OUT018</td>
      <td>2009</td>
      <td>Medium</td>
      <td>Tier 3</td>
      <td>Supermarket Type2</td>
      <td>443.4228</td>
    </tr>
    <tr>
      <th>2</th>
      <td>FDN15</td>
      <td>17.50</td>
      <td>Low Fat</td>
      <td>0.016760</td>
      <td>Meat</td>
      <td>141.6180</td>
      <td>OUT049</td>
      <td>1999</td>
      <td>Medium</td>
      <td>Tier 1</td>
      <td>Supermarket Type1</td>
      <td>2097.2700</td>
    </tr>
    <tr>
      <th>3</th>
      <td>FDX07</td>
      <td>19.20</td>
      <td>Regular</td>
      <td>0.000000</td>
      <td>Fruits and Vegetables</td>
      <td>182.0950</td>
      <td>OUT010</td>
      <td>1998</td>
      <td>NaN</td>
      <td>Tier 3</td>
      <td>Grocery Store</td>
      <td>732.3800</td>
    </tr>
    <tr>
      <th>4</th>
      <td>NCD19</td>
      <td>8.93</td>
      <td>Low Fat</td>
      <td>0.000000</td>
      <td>Household</td>
      <td>53.8614</td>
      <td>OUT013</td>
      <td>1987</td>
      <td>High</td>
      <td>Tier 3</td>
      <td>Supermarket Type1</td>
      <td>994.7052</td>
    </tr>
  </tbody>
</table>
</div>




```python
data.columns
```




    Index(['Item_Identifier', 'Item_Weight', 'Item_Fat_Content', 'Item_Visibility',
           'Item_Type', 'Item_MRP', 'Outlet_Identifier',
           'Outlet_Establishment_Year', 'Outlet_Size', 'Outlet_Location_Type',
           'Outlet_Type', 'Item_Outlet_Sales'],
          dtype='object')




```python
#changing the column header to upper case
data.columns=data.columns.str.upper()
```


```python
data.columns
```




    Index(['ITEM_IDENTIFIER', 'ITEM_WEIGHT', 'ITEM_FAT_CONTENT', 'ITEM_VISIBILITY',
           'ITEM_TYPE', 'ITEM_MRP', 'OUTLET_IDENTIFIER',
           'OUTLET_ESTABLISHMENT_YEAR', 'OUTLET_SIZE', 'OUTLET_LOCATION_TYPE',
           'OUTLET_TYPE', 'ITEM_OUTLET_SALES'],
          dtype='object')




```python
#checking duplicate rows in the dataset
data[data.duplicated()]
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
      <th>ITEM_IDENTIFIER</th>
      <th>ITEM_WEIGHT</th>
      <th>ITEM_FAT_CONTENT</th>
      <th>ITEM_VISIBILITY</th>
      <th>ITEM_TYPE</th>
      <th>ITEM_MRP</th>
      <th>OUTLET_IDENTIFIER</th>
      <th>OUTLET_ESTABLISHMENT_YEAR</th>
      <th>OUTLET_SIZE</th>
      <th>OUTLET_LOCATION_TYPE</th>
      <th>OUTLET_TYPE</th>
      <th>ITEM_OUTLET_SALES</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>
</div>




```python
data.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 8523 entries, 0 to 8522
    Data columns (total 12 columns):
     #   Column                     Non-Null Count  Dtype  
    ---  ------                     --------------  -----  
     0   ITEM_IDENTIFIER            8523 non-null   object 
     1   ITEM_WEIGHT                7060 non-null   float64
     2   ITEM_FAT_CONTENT           8523 non-null   object 
     3   ITEM_VISIBILITY            8523 non-null   float64
     4   ITEM_TYPE                  8523 non-null   object 
     5   ITEM_MRP                   8523 non-null   float64
     6   OUTLET_IDENTIFIER          8523 non-null   object 
     7   OUTLET_ESTABLISHMENT_YEAR  8523 non-null   int64  
     8   OUTLET_SIZE                6113 non-null   object 
     9   OUTLET_LOCATION_TYPE       8523 non-null   object 
     10  OUTLET_TYPE                8523 non-null   object 
     11  ITEM_OUTLET_SALES          8523 non-null   float64
    dtypes: float64(4), int64(1), object(7)
    memory usage: 799.2+ KB
    


```python
#checking the number of null values in each column
data.isnull().any()
```




    ITEM_IDENTIFIER              False
    ITEM_WEIGHT                   True
    ITEM_FAT_CONTENT             False
    ITEM_VISIBILITY              False
    ITEM_TYPE                    False
    ITEM_MRP                     False
    OUTLET_IDENTIFIER            False
    OUTLET_ESTABLISHMENT_YEAR    False
    OUTLET_SIZE                   True
    OUTLET_LOCATION_TYPE         False
    OUTLET_TYPE                  False
    ITEM_OUTLET_SALES            False
    dtype: bool




```python
#checking the number of null values in each column
data.isnull().sum()
```




    ITEM_IDENTIFIER                 0
    ITEM_WEIGHT                  1463
    ITEM_FAT_CONTENT                0
    ITEM_VISIBILITY                 0
    ITEM_TYPE                       0
    ITEM_MRP                        0
    OUTLET_IDENTIFIER               0
    OUTLET_ESTABLISHMENT_YEAR       0
    OUTLET_SIZE                  2410
    OUTLET_LOCATION_TYPE            0
    OUTLET_TYPE                     0
    ITEM_OUTLET_SALES               0
    dtype: int64




```python
#To fill the null values in the data
data['ITEM_WEIGHT'].value_counts()
```




    12.150    86
    17.600    82
    13.650    77
    11.800    76
    15.100    68
              ..
    7.560      2
    9.420      1
    5.400      1
    6.520      1
    7.685      1
    Name: ITEM_WEIGHT, Length: 415, dtype: int64




```python
data=data.fillna(0)
data
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
      <th>ITEM_IDENTIFIER</th>
      <th>ITEM_WEIGHT</th>
      <th>ITEM_FAT_CONTENT</th>
      <th>ITEM_VISIBILITY</th>
      <th>ITEM_TYPE</th>
      <th>ITEM_MRP</th>
      <th>OUTLET_IDENTIFIER</th>
      <th>OUTLET_ESTABLISHMENT_YEAR</th>
      <th>OUTLET_SIZE</th>
      <th>OUTLET_LOCATION_TYPE</th>
      <th>OUTLET_TYPE</th>
      <th>ITEM_OUTLET_SALES</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>FDA15</td>
      <td>9.300</td>
      <td>Low Fat</td>
      <td>0.016047</td>
      <td>Dairy</td>
      <td>249.8092</td>
      <td>OUT049</td>
      <td>1999</td>
      <td>Medium</td>
      <td>Tier 1</td>
      <td>Supermarket Type1</td>
      <td>3735.1380</td>
    </tr>
    <tr>
      <th>1</th>
      <td>DRC01</td>
      <td>5.920</td>
      <td>Regular</td>
      <td>0.019278</td>
      <td>Soft Drinks</td>
      <td>48.2692</td>
      <td>OUT018</td>
      <td>2009</td>
      <td>Medium</td>
      <td>Tier 3</td>
      <td>Supermarket Type2</td>
      <td>443.4228</td>
    </tr>
    <tr>
      <th>2</th>
      <td>FDN15</td>
      <td>17.500</td>
      <td>Low Fat</td>
      <td>0.016760</td>
      <td>Meat</td>
      <td>141.6180</td>
      <td>OUT049</td>
      <td>1999</td>
      <td>Medium</td>
      <td>Tier 1</td>
      <td>Supermarket Type1</td>
      <td>2097.2700</td>
    </tr>
    <tr>
      <th>3</th>
      <td>FDX07</td>
      <td>19.200</td>
      <td>Regular</td>
      <td>0.000000</td>
      <td>Fruits and Vegetables</td>
      <td>182.0950</td>
      <td>OUT010</td>
      <td>1998</td>
      <td>0</td>
      <td>Tier 3</td>
      <td>Grocery Store</td>
      <td>732.3800</td>
    </tr>
    <tr>
      <th>4</th>
      <td>NCD19</td>
      <td>8.930</td>
      <td>Low Fat</td>
      <td>0.000000</td>
      <td>Household</td>
      <td>53.8614</td>
      <td>OUT013</td>
      <td>1987</td>
      <td>High</td>
      <td>Tier 3</td>
      <td>Supermarket Type1</td>
      <td>994.7052</td>
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
    </tr>
    <tr>
      <th>8518</th>
      <td>FDF22</td>
      <td>6.865</td>
      <td>Low Fat</td>
      <td>0.056783</td>
      <td>Snack Foods</td>
      <td>214.5218</td>
      <td>OUT013</td>
      <td>1987</td>
      <td>High</td>
      <td>Tier 3</td>
      <td>Supermarket Type1</td>
      <td>2778.3834</td>
    </tr>
    <tr>
      <th>8519</th>
      <td>FDS36</td>
      <td>8.380</td>
      <td>Regular</td>
      <td>0.046982</td>
      <td>Baking Goods</td>
      <td>108.1570</td>
      <td>OUT045</td>
      <td>2002</td>
      <td>0</td>
      <td>Tier 2</td>
      <td>Supermarket Type1</td>
      <td>549.2850</td>
    </tr>
    <tr>
      <th>8520</th>
      <td>NCJ29</td>
      <td>10.600</td>
      <td>Low Fat</td>
      <td>0.035186</td>
      <td>Health and Hygiene</td>
      <td>85.1224</td>
      <td>OUT035</td>
      <td>2004</td>
      <td>Small</td>
      <td>Tier 2</td>
      <td>Supermarket Type1</td>
      <td>1193.1136</td>
    </tr>
    <tr>
      <th>8521</th>
      <td>FDN46</td>
      <td>7.210</td>
      <td>Regular</td>
      <td>0.145221</td>
      <td>Snack Foods</td>
      <td>103.1332</td>
      <td>OUT018</td>
      <td>2009</td>
      <td>Medium</td>
      <td>Tier 3</td>
      <td>Supermarket Type2</td>
      <td>1845.5976</td>
    </tr>
    <tr>
      <th>8522</th>
      <td>DRG01</td>
      <td>14.800</td>
      <td>Low Fat</td>
      <td>0.044878</td>
      <td>Soft Drinks</td>
      <td>75.4670</td>
      <td>OUT046</td>
      <td>1997</td>
      <td>Small</td>
      <td>Tier 1</td>
      <td>Supermarket Type1</td>
      <td>765.6700</td>
    </tr>
  </tbody>
</table>
<p>8523 rows × 12 columns</p>
</div>




```python
#checking the mode of the data in OUTLET_SIZE
data['OUTLET_SIZE'].mode()[0]
```




    'Medium'




```python
#using the mode to fill in the empty rows in the OUTLET_SIZE column
#filling the empty rows in outlet_size with the column mode
data['OUTLET_SIZE'].replace(['null'],['medium'], inplace=True) 
data
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
      <th>ITEM_IDENTIFIER</th>
      <th>ITEM_WEIGHT</th>
      <th>ITEM_FAT_CONTENT</th>
      <th>ITEM_VISIBILITY</th>
      <th>ITEM_TYPE</th>
      <th>ITEM_MRP</th>
      <th>OUTLET_IDENTIFIER</th>
      <th>OUTLET_ESTABLISHMENT_YEAR</th>
      <th>OUTLET_SIZE</th>
      <th>OUTLET_LOCATION_TYPE</th>
      <th>OUTLET_TYPE</th>
      <th>ITEM_OUTLET_SALES</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>FDA15</td>
      <td>9.300</td>
      <td>Low Fat</td>
      <td>0.016047</td>
      <td>Dairy</td>
      <td>249.8092</td>
      <td>OUT049</td>
      <td>1999</td>
      <td>Medium</td>
      <td>Tier 1</td>
      <td>Supermarket Type1</td>
      <td>3735.1380</td>
    </tr>
    <tr>
      <th>1</th>
      <td>DRC01</td>
      <td>5.920</td>
      <td>Regular</td>
      <td>0.019278</td>
      <td>Soft Drinks</td>
      <td>48.2692</td>
      <td>OUT018</td>
      <td>2009</td>
      <td>Medium</td>
      <td>Tier 3</td>
      <td>Supermarket Type2</td>
      <td>443.4228</td>
    </tr>
    <tr>
      <th>2</th>
      <td>FDN15</td>
      <td>17.500</td>
      <td>Low Fat</td>
      <td>0.016760</td>
      <td>Meat</td>
      <td>141.6180</td>
      <td>OUT049</td>
      <td>1999</td>
      <td>Medium</td>
      <td>Tier 1</td>
      <td>Supermarket Type1</td>
      <td>2097.2700</td>
    </tr>
    <tr>
      <th>3</th>
      <td>FDX07</td>
      <td>19.200</td>
      <td>Regular</td>
      <td>0.000000</td>
      <td>Fruits and Vegetables</td>
      <td>182.0950</td>
      <td>OUT010</td>
      <td>1998</td>
      <td>medium</td>
      <td>Tier 3</td>
      <td>Grocery Store</td>
      <td>732.3800</td>
    </tr>
    <tr>
      <th>4</th>
      <td>NCD19</td>
      <td>8.930</td>
      <td>Low Fat</td>
      <td>0.000000</td>
      <td>Household</td>
      <td>53.8614</td>
      <td>OUT013</td>
      <td>1987</td>
      <td>High</td>
      <td>Tier 3</td>
      <td>Supermarket Type1</td>
      <td>994.7052</td>
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
    </tr>
    <tr>
      <th>8518</th>
      <td>FDF22</td>
      <td>6.865</td>
      <td>Low Fat</td>
      <td>0.056783</td>
      <td>Snack Foods</td>
      <td>214.5218</td>
      <td>OUT013</td>
      <td>1987</td>
      <td>High</td>
      <td>Tier 3</td>
      <td>Supermarket Type1</td>
      <td>2778.3834</td>
    </tr>
    <tr>
      <th>8519</th>
      <td>FDS36</td>
      <td>8.380</td>
      <td>Regular</td>
      <td>0.046982</td>
      <td>Baking Goods</td>
      <td>108.1570</td>
      <td>OUT045</td>
      <td>2002</td>
      <td>medium</td>
      <td>Tier 2</td>
      <td>Supermarket Type1</td>
      <td>549.2850</td>
    </tr>
    <tr>
      <th>8520</th>
      <td>NCJ29</td>
      <td>10.600</td>
      <td>Low Fat</td>
      <td>0.035186</td>
      <td>Health and Hygiene</td>
      <td>85.1224</td>
      <td>OUT035</td>
      <td>2004</td>
      <td>Small</td>
      <td>Tier 2</td>
      <td>Supermarket Type1</td>
      <td>1193.1136</td>
    </tr>
    <tr>
      <th>8521</th>
      <td>FDN46</td>
      <td>7.210</td>
      <td>Regular</td>
      <td>0.145221</td>
      <td>Snack Foods</td>
      <td>103.1332</td>
      <td>OUT018</td>
      <td>2009</td>
      <td>Medium</td>
      <td>Tier 3</td>
      <td>Supermarket Type2</td>
      <td>1845.5976</td>
    </tr>
    <tr>
      <th>8522</th>
      <td>DRG01</td>
      <td>14.800</td>
      <td>Low Fat</td>
      <td>0.044878</td>
      <td>Soft Drinks</td>
      <td>75.4670</td>
      <td>OUT046</td>
      <td>1997</td>
      <td>Small</td>
      <td>Tier 1</td>
      <td>Supermarket Type1</td>
      <td>765.6700</td>
    </tr>
  </tbody>
</table>
<p>8523 rows × 12 columns</p>
</div>




```python
data.head()
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
      <th>ITEM_IDENTIFIER</th>
      <th>ITEM_WEIGHT</th>
      <th>ITEM_FAT_CONTENT</th>
      <th>ITEM_VISIBILITY</th>
      <th>ITEM_TYPE</th>
      <th>ITEM_MRP</th>
      <th>OUTLET_IDENTIFIER</th>
      <th>OUTLET_ESTABLISHMENT_YEAR</th>
      <th>OUTLET_SIZE</th>
      <th>OUTLET_LOCATION_TYPE</th>
      <th>OUTLET_TYPE</th>
      <th>ITEM_OUTLET_SALES</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>FDA15</td>
      <td>9.30</td>
      <td>Low Fat</td>
      <td>0.016047</td>
      <td>Dairy</td>
      <td>249.8092</td>
      <td>OUT049</td>
      <td>1999</td>
      <td>Medium</td>
      <td>Tier 1</td>
      <td>Supermarket Type1</td>
      <td>3735.1380</td>
    </tr>
    <tr>
      <th>1</th>
      <td>DRC01</td>
      <td>5.92</td>
      <td>Regular</td>
      <td>0.019278</td>
      <td>Soft Drinks</td>
      <td>48.2692</td>
      <td>OUT018</td>
      <td>2009</td>
      <td>Medium</td>
      <td>Tier 3</td>
      <td>Supermarket Type2</td>
      <td>443.4228</td>
    </tr>
    <tr>
      <th>2</th>
      <td>FDN15</td>
      <td>17.50</td>
      <td>Low Fat</td>
      <td>0.016760</td>
      <td>Meat</td>
      <td>141.6180</td>
      <td>OUT049</td>
      <td>1999</td>
      <td>Medium</td>
      <td>Tier 1</td>
      <td>Supermarket Type1</td>
      <td>2097.2700</td>
    </tr>
    <tr>
      <th>3</th>
      <td>FDX07</td>
      <td>19.20</td>
      <td>Regular</td>
      <td>0.000000</td>
      <td>Fruits and Vegetables</td>
      <td>182.0950</td>
      <td>OUT010</td>
      <td>1998</td>
      <td>medium</td>
      <td>Tier 3</td>
      <td>Grocery Store</td>
      <td>732.3800</td>
    </tr>
    <tr>
      <th>4</th>
      <td>NCD19</td>
      <td>8.93</td>
      <td>Low Fat</td>
      <td>0.000000</td>
      <td>Household</td>
      <td>53.8614</td>
      <td>OUT013</td>
      <td>1987</td>
      <td>High</td>
      <td>Tier 3</td>
      <td>Supermarket Type1</td>
      <td>994.7052</td>
    </tr>
  </tbody>
</table>
</div>




```python

```
