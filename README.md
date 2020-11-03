## TelecomAnomalies

Detecting Performance Anomalies in Cellular Networks

Download entire folder from below link.

GitHub Link: https://github.com/littlew/CellPAD

http://adslab.cse.cuhk.edu.hk/software/cellpad/




requirements.txt and example folder as shown below.

<img src="imgs/Cellpad.png" alt="My cool logo"/>


CELLPAD, a unified performance anomaly detection framework for KPI time-series data. 

CELLPAD realizes simple statistical modeling and machine-learning-based regression for anomaly detection; in particular, it specifically takes into account seasonality and trend components as well as supports automated prediction model retraining based on prior detection results. 

CELLPAD detects two types of anomalies of practical interest, namely sudden drops and correlation changes, based on a large-scale real-world KPI dataset collected from a metropolitan LTE network.



How to call different algorithms?

• For DropController, "predictor" can be "RF", "RT", "SLR", "HR", "WMA", "EWMA", "HW".

• For ChangeController, "predictor" can be "RF", "RT", "SLR", "HR","LCS".


How to perform feature selection?

• "feature_types" can be a subset of ["Numerical", "Indexical"]
• "feature_time_grain" can be a subset of ["Hourly", "Daily", "Hourly"]
• "feature_operations" can be a subset of ["Raw", "Mean", "Median", "Wma", "Ewma"]

How to remove any trend components?

•	DropController(to_remove_trend=True, trend_remove_method="center_mean")

•	ChangeController(to_remove_trend=False, trend_remove_method="center_mean")

•	"to_remove_trend" is True or False to indicate whether to remove the trend or not.

•	"trend_remove_method" is "center_mean" or "past_mean".

•	"center_mean": the trend at time i is the mean of the points in [i-84, i+83].

•	"past_mean": the trend at time i is the mean of the points in [i-167, i].

