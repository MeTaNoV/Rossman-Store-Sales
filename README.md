# Rossman-Store-Sales

## Introduction

To solve the test proposed, I will use:

- python >= 3.5
- virtualenv
- Jupyter notebook
- numpy / pandas / matplotlib / seaborn
- scikit-learn and TensorFlow

## Setup

Clone the following repository: `https://github.com/MeTaNoV/Rossman-Store-Sales.git`

```bash
cd /some/path/Rossman-Store-Sales
```

Setup the environment by using virtualenv:

```bash
virtualenv venv
```

Then activate the environment:

```bash
source venv/bin/activate (or source venv/Scripts/activate on windows)
```

And install the required package: (choose the proper requirents file w/ or w/o GPU, depending on your HW)

```bash
pip install -r requirement-gpu.txt
```

## Approach

We will conduct our experiment in two phases using Jupyter Notebooks.

The first will take care of data analysis and preparation.
The second will focus on model design and prediction.

A lot of people used XGboost to perform this challenge. I will myself focus on a DNN architecture for this challenge.

```bash
jupyter notebook
```

### Data Analysis and Preparation

Open the notebook named `Data - Analysis Cleaning Preparation.ipynb` and follow the instructions from there.

### Model Design and Prediction

Open the notebook named `Model - Design Prediction.ipynb` and follow the instructions from there.

## Conclusion

We can see that with a rather low effort in feature engineering and model design, we managed to have a model that performed
rather well with a RMSPE between 0.14 and 0.16 which does not enable us to reach the top of the leaderboard around 0.10 but which is far better than the simple Median DayOfWeek Benchmark which is 0.24.

Here is a list of actions which could increase our performance:

- do more feature engineering to take into account the temporal aspect of the data
- add external data like top contributors did with State, Weather or Google Trends data to enrich the given dataset
- if we keep a DNN, create a custom one taking into account the proper RMSPE loss and not RMSE
- instead, use a time series model like LSTM optionally completed by a convolutional layer
- do more fine parameter tuning