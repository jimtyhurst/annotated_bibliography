# Time Series in R: Notes

**Contents**

* [Review of pre-tidyverse libraries](#review-of-pre-tidyverse-libraries)
* [Time series libraries compatible with the `tidyverse`](#time-series-libraries-compatible-with-the-tidyverse)
    * [Rob Hyndman: R libraries](#rob-hyndman-r-libraries)
    * [Matt Dancho: R libraries](#matt-dancho-r-libraries)
* [Facebook: `prophet` package](#facebook-prophet-package)
* [Twitter: AnomalyDetection](#twitter-anomalydetection)
* [Google: `CausalImpact` package](#google-causalimpact-package)
* [Online Courses](#online-courses)
    * [Coursera: Intro to Time Series Analysis in R](#coursera-intro-to-time-series-analysis-in-r)
    * [Coursera: Time series forecasting with Prophet](#coursera-time-series-forecasting-with-prophet)
    * [Georgia Institute of Technology: Introduction to Analytics Modeling](#georgia-institute-of-technology-introduction-to-analytics-modeling).
    * [Matt Dancho: High-Performance Time Series Forecasting course](#matt-dancho-high-performance-time-series-forecasting-course)
* [R Books](#r-books)
* [Python Books](#python-books)

---

## Review of pre-tidyverse libraries
Abraham Mathew. 2019-08-18. [Packages for Getting Started with Time Series Analysis in R](https://mathewanalytics.com/packages-for-getting-started-with-time-series-analysis-in-r/). Blog post.

* Provides a brief survey of R libraries used for time series before `tidyverse` development became popular.
* [ts](https://rdrr.io/r/stats/ts.html) vs [xts](https://joshuaulrich.github.io/xts/) for representing time series data.
* [dynlm](https://rdrr.io/cran/dynlm/api/) for comparing regressors at different times. [usage](https://www.rdocumentation.org/packages/dynlm/versions/0.3-6/topics/dynlm) documentation.
* [forecast](https://robjhyndman.com/publications/automatic-forecasting/) for time series forecasting.

## Time series libraries compatible with the `tidyverse`
### Rob Hyndman: R libraries
* [Tidy tools for time series](https://tidyverts.org/).
* [tsibble](https://tsibble.tidyverts.org/): Tidy Temporal Data Frames and Tools.
* [fable](https://fable.tidyverts.org/): Forecasting Models for Tidy Time Series.
* [feasts](https://feasts.tidyverts.org/): Feature Extraction and Statistics for Time Series.

Related presentations:

* Rob J. Hyndman. 2020-01-27. [Tidy Time Series and Forecasting in R](https://github.com/rstudio-conf-2020/time-series-forecasting). rstudio::conf 2020. 2-day workshop.
* Rob J. Hyndman. 2018-07-13. [Tidy Forecasting in R](https://www.youtube.com/watch?v=MemnYSGeJ34). useR2018. 14 minutes.

Related blog posts:

* Rob Hyndman. 2021-05-16. [Time series cross-validation using fable](https://robjhyndman.com/hyndsight/tscv-fable/).

### Matt Dancho: R libraries
* [timetk](https://business-science.github.io/timetk/): A Tool Kit for Working with Time Series in R.
    * data wrangling
    * visualization
    * feature engineering
* [modeltime](https://business-science.github.io/modeltime/): The Tidymodels Extension for Time Series Modeling.
    * fast experimentation with many software models.

## Facebook: `prophet` package
* [Prophet](https://facebook.github.io/prophet/): Forecasting at scale. home page.
* [prophet](https://cran.r-project.org/package=prophet) package: Automatic Forecasting Procedure.
    * "Implements a procedure for forecasting time series data based on an additive model where non-linear trends are fit with yearly, weekly, and daily seasonality, plus holiday effects. It works best with time series that have strong seasonal effects and several seasons of historical data. Prophet is robust to missing data and shifts in the trend, and typically handles outliers well."
* Prophet [Quick Start](https://facebook.github.io/prophet/docs/quick_start.html). documentation.
* Sean J. Taylor, Ben Letham. 2017-02-23. [Prophet: forecasting at scale](https://research.fb.com/blog/2017/02/prophet-forecasting-at-scale/). Blog post.
* [Time series forecasting with Prophet](https://www.coursera.org/projects/time-series-forecasting-with-prophet). Coursera Guided Project. 1-hour project.

## Twitter: AnomalyDetection
* [AnomalyDetection](https://github.com/twitter/AnomalyDetection). GitHub repository.

## Google: `CausalImpact` package
* [CausalImpact](https://google.github.io/CausalImpact/CausalImpact.html): Inferring Causal Effects using Bayesian Structural Time-Series Models.
* [CausalImpact: An R package for causal inference in time series](https://google.github.io/CausalImpact/).
* [GitHub repository](https://github.com/google/CausalImpact).

## Online Courses
### Coursera: Intro to Time Series Analysis in R
[Intro to Time Series Analysis in R](https://www.coursera.org/projects/intro-time-series-analysis-in-r). Coursera Guided Project. 2-hour project-based course.

### Coursera: Time series forecasting with Prophet
[Time series forecasting with Prophet](https://www.coursera.org/projects/time-series-forecasting-with-prophet). Coursera Guided Project. 1-hour project.

### Georgia Institute of Technology: Introduction to Analytics Modeling
[Introduction to Analytics Modeling](https://www.edx.org/course/introduction-to-analytics-modeling). Free online course at [edX](https://www.edx.org/). Week 3 covers "Time Series Models".

### Matt Dancho: High-Performance Time Series Forecasting course
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

Related blog posts:

* Time Series in 5-Minutes
    * Part 1: [Data Wrangling and Rolling Calculations](https://www.business-science.io/code-tools/2020/08/19/five-minute-time-series-rolling-calculations.html)
    * Part 2: [The Time Plot](https://www.business-science.io/code-tools/2020/06/08/five-minute-time-series-time-plot.html)
    * Part 3: [Autocorrelation](https://www.business-science.io/code-tools/2020/06/17/five-minute-time-series-part-2.html)
    * Part 4: [Seasonality](https://www.business-science.io/code-tools/2020/08/26/five-minute-time-series-seasonality.html)
    * Part 5: [Anomalies and Anomaly Detection](https://www.business-science.io/code-tools/2020/09/02/five-minute-time-series-anomaly-detection.html)
    * Part 6: [Modeling Time Series Data](https://www.business-science.io/code-tools/2020/09/09/five-minute-time-series-modeling-data.html)

Releated podcasts:

* SuperDataScience. [SDS 463: Time Series Analysis](https://www.superdatascience.com/podcast/time-series-analysis). Jon Krohn interviews Matt Dancho. See especially:
    * Matt’s 6 time series models [14:11]
    * Timetk [15:02]
    * Modeltime [29:32]
    * Gluon package [36:04]

## R Books
* Rob J. Hyndman. 2021. [Forecasting: Principles and Practice](https://otexts.com/fpp3/), 3rd edition. Free to read online.
* Galit Shmueli, Kenneth C. Lichtendahl Jr. 2016. [Practical Time Series Forecasting with R: A Hands-On Guide](http://www.forecastingbook.com/). 2nd Edition.

## Python Books
* Aileen Nielsen. 2019. [Practical Time Series Analysis](https://learning.oreilly.com/library/view/practical-time-series/9781492041641/). O'Reilly Media, Inc.
* B.V. Vishwas, Ashish Patel. 2020. [Hands-on Time Series Analysis with Python: From Basics to Bleeding Edge Techniques](https://learning.oreilly.com/library/view/hands-on-time-series/9781484259924/). Apress.
