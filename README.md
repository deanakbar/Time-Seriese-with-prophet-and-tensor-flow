# Time Series Daily Climate

Analyze Temperature Trends: Look at past temperature data to understand how it changes throughout the year.

## Project Setup

### 1. Mount Google Drive

```python
from google.colab import drive
drive.mount("/content/gdrive", force_remount=True)
```

### 2. Load and Preprocess Data 
```import pandas as pd
#Read,train and test dataset
train_data = pd.read_csv("/content/gdrive/MyDrive/Time series/DailyDelhiClimateTrain.csv")
test_data = pd.read_csv("/content/gdrive/MyDrive/Time series/DailyDelhiClimateTest.csv")
```

### 3. Change date column datatype from object to datetime
```change date column datatype from object to datetime
train_data['date']= pd.to_datetime(train_data['date'])
test_data['date']= pd.to_datetime(test_data['date'])
```

### 4. Analyze Train dataset
    our analysis, we prioritize using temperature data over wind speed because temperature is more universally understood and meaningful to the general public.
    While wind speed has its relevance, temperature provides a more direct and relatable measure of weather conditions that people encounter daily.
    By focusing on temperature, we can present our findings in a way that is not only more accessible but also more actionable for those who may not have a technical background.
    This approach ensures that our insights are both useful and easily comprehensible to a wider audience.

### 5. Modeling
   ### 1. TensorFlow Neural Network

- **Description**: A neural network model implemented using TensorFlow.
- **Architecture**: ![image](https://github.com/user-attachments/assets/6a8f6b67-1ef5-46e3-95a8-d49e0102f365)

- **Performance**:
  - MAE (Mean Absolute Error): 15.91
  - [Add any additional performance metrics or details]

### 2. Prophet Time Series Forecasting

- **Description**: A forecasting model using the Prophet library, suitable for time series data.
- **Parameters**: [List any parameters or configurations used with Prophet]
- **Performance**:
  - MAE (Mean Absolute Error): 2.18

## Performance Comparison

| Model           | MAE  |
|-----------------|------|
| TensorFlow NN   | 15.91|
| Prophet         | 2.18 |

- **Observation**: The Prophet model outperforms the TensorFlow model significantly in terms of MAE.

