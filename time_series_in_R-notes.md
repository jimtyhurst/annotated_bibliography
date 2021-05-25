# Time Series in R: Notes

**Contents**

* [Rob Hyndman: R libraries](#rob-hyndman-r-libraries)
* [Book: _Forecasting: Principles and Practice_](#book-forecasting-principles-and-practice)
* [Facebook: `prophet` package](#facebook-prophet-package)
* [Google: `CausalImpact` package](#google-causalimpact-package)
* [Twitter: AnomalyDetection](#twitter-anomalydetection)
* [Matt Dancho: R libraries](#matt-dancho-r-libraries)
* [Matt Dancho: High-Performance Time Series Forecasting course](#matt-dancho-high-performance-time-series-forecasting-course)
* [R Books](#r-books)
* [Python Books](#python-books)

---

## Rob Hyndman: R libraries
* [tsibble](https://cran.r-project.org/package=tsibble): Tidy Temporal Data Frames and Tools.
* [fable](https://cran.r-project.org/package=fable): Forecasting Models for Tidy Time Series.
* [feasts](https://cran.r-project.org/package=feasts): Feature Extraction and Statistics for Time Series.

## Book: _Forecasting: Principles and Practice_
Rob J. Hyndman. 2021. [Forecasting: Principles and Practice](https://otexts.com/fpp3/), 3rd edition. Free to read online.

## Facebook: `prophet` package
* [prophet](https://cran.r-project.org/package=prophet) package: Automatic Forecasting Procedure.
    * "Implements a procedure for forecasting time series data based on an additive model where non-linear trends are fit with yearly, weekly, and daily seasonality, plus holiday effects. It works best with time series that have strong seasonal effects and several seasons of historical data. Prophet is robust to missing data and shifts in the trend, and typically handles outliers well."
* [Prophet](https://facebook.github.io/prophet/): Forecasting at scale. home page.
* Prophet [Quick Start](https://facebook.github.io/prophet/docs/quick_start.html). documentation.
* Sean J. Taylor, Ben Letham. 2017-02-23. [Prophet: forecasting at scale](https://research.fb.com/blog/2017/02/prophet-forecasting-at-scale/). Blog post.

## Google: `CausalImpact` package
* [CausalImpact](https://cran.r-project.org/package=CausalImpact): Inferring Causal Effects using Bayesian Structural Time-Series Models.
* [CausalImpact: An R package for causal inference in time series](https://google.github.io/CausalImpact/).

## Twitter: AnomalyDetection
* [AnomalyDetection](https://github.com/twitter/AnomalyDetection). GitHub repository.

## Matt Dancho: R libraries
* [timetk](https://cran.r-project.org/package=timetk): A Tool Kit for Working with Time Series in R.
    * data wrangling
    * visualization
    * feature engineering
* [modeltime](https://cran.r-project.org/package=modeltime): The Tidymodels Extension for Time Series Modeling.
    * fast experimentation with many software models.

## Matt Dancho: High-Performance Time Series Forecasting course
https://university.business-science.io/p/ds4b-203-r-high-performance-time-series-forecasting/

Cost: $499

Summary:

* Part 1 - Feature Engineering with [timetk](https://cran.r-project.org/package=timetk)
* Part 2 - Machine Learning with [modeltime](https://cran.r-project.org/package=modeltime)
* Part 3 - Deep Learning with [GluonTS](https://gluon-ts.mxnet.io/)
* Challenges & Cheat Sheets

Details:

* part 1: Feature Engineering
    * Competition overview: 5 competitions and strategies that won. 30 min.
    * TS Jumpstart. 1+ hr.
    * Visualization. 1.5 hr.
    * Wrangling. 1.5 hr.
    * Transformation. 1.5 hr.
    * Feature engineering. 3 hr.
* Part 2: Machine Learning and Forecasting
    * ARIMA: 1.5 hrs.
    * Prophet: 45 min.
    * ETS, TBATS, Seasonal Decomp. 1 hr.
    * Machine Learning: GLMNet, KNN, RF, XGBoost, Rule Based. 2 hrs.
    * Boosted algorithms: Prophet, ARIMA. 30 min.
    * Hyper Parameter Tuning and Cross Validation. 1+ hrs.
    * Scalable Modeling and Time Series Groups. 1+ hrs.
    * Ensemble approaches: Averaging, Stacking. 1+ hrs.
* Part 3: Deep Learning
    * Deep Learning. several hours.
        * DeepAR
        * DeepVAR
        * NBeats
        * and more!

Use 3 libraries:

* [timetk](https://cran.r-project.org/package=timetk)
    * data wrangling
    * visualization
    * feature engineering
* [modeltime](https://cran.r-project.org/package=modeltime)
    * fast experimentation with many software models.
* [GluonTS](https://gluon-ts.mxnet.io/)
    * Python library is part of mxnet.
    * Deep Learning for time series.
    * developed at Amazon.
    * Use Reticulate to combine Gluon and R.

Related blogs:

* Time Series in 5-Minutes
    * Part 1: [Data Wrangling and Rolling Calculations](https://www.business-science.io/code-tools/2020/08/19/five-minute-time-series-rolling-calculations.html)
    * Part 2: [The Time Plot](https://www.business-science.io/code-tools/2020/06/08/five-minute-time-series-time-plot.html)
    * Part 3: [Autocorrelation](https://www.business-science.io/code-tools/2020/06/17/five-minute-time-series-part-2.html)
    * Part 4: [Seasonality](https://www.business-science.io/code-tools/2020/08/26/five-minute-time-series-seasonality.html)
    * Part 5: [Anomalies and Anomaly Detection](https://www.business-science.io/code-tools/2020/09/02/five-minute-time-series-anomaly-detection.html)
    * Part 6: [Modeling Time Series Data](https://www.business-science.io/code-tools/2020/09/09/five-minute-time-series-modeling-data.html)

## R Books
* Rob J. Hyndman. 2021. [Forecasting: Principles and Practice](https://otexts.com/fpp3/), 3rd edition. Free to read online.

## Python Books
* Aileen Nielsen. 2019. [Practical Time Series Analysis](https://learning.oreilly.com/library/view/practical-time-series/9781492041641/). O'Reilly Media, Inc.
* B.V. Vishwas, Ashish Patel. 2020. [Hands-on Time Series Analysis with Python: From Basics to Bleeding Edge Techniques](https://learning.oreilly.com/library/view/hands-on-time-series/9781484259924/). Apress.
