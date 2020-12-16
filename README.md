# ca4022-churn-prediction

Collection of source code used in analysis of customer churn data and development of churn prediction models.

**create_cluster.sh** will configure a Google Cloud Dataproc Cluster. We have set parameters to enable usage of Spark 3.0.1 and Python 3.8 on Ubuntu 18. Environment variables such as Region, Cluster Name, and Storage Bucket Name are set here.


**pyspark_train_model.sh** will submit a PySpark job to the previously created Dataproc Cluster.

**train_model.py** is th actual Python script submitted for the PySpark job. It will read in the Sparkify dataset, perform feature extraction and data cleaning, and build a decision tree model using the resulting data. 

A saved version of the model and a visualisation of the decision process is output into the bucket 'ca4022-files/output/'.

