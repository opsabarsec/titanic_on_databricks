# Simple machine learning pipeline that runs on the Databricks platform

This ML pipeline is intended to run in a Spark environment. It was tested on the Databricks community open source platform (ApacheSpark3.1.2).

![datapipeline](9892.jpg)

## 1. Background
A large manufacturing company data flow is getting more important by the day. The company has tested some Python code on local machines to treat data but now there is the need to automatize and scale up the ML pipeline. 

Databricks would provide a very efficient solution, with code running 50X faster than that written in Python since the volume of data treated every day is estimated to be several gigabytes. And it is going to further increase over time. 

Still, stakeholders are suspicious of this new technology and before transitioning to this platform the company would like to have a demo of this technology using a simple free data set: the Titanic survival data.

## 2. The data
A csv file has been  sourced from https://www.kaggle.com/c/titanic/data and imported into Databricks.

The ETL pipeline is broken into three steps that correspond to different quality levels in the pipeline:  
    • data ingestion (“Bronze” tables). Set the correct schema.
    • data cleaning, augmenting (“Silver” tables)
    • transformation/feature engineering to make it ready for ML/AI (“Gold” tables)
      Having separated tables allows having checkpoints, helping later modifications of the code

## 3. The model
 
![jupyter](jupyter.png)A Spark machine learning pipeline has been coded and can be found in the [following Jupyter notebook](https://github.com/opsabarsec/titanic_on_databricks/blob/master/04-ML_pipeline.ipynb)


## 4. Conclusions 
Databricks provides and intuitive and powerful ETL platform. The ML pipeline shows that data can be conveniently transformed and sent to a classical ML model, in this case a Logistic Regression
