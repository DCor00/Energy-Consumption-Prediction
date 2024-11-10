# Energy Consumption Prediction and Forecasting

This repository contains a project developed for the **Master's Course in Artificial Intelligence for Science and Technology** at **University of Milano-Bicocca** (2024). The primary focus of the project is to predict and forecast energy consumption using various machine learning and data analysis techniques.

## Project Objectives

The primary goals of this project are:
1. **Data Preparation**: Preprocess the GREEND dataset for optimal model input.
2. **Model Evaluation**: Compare multiple forecasting models' performance on univariate and multivariate time series data.
3. **Generalization Testing**: Assess the model's performance on unseen data from different sensors and buildings.


## Models Used

The forecasting models include:
- **Baseline Model**: ARIMA (AutoRegressive Integrated Moving Average), a statistical method well-suited for univariate time series.
- **Deep Learning Models**:
  - **LSTM (Long Short-Term Memory)** and its variations: simple, multi-layered, and bidirectional, used to capture temporal dependencies.
  - **CNN (Convolutional Neural Network)**: For extracting spatial features from sequences.
  - **Hybrid Models**: ConvLSTM and 1D CNN combined with LSTM layers to leverage both spatial and temporal data patterns.
  - **GRU (Gated Recurrent Unit)**: A variation of RNN, which is more computationally efficient than LSTM.
 
**Univariate Models**: Initially, the models are tested on individual time series (one sensor at a time) to assess how well each model can predict based on the data from a single sensor.

**Multivariate Models**: The models are extended to handle data from an entire building as a multivariate time series, where multiple sensor readings are used to improve the accuracy and robustness of the forecasts.
  
The comparison between univariate and multivariate models helps evaluate whether treating the data as multivariate improves model generalization and performance.


## Evaluation Metrics

- **Mean Squared Error (MSE)**: MSE is the primary metric for model performance comparison.
- **Visualization**: Predictions and actual values are plotted to help visually interpret model performance.

## Generalization Testing

For further evaluation, a validation set from `building_0` is used, targeting a different sensor than that in `building_1`. This provides insights into how well models generalize to unseen data, a key measure of their adaptability.


## Dataset 
[GREEND Dataset](https://sourceforge.net/projects/greend/) is an energy dataset containing power measurements collected from multiple households in Austria and Italy. It provides detailed energy profiles on a per device basis with a sampling rate of 1 Hz.

Special thanks to the creators for making this data available for research and analysis.


## License 📜
See the [LICENSE](LICENSE) file for more details.

