# BRAIN-TUMOUR-DETECTION


[![Website shields.io](https://img.shields.io/website-up-down-green-red/http/shields.io.svg)](http://brain-tumor-detection-sundi.azurewebsites.net/)&nbsp;
[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/)&nbsp;
<img src="https://img.shields.io/badge/Made%20with-Markdown-1f425f.svg">&nbsp;
![GitHub repo size](https://img.shields.io/github/repo-size/Shashank-Sundi/BRAIN-TUMOUR-DETECTION)&nbsp;
![Lines of code](https://img.shields.io/tokei/lines/github/Shashank-Sundi/BRAIN-TUMOUR-DETECTION?style=flat)

<hr>

## Deployments
* Azure : http://brain-tumor-detection-sundi.azurewebsites.net/

* Heroku :  https://insurance-fraud-detector-sundi.herokuapp.com/

<hr>

## Original Dataset and  Notebooks

* Original Dataset : https://github.com/SartajBhuvaji/Brain-Tumor-Classification-DataSet.git

* Notebook Page : https://shashank-sundi.github.io/BRAIN-TUMOUR-DETECTION/

* Colab Notebook : https://colab.research.google.com/drive/1IjFYHuim8on_1gbiiaBStBpxoe4voB9e?usp=sharing

<hr>

## Project Description

Brain Tumors are complex. There are a lot of abnormalities in the sizes and location of the brain tumors. This makes it really difficult for complete understanding of the nature of the tumor. Also, a professional Neurosurgeon is required for MRI analysis. Often times in developing countries the lack of skillful doctors and lack of knowledge about tumors makes it really challenging and time-consuming to generate reports from MRI. A manual examination can be error-prone due to the level of complexities involved in brain tumors and their properties.Hence , I've built this web page which will help to classify the type of tumor(if any) , based on results from the Densenet-121 retrained model.

<img src="static\images\national-cancer-institute-BDKid0yJcAk-unsplash.jpg" style="width: 1000px;
    height: 500px; object-fit: cover;
    object-position: 20% 60%;" alt="affair" />
<hr>

|**Models**| **VGG-19** | **Alexnet**  | **Resnet-101**  | **Resnet-50** | **Inception-V3** |**Effiecient Net**|**DenseNet**|**Googlenet**|
| :---| :-------- | :------- | :------------------------- | :-------| :-------| :-------| :-------| :-------|
|**Accuracy**|89.91|89.45|82.03|82.27|81.47|81.35|81.57|78.78|
|**Recall**|89.95|89.90|83.68|83.22|82.81|82.41|81.66|80.77|
|**Precision**|90.29|88.83|80.66|80.11|81.16|82.99|79.56|78.37|
|**Model Size**|549mb|233mb|171mb|97.8mb|104mb|255mb|30.8mb|49.7mb|


<hr>

## Project Execution

### (A) **Analysis in Jupyter Notebook**

| **Step**|**Execution of the project was carried out as given in the following steps :** |
| :--------|:-------- | 
|1| Validated and rectified the data types of the features and analysed their statistical properties|
|2|Performed Random Sample Imputation for Categorical columns and KNN imputation for Numerical Columns
|3| Performed EDA on data - checked the distribution of data using NPP, KDE plots , visualized relation between the different features|
|4|Performed Mean , Target Guided Ordinal , One-hot and frequency encoding on the various categorical features, according to the type and information of features
|6|Visualized Outliers via BoxPlots and removed the possible Outliers
|7| Created new features from existing date columns
|8| Visualized the correlation matrix and removed highly correlated columns
|9| Performed Feature Selection using various methods like SFS , SBS ,RFE,CHI2 etc. and compared overall performance of the individual features
|10|Chose 20 features based on feature v/s performance graph from SFS
|11| Handled the Imbalance in the dataset by using SMOTE
|12|Clustered the dataset into 4 clusters , using Kmeans and the kmeans-elbow graph
|13| Metric used to evaluate models - Recall and Accuracy
|14| Trained and tested various models on the data clusters and for each cluster , chose the model which gave highest Accuracy and Recall
|15|By analyzing the performance of the models , it was unsderstood that the Models generalized better after clustering , hence we chose different models for each cluster
|16|Performed Hyperparameter Tuning on all the four models
|17|Cluster 1 - Model : Random Forest :Recall-90.34% Accuracy-89.51%
|18|Cluster 2 - Model : KNN :Recall-100% Accuracy-100%
|19|Cluster 3 - Model : Adaboost :Recall-100% Accuracy-96.55%
|20|Cluster 4 - Model : Logistic Regression :Recall-100% Accuracy-87.5%
|21| Exported all required models via pickle


### (B) **Building the Application**

| **Step**|**Execution of the project was carried out as given in the following steps :** |
| :--------|:-------- | 
|1| Built Log Writer Package , for writing the log messages in a centralised log file
|2| Built the Data Formatter Package, for aggregating the inputs from the html form ; converting the input to a dataframe
|3| Buil the Valaidator Package , to validate the data types of inputs , column names , length etc.
|4| Built the Preprocessing Package ,for imputation , encoding and other transformations
|5| Built Package for finding the cluster to which the input data belongs ; exporting the model trained for the corresponding cluster
|5| Built REST API using Flask framework ; created routes for home page and prediction , by calling all the required modules 
|6| Created the requirements.txt , Procfile , etc. and all other requirements to be satisfied for deployment.
|7| Built html pages for data input and results prediction
|8| Deployed the model on Heroku via Git Bash terminal

<hr>

## Screenshots

### **Enter the required inputs in home page and press predict button**

<img src="static\images\home fraud.PNG" alt="FIFA" />

### **The Prediction Page**

<img src="static\images\result fraud.PNG" alt="FIFA" />

<hr>
  
## Contact

<a href="https://www.linkedin.com/in/shashank-sundi-4b78561b1"> ![alt text](https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)</a>&emsp;
<a href="https://www.instagram.com/shashank_sundi13/">![alt text](https://img.shields.io/badge/Shashank_Sundi-%23E4405F.svg?style=for-the-badge&logo=Instagram&logoColor=white)</a>&emsp;
<a href="mailto:sundi.sn@gmail.com">![alt text](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)</a>

<hr>
