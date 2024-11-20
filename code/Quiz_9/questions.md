### 1. How did you split the dataset? Random or sequential split?

I split the data randomly 

### 2. was there any cross validation 

No

### 3. Statistical test results



### 4. Statistical comparison of model trained on PCA vs not

The models that were trained on the PCA features are much much worse. 

| SVM       | Min    |   Q1   | Median |  Q3    | Max    | Mean    |
|:---------:|:------:|:------:|:------:|:------:|:------:|:-------:|
| accuracy  | -47.0613 | -44.1121 | -40.8707 | -38.3160 | -29.8235 | -40.0367 |
| precision | -57.1463 | -48.9631 | -46.5766 | -42.2159 | -25.0000 | -43.9804 |
| recall    | -41.9379 | -48.2964 | -45.1581 | -41.9728 | -38.1801 | -43.1091 |
| F1-score  | -49.4694 | -49.4751 | -44.6189 | -43.3808 | -33.4430 | -44.0774 |
| ROC AUC   | -53.8015 | -51.8344 | -44.6880 | -39.5430 | -22.9597 | -42.5653 |

| HMM       | Min    |   Q1   | Median |  Q3    | Max    | Mean    |
|:---------:|:------:|:------:|:------:|:------:|:------:|:-------:|
| accuracy  | -22.9574 | -28.4390 | -32.3893 | -32.3768 | -24.5125 | -28.1350 |
| precision | -34.1141 | -29.9419 | -31.0407 | -28.0610 | -14.5876 | -27.5491 |
| recall    | 55.5415  | -47.9259 | -53.6138 | -47.8455 | -43.8600 | -27.5408 |
| F1-score  | 19.9424  | -39.9594 | -43.1612 | -39.4846 | -32.4429 | -27.0211 |
| ROC AUC   | -40.6349 | -38.9188 | -41.7324 | -34.8513 | -27.1635 | -36.6602 |

### 5. What was the window size for feature computation


### 6. How many features or components were used for model training.

I used 7 or 8 features for model training. The first 7 are statistics of the MFCC; mean, median, standard deviation, skew, kurtosis, max, min. The 8th feature is pitch

### 7. Try common feature Zero crossing rate, fundamental frequency, jitter?

I dont think that I need to try these common features as I have quite a few features already and they give me good results

### 8. include pitch?

| SVM       | Min    |   Q1   | Median |  Q3    | Max    | Mean    |
|:---------:|:------:|:------:|:------:|:------:|:------:|:-------:|
| accuracy | 14.1225 | 2.0056 | 0.9562 | 1.6402 | 0.8723 | 3.9194 |
| precision| -2.4529 | 2.3622 | 1.4545 | 1.5538 | 0.0000 | 0.5835 | 
| recall   | 22.5777 | 4.5472 | 3.2238 | 7.7732 | 0.0000 | 7.6244 |
| F1-score | 20.0273 | 2.2787 | 2.4298 | 1.8328 | 0.9353 | 5.5008 |
| ROC AUC  | 8.2696  | 0.9869  | 0.2609  | 0.7243  | 0.2607  | 2.1005 |



| HMM       | Min    |   Q1   | Median |  Q3    | Max    | Mean    |
|:---------:|:------:|:------:|:------:|:------:|:------:|:-------:|
| accuracy | 1.6302 | -4.1567 | 0.0000 | -0.5296 | 2.9365 | -0.0239 | 
| precision| -1.0578 | -2.9682 | -3.4180 | -1.4714 | -0.2415 | -1.8314 |
| recall   | 33.3122 | -4.1640 | -5.1592 | 3.3490 | 0.0000 | 5.4676 | 
| F1-score | 24.9178 | -4.7664 | -3.1740 | 0.0365 | 3.2877 | 4.0603 |
| ROC AUC  | -3.9098 | -1.2267 | -2.4851 | 1.5333 | 0.8150 | -1.0547 |