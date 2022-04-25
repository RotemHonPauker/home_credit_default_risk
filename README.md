<p align="center">
  <img src="images/credit_title_2.jpeg" width="300"/>
</p>

The repository is organized as the following:

1. [Kaggle competition's dataset](https://www.kaggle.com/competitions/home-credit-default-risk/data) includes 7 different sources of data: 

:red_square:CURRENT:red_square:
* application_train.csv --> df_app.csv: basic socio-economic information about each applicant at Home Credit.

:red_square:BU:red_square:
* bureau.csv --> df_bureau.csv: data concerning client's previous credits from other financial institutions.
* bureau_balance.csv --> None: monthly data about the previous credits in bureau.

:red_square:HC:red_square:
* previous_application.csv --> df_prev.csv: previous applications for loans at Home Credit of clients who have.
* POS_CASH_balance.csv --> df_pos.csv: monthly data about previous point of sale or cash loans clients have had with Home Credit.
* installments_payments.csv --> df_inst.csv: payment history for previous loans at Home Credit.
* credit_card_balance.csv --> None: monthly data about previous credit cards clients have had with Home Credit.

<p align="center">
  <img src="images/Slide2.JPG" width="500"/>
</p>

2. [Aggregation](https://github.com/RotemHonPauker/home_credit_default_risk/blob/master/credit_Agg.ipynb) as well as feature engineering and feature selection were executed on 5 out of the 7 sources (output files' names as mentioned above), and later [merged](https://github.com/RotemHonPauker/home_credit_default_risk/blob/master/credit_Merge.ipynb) together (output file's name: df_total.csv).

<p align="center">
  <img src="images/Slide3.JPG" width="500"/>
</p>

3. In order to retrieve more insights from the data, [clustering and anomaly detection](https://github.com/RotemHonPauker/home_credit_default_risk/blob/master/credit_ClusterAnomaly.ipynb) algorithms such as hierarchical clustering and DBSCAN as well as Isolation Forest, One Class SVM and LOF, were tested. Unfortunately, none of them were useful, and further [manually research](https://github.com/RotemHonPauker/home_credit_default_risk/blob/master/credit_EDA.ipynb) was required. Two detected phenomena of TYPE_EDUCATIOM feature and DAYS_EMPLOYED feature are shown below. The final processed dataset which the classification models were trained and evaluated by can be found in /csv directiory.

<p align="center">
  <img src="images/Slide4.JPG" width="500"/>
</p>

<p align="center">
  <img src="images/Slide5.JPG" width="500"/>
</p>

4. Four classification models were compared: Logistic Regression, Random Forest, XGBoost, LightGBM. [The results](https://github.com/RotemHonPauker/home_credit_default_risk/blob/master/credit_Class.ipynb) are shown below. The models' performences were examine taking in account the imbalance and overlapping targets issues which were observed earlier.

<p align="center">
  <img src="images/Slide6.JPG" width="500"/>
</p>

<p align="center">
  <img src="images/Slide7.JPG" width="500"/>
</p>
