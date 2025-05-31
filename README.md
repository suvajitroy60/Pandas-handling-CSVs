<a href="https://colab.research.google.com/github/suvajitroy60/Pandas-handling-CSVs/blob/main/Snippets_Importing_libraries.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

# Importing a library handling CSV

To import a library that's not in Colaboratory by default, you can use `!pip install` or `!apt-get install`.


```
!pip install pandas as pd

```

    Requirement already satisfied: pandas in /usr/local/lib/python3.11/dist-packages (2.2.2)
    Requirement already satisfied: numpy>=1.23.2 in /usr/local/lib/python3.11/dist-packages (from pandas) (2.0.2)
    Requirement already satisfied: python-dateutil>=2.8.2 in /usr/local/lib/python3.11/dist-packages (from pandas) (2.9.0.post0)
    Requirement already satisfied: pytz>=2020.1 in /usr/local/lib/python3.11/dist-packages (from pandas) (2025.2)
    Requirement already satisfied: tzdata>=2022.7 in /usr/local/lib/python3.11/dist-packages (from pandas) (2025.2)
    Requirement already satisfied: six>=1.5 in /usr/local/lib/python3.11/dist-packages (from python-dateutil>=2.8.2->pandas) (1.17.0)



```
import pandas as pd

# Replace with the raw link to your CSV file on GitHub
github_csv_url = 'https://raw.githubusercontent.com/suvajitroy60/Pandas-handling-CSVs/refs/heads/main/warmup-data/coffee.csv'

coffee = pd.read_csv(github_csv_url)

# Display the first few rows to verify
print(" Coffee Shop :")
print(coffee.head())
```

     Coffee Shop :
             Item Category  Price  In_Stock
    0    Espresso    Drink   3.50      True
    1       Latte    Drink   4.00      True
    2  Cappuccino    Drink   4.25      True
    3   Croissant   Pastry   2.50      True
    4      Muffin   Pastry   2.75     False


# Create a sample DataFrame


```
data = {
    'Day': ['Monday', 'Monday', 'Tuesday', 'Tuesday', 'Wednesday', 'Wednesday',
            'Thursday', 'Thursday', 'Friday', 'Friday', 'Saturday', 'Saturday',
            'Sunday', 'Sunday'],
    'Coffee Type': ['Espresso', 'Latte', 'Espresso', 'Latte', 'Espresso', 'Latte',
                    'Espresso', 'Latte', 'Espresso', 'Latte', 'Espresso', 'Latte',
                    'Espresso', 'Latte'],
    'Price': [25, 15, 30, 20, 35, 25, 40, 30, 45, 35, 45, 35, 45, 35]
}

df = pd.DataFrame(data)
print(df)

df.describe()

```

              Day Coffee Type  Price
    0      Monday    Espresso     25
    1      Monday       Latte     15
    2     Tuesday    Espresso     30
    3     Tuesday       Latte     20
    4   Wednesday    Espresso     35
    5   Wednesday       Latte     25
    6    Thursday    Espresso     40
    7    Thursday       Latte     30
    8      Friday    Espresso     45
    9      Friday       Latte     35
    10   Saturday    Espresso     45
    11   Saturday       Latte     35
    12     Sunday    Espresso     45
    13     Sunday       Latte     35






  <div id="df-0c1ac3b9-584a-4b5b-a718-885926960334" class="colab-df-container">
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
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>14.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>32.857143</td>
    </tr>
    <tr>
      <th>std</th>
      <td>9.346798</td>
    </tr>
    <tr>
      <th>min</th>
      <td>15.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>26.250000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>35.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>38.750000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>45.000000</td>
    </tr>
  </tbody>
</table>
</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-0c1ac3b9-584a-4b5b-a718-885926960334')"
            title="Convert this dataframe to an interactive table."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"/>
  </svg>
    </button>

  <style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

    <script>
      const buttonEl =
        document.querySelector('#df-0c1ac3b9-584a-4b5b-a718-885926960334 button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-0c1ac3b9-584a-4b5b-a718-885926960334');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
  </div>


    <div id="df-08aa1d7a-11f1-4eba-b2fe-79c497552c04">
      <button class="colab-df-quickchart" onclick="quickchart('df-08aa1d7a-11f1-4eba-b2fe-79c497552c04')"
                title="Suggest charts"
                style="display:none;">

<svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
     width="24px">
    <g>
        <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"/>
    </g>
</svg>
      </button>

<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>

      <script>
        async function quickchart(key) {
          const quickchartButtonEl =
            document.querySelector('#' + key + ' button');
          quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
          quickchartButtonEl.classList.add('colab-df-spinner');
          try {
            const charts = await google.colab.kernel.invokeFunction(
                'suggestCharts', [key], {});
          } catch (error) {
            console.error('Error during call to suggestCharts:', error);
          }
          quickchartButtonEl.classList.remove('colab-df-spinner');
          quickchartButtonEl.classList.add('colab-df-quickchart-complete');
        }
        (() => {
          let quickchartButtonEl =
            document.querySelector('#df-08aa1d7a-11f1-4eba-b2fe-79c497552c04 button');
          quickchartButtonEl.style.display =
            google.colab.kernel.accessAllowed ? 'block' : 'none';
        })();
      </script>
    </div>

    </div>
  </div>





```
bios = pd.read_csv('https://raw.githubusercontent.com/suvajitroy60/Pandas-handling-CSVs/refs/heads/main/data/bios.csv')
results = pd.read_csv('https://raw.githubusercontent.com/suvajitroy60/Pandas-handling-CSVs/refs/heads/main/data/results.csv')


```

# Display the DataFrame


```
print("Original DataFrame:")
print(df)
```

    Original DataFrame:
              Day Coffee Type  Units Sold
    0      Monday    Espresso          25
    1      Monday       Latte          15
    2     Tuesday    Espresso          30
    3     Tuesday       Latte          20
    4   Wednesday    Espresso          35
    5   Wednesday       Latte          25
    6    Thursday    Espresso          40
    7    Thursday       Latte          30
    8      Friday    Espresso          45
    9      Friday       Latte          35
    10   Saturday    Espresso          45
    11   Saturday       Latte          35
    12     Sunday    Espresso          45
    13     Sunday       Latte          35


# --- Accessing Data ---

# Using .loc to access rows by label

print("\nAccessing row with index 1 using .loc:")
print(coffee.loc[1])

# Applying a function to a column


```

```


```
print("\nAccessing row at index 2 using .iloc:")
print(coffee.iloc[2])
```

    
    Accessing row at index 2 using .iloc:
    Day             Tuesday
    Coffee Type    Espresso
    Units Sold           30
    Name: 2, dtype: object



```
print("\nAccessing value at row label 0 and column 'Price' using .at:")
print(coffee.at[0, 'Price'])
```

    
    Accessing value at row label 0 and column 'Price' using .at:
    3.5



```
print("\nAccessing value at row index 3 and column index 1 (Category) using .iloc:")
print(coffee.iloc[3, 1])
```

    
    Accessing value at row index 3 and column index 1 (Category) using .iloc:
    Pastry


NumPy array first. However, for the operation of checking for substring presence, pandas .str.contains() is the recommended approach when working with DataFrames.
---
Sources
[https://numpy.org/doc/1.25/reference/routines.char.html](https://numpy.org/doc/1.25/reference/routines.char.html)
---


```
print("\nConverting 'Item' names to lowercase:")
coffee['Item_lower'] = coffee['Item'].str.lower()
print(coffee)
```

    
    Checking if 'col2' contains the letter 'A':
       col1 col2  col3  col1_squared col2_lower  col2_contains_A
    0     1    A  10.1             1          a             True
    1     2    B  11.2             4          b            False
    2     3    C  12.3             9          c            False
    3     4    D  13.4            16          d            False
    4     5    E   NaN            25          e            False



```
print("\nChecking if 'Category' contains the substring 'Dr':")
coffee['Is_Drink_Category'] = coffee['Category'].str.contains('Dr')
print(coffee)
```




```
print("\nSelecting a single column ('Price'):")
print(coffee['Price'])
```


```
print("\nSelecting multiple columns ('Item' and 'Price'):")
print(coffee[['Item', 'Price']])
```

# Filtering Values


```
print("\nFiltering rows where 'Price' is greater than 4.00:")
print(coffee[coffee['Price'] > 4.00])
```


```
print("\nFiltering rows where 'Category' is 'Drink' AND 'In_Stock' is True:")
print(coffee[(coffee['Category'] == 'Drink') & (coffee['In_Stock'] == True)])
```

    
    Filtering rows where 'Category' is 'Drink' AND 'In_Stock' is True:
             Item Category  Price  In_Stock
    0    Espresso    Drink   3.50      True
    1       Latte    Drink   4.00      True
    2  Cappuccino    Drink   4.25      True


# Null Remove


```
print("\nDataFrame after dropping rows with null values:")
print(coffee.dropna())
```

    
    DataFrame after dropping rows with null values:
             Item Category  Price  In_Stock
    0    Espresso    Drink   3.50      True
    1       Latte    Drink   4.00      True
    2  Cappuccino    Drink   4.25      True
    3   Croissant   Pastry   2.50      True
    4      Muffin   Pastry   2.75     False
    5    Sandwich     Food   5.00      True
    6       Salad     Food   6.00      True



```
print("\nDataFrame after filling null values with 0 (e.g., for missing stock counts):")
print(coffee.fillna(0))
```

    
    DataFrame after filling null values with 0 (e.g., for missing stock counts):
             Item Category  Price  In_Stock
    0    Espresso    Drink   3.50      True
    1       Latte    Drink   4.00      True
    2  Cappuccino    Drink   4.25      True
    3   Croissant   Pastry   2.50      True
    4      Muffin   Pastry   2.75     False
    5    Sandwich     Food   5.00      True
    6       Salad     Food   6.00      True



```
print("\nDescriptive statistics for numerical columns:")
print(coffee.describe())
```

    
    Descriptive statistics for numerical columns:
           Units Sold
    count   14.000000
    mean    32.857143
    std      9.346798
    min     15.000000
    25%     26.250000
    50%     35.000000
    75%     38.750000
    max     45.000000



```
print("\nGrouping by 'Category' and calculating the average 'Price':")
print(coffee.groupby('Category')['Price'].mean())
```

    
    Grouping by 'Category' and calculating the average 'Price':
    Category
    Drink     3.916667
    Food      5.500000
    Pastry    2.625000
    Name: Price, dtype: float64



```
print("\nSorting by 'Price' in ascending order:")
print(coffee.sort_values(by='Price'))
```

    
    Sorting by 'Price' in ascending order:
             Item Category  Price  In_Stock
    3   Croissant   Pastry   2.50      True
    4      Muffin   Pastry   2.75     False
    0    Espresso    Drink   3.50      True
    1       Latte    Drink   4.00      True
    2  Cappuccino    Drink   4.25      True
    5    Sandwich     Food   5.00      True
    6       Salad     Food   6.00      True



```
print(coffee.groupby ('Category')['Price'].mean())
```

    Category
    Drink     3.916667
    Food      5.500000
    Pastry    2.625000
    Name: Price, dtype: float64



```
print("\nSorting by 'In_Stock' (False first, then True):")
print(coffee.sort_values(by='In_Stock'))
```

    
    Sorting by 'In_Stock' (False first, then True):
             Item Category  Price  In_Stock
    4      Muffin   Pastry   2.75     False
    0    Espresso    Drink   3.50      True
    1       Latte    Drink   4.00      True
    2  Cappuccino    Drink   4.25      True
    3   Croissant   Pastry   2.50      True
    5    Sandwich     Food   5.00      True
    6       Salad     Food   6.00      True

