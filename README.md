**Overview**
- Developed a time series forecasting model to predict hourly visibility at JFK Airport using the LSTM and GRU models.

**Data Preprocessing**
- Loaded a cleaned weather dataset and converted the 'DATE' column to datetime format.
- Set the 'DATE' column as the index, dropped it from the Dataframe, and visualized the hourly visibility over time.
- Split the time series data into input sequences using a sliding window approach for a univariate model.
- Reshaped input data to fit the LSTM and GRU models and divided it into training, validation, and test sets.

**Methodology**
- Constructed an LSTM model with three layers: an LSTM layer, a ReLU dense layer, and a linear output layer.
- Compiled the model using Mean Squared Error loss and Root Mean Squared Error as a metric, with the Adam optimizer.
- Trained the model over 300 epochs with ModelCheckpoint to save the best model.
- Implemented a similar GRU model with three layers for comparison, trained, and saved the best model.

**Results**

### Multivariate Time Series Analysis

| Model | Train Loss | Validation Loss | Test Loss |
|-------|------------|-----------------|-----------|
| **LSTM** | 1.0077 | 1.0054 | 1.1556 |
| **GRU**  | 1.0039 | 1.0080 | 1.1390 |

### Univariate Time Series Analysis

| Model | Train Loss | Validation Loss | Test Loss |
|-------|------------|-----------------|-----------|
| **LSTM** | 1.0561 | 1.0490 | 1.1654 |
| **GRU**  | 1.0565 | 1.0478 | 1.1680 |
