---
layout: page
title: PM2.5 Prediction
description: Project testing various RNNs for short term PM2.5 prediction in the US
img: assets/img/3.jpg
importance: 2
category: work
giscus_comments: true
---

# Short Term Particulate Measurements
The EPA's IMPROVE and CSN networks are the USAs primary provider of accuract PM data. One drawback to these networks is that they require postprocessing of their data, which can take a few days time. Thus data is always a few days behind. This project uses RNN architectures to try to close that gap and predict real-time PM2.5 hourly concentrations based off of previously reported values.

# Data
Data was from a kaggle dataset showing hourly concentrations from 2014-2015 for all US monitoring sites (~8 million data points). High level statistics from 2014 were used and data from 2015 was used for training and testing. Outliers were detected and taken out based on validation accuracy increases.
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/rnn/site_data.PNG" title="Example Data" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/rnn/anomaly_detection.PNG" title="Anomaly Detection" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Example data from one monitoring site on left. The data is hourly and shows the PM2.5 concentration in ug/m^3.
    Anomaly detection results on right. The red dots are the data points which were removed, values are in ug/m^3.
</div>

# Models
All models were created with PyTorch and hyperparameters were tuned with Ray Tune. GRUs, LSTMs, and Vanilla RNNs were tested. Different prediction and data point lengths were also tested, in the end the best predictions came from using the past seven days to predict the next 3 days. The best performing model was a GRU with one recurrent layer and three dense layers trained for 100 epochs.

## Model Performance
The model was able to capture most of the variance in PM2.5, but had a hard time with extreme values. This makes sense since many of these events would be expected to be either a chance event (such as a truck driving by) or an annual event such as a forest fire. The past seven days of measurements would be unlikely to predict these scenarios.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/rnn/rnn_predictions.PNG" title="Model Performance" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Model prediction results. RMSE for each prediction ended at 5.01 ug/m^3, which is roughly in line with existing published models.
</div>
