# Multivariate-Multiple-Regressor

In this project, I developed a multivariate multiple regression model to study the
effect of eight input variables on two output variables, which are the heating load and
the cooling load, of residential buildings.

### Data Sources and Description
The data set used for this project was gotten from the 
[University of Carlifornia (UCI) machine learning repository](https://archive.ics.uci.edu/ml/machine-learning-database/00374)
The dataset is at 10 min for about 4.5 months. The temperature and humidity conditions were monitored with a ZigBee wireless sensor network. Each wireless node transmitted the tempereature and humidity conditions around 3.3 min.
Then the wireless data was averaged for 10 minutes periods. The energy data was logged every 10 minutes with m-bus energy metres. Weather from the nearest airport weather station (Chievres Airport, Belguim) was downloaded from a public dataset from reliable prognosis and merged together with the experimental data sets using the date and time column 

Two random variables have been included in the data sets for testing the regression models and to filter out non predictive attributes (parameters). 

### Exploratory Data Analysis
The statistical overview was properly investigated using the pandas_profiling method frrom which features with high correlations were ascertained.
The Exploratory Data analysis on the date feature was also carried out to detect the trends in the date feature in the dataset.
The figure below shows the correlogram of the dataset
{{< figure src="/images/corr.png" title="Data Correllogram" >}}


### Data Preprocessing
The data was normalized using MinMaxScaler method from the scikit-learns library

### Modelling 
* Linear regression, Lasso, Ridge, and Decision Tree regressors from the Scikit-Learns library was used. 
* A Hyperparametr tunning was done using GridSearchCV, Stratified KFold Cross validation to find the best performing model.
* The model was evaluated using different metrics such as Accuracy, Mean Squared Error (MSE), Mean Absolute Error (MAE), and Root Mean Squared Error RMSE.

### Conclusion