
The security status of the location where we live is one of the most critical and important issues for every citizen. 
As most individuals will remember, In order to determine the security status, it is difficult to ignore the crime rate. 
Several variables can affect the incidence of crimes, including time, places, population, level of education, income rate. 
Big Data Analytics project was implemented to provide predictions and exploratory analysis for Chicago Crime Rate Pattern. 
The data was collected from the Chicago data portal spanning from 2017-2020. 
Main goal was set to find the crime trend through the years from which we can know whether the security status in the city is getting better or worse. 
Secondly, what time is relatively more secure and which time period is more dangerous are also important for us. 
Besides, as we all know, different crime types have different levels of harm,  are interested in the proportion of different types of crime.


DATA DESCRIPTION:

Data was collected from the Chicago Data Portal spanning from 2001 to November 2020, In order to protect the privacy of crime victims, addresses are shown at the block level only and specific locations are not identified. In general, the data contained data such as the date/time that the crime occurred, the block where the crime occurred, type of crime, definition of location, whether an arrest occurred, and coordinates of location. 
The data shown also includes more features such as  latitude, longitude and location coordinates, but these features do not have strong correlation with respective selected features hence were not used for analysis purpose.
linked the names of community areas obtained from  https://www.chicago.gov/city/en/depts/cpd/dataset/police_stations.html based on the community area code, Chicago has 77 communities the PDF for the same is attached with the submission. 

SIZE OF DATA:
The dataset contains 1056780 number of records and 24 columns out of which the 17 columns are important for the analysis. 


DATA EXTRACTION: 
1.	Downloaded the folder in CSV format and Used Python Pandas 
2.	Data preprocessing procedure which is cleaning was implemented by:
a.	Removing duplicate rows
b.	Removing missing values (etc. Null/NA values) in the dataset
c.	Filtering out all the features from the dataset that are not relevant

TECHNIQUES
Dealing with a big data set in our project, so the need to use technology to deal with the big data set wasn't an issue. It was however a bit of a struggle to decide between MapReduce and Spark. These two structures have their own qualities and advantages.
The main difference between them in fact, lies in the processing approach: Spark can do it in memory, while Hadoop MapReduce needs to read from and write to a disk. As a consequence, the processing speed varies significantly. But we decided on choosing Spark for the data analysis, as Spark in-memory computation is much faster and efficient in today’s world, we used Spark as our main framework.

IMPORTANT LIBRARIES USED FOR EXPLORATORY ANALYSIS
import pandas as pd
import re
from pyspark import SparkContext
import seaborn as sns
import matplotlib.pyplot as plt

PREDICTIVE ANALYSIS

Library Functions:
from pyspark.ml.feature import StringIndexer, VectorAssembler
from pyspark.ml.classification import LogisticRegression

1.	For our predictive crime analysis, we used the logistic regression model from the apache spark machine learning library. 

2.	The correlation among attributes is not high which is an obvious indication of obtaining a less accuracy score. Therefore, to make shift in obtained accuracy we converted the required string type feature into vector index.






