# Beijing Air Quality Forecasting

## Project Overview

This project aims to predict PM2.5 levels in Beijing using historical air quality and weather data. PM2.5 is a key air quality measure representing fine particulate matter hazardous to human health. Accurate forecasting enables proactive measures to mitigate air pollution effects.


We employ various machine learning techniques, particularly Recurrent Neural Networks (RNNs) and Long Short-Term Memory (LSTM) models, to capture temporal dependencies in the data.


### File Structure:
```
.
├── notebooks/
│   ├── visualizations.ipynb
│   └── beijing_air_quality_forecasting.ipynb
├── submissions/
│   ├── model1_submission.csv
│   ├── model2_submission.csv
│   ├── model3_submission.csv
│   ├── model4_submission.csv
│   ├── model5_submission.csv
│   └── ...
├── data/
│   ├── train.csv
│   └── test.csv
└── README.md
```

### Getting Started
#### Prerequisites
- Python 3.7+
- Required packages: numpy, pandas, matplotlib, scikit-learn, tensorflow
#### Installation

1. Clone the repository
2. Create and activate a virtual environment
3. Install requirements

### Reproducing Results
#### 1. Data Preparation
The data/ folder contains the raw train and test datasets. If you need to download the data manually:

```
! pip install kaggle
! mkdir ~/.kaggle
! cp kaggle.json ~/.kaggle/
! chmod 600 ~/.kaggle/kaggle.json
! kaggle competitions download -c assignment-1-time-series-forecasting-may-2025
! mkdir 'data' && unzip assignment-1-time-series-forecasting-may-2025.zip -d data
```

#### 2. Exploratory Data Analysis and Preprocessing
Run the preprocessing notebook to understand data characteristics and prepare data for modeling

#### 3. Model Development and Training
Execute the model development notebook to train various forecasting models. 

#### 4. Generate Submissions
After training models, submission files will be automatically generated in the submissions/ folder.
##### Submission Files
Each submission file in the submissions/ directory corresponds to a different model architecture:
- model1_submission.csv: Basic LSTM model
- model2_submission.csv: Deeper LSTM model
- model3_submission.csv: Bidirectional LSTM model
- model4_submission.csv: GRU with Batch Normalization (best performing model)
- model5_submission.csv: Hybrid CNN-LSTM model
... (other model submissions)

#### Results and Discussion
Model performance can be evaluated through validation scores. The project demonstrates systematic improvements through various model architectures, with the GRU-based model with Batch Normalization achieving the best results.


#### License
This project is licensed under the MIT License - see the LICENSE file for details.

#### Acknowledgements
Data source: Kaggle Beijing Air Quality Forecasting Competition (May 2025)