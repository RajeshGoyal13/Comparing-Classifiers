# Comparing-Classifiers

## Business Understanding:
The goal of this assignment is to compare the performance of the classifiers (k-nearest neighbors, logistic regression, decision trees, and support vector machines). The dataset is related to the marketing of bank products over the telephone.

## Data Understanding:

The first step for this assignemnt was to understand the data. Looked into the attributes of the data. Most of the columns have non- numeric data. There are any columns which have null data also. Checked if there was any duplication of data and found that there was no duplication of data.

<img width="1005" alt="Screenshot 2024-06-10 at 3 20 03 PM" src="https://github.com/RajeshGoyal13/Comparing-Classifiers/assets/161057282/47ca0dd4-de95-4e8d-ad90-7c19d5972ea0">

<img width="396" alt="Screenshot 2024-06-10 at 3 20 22 PM" src="https://github.com/RajeshGoyal13/Comparing-Classifiers/assets/161057282/9ff17a70-4d54-44b9-aa90-cf4567ff20bc">

<img width="914" alt="Screenshot 2024-06-10 at 3 20 54 PM" src="https://github.com/RajeshGoyal13/Comparing-Classifiers/assets/161057282/7d265d8d-c5b6-45bf-9cc6-9275d5043321">


<img width="996" alt="Screenshot 2024-06-10 at 3 21 14 PM" src="https://github.com/RajeshGoyal13/Comparing-Classifiers/assets/161057282/e205ac12-dce9-4f52-aa9f-c8b566246f70">
There were many columns which have same value "Unknown". So changed the value "Unknown" as per the feature columns.

<img width="996" alt="Screenshot 2024-06-10 at 3 24 49 PM" src="https://github.com/RajeshGoyal13/Comparing-Classifiers/assets/161057282/5920dc4f-6b21-4d38-b67c-824d4be138e2">

## Data Preperation:

Created various histograms to see how the data is scattered in the various categories.

<img width="996" alt="Screenshot 2024-06-10 at 3 27 00 PM" src="https://github.com/RajeshGoyal13/Comparing-Classifiers/assets/161057282/949b6715-c4fe-4ce2-8b8e-44c3c727ca42">
<img width="996" alt="Screenshot 2024-06-10 at 3 27 15 PM" src="https://github.com/RajeshGoyal13/Comparing-Classifiers/assets/161057282/ac5a6022-930e-4f74-a2ab-8a2c23a10786">
<img width="996" alt="Screenshot 2024-06-10 at 3 27 25 PM" src="https://github.com/RajeshGoyal13/Comparing-Classifiers/assets/161057282/1992d717-83fe-4af2-a9d9-f4b4406a0944">

Next step was to check if there are any outliers in the data. Created the histogram for Price, Year and Odometer. It shows that there are some outliers. So used the Inter quartile method to remove the outliers. Here is the comparison of data before  and after quartile methods. Difference can be seen clearly.


<img width="496" alt="Screenshot 2024-06-10 at 3 37 04 PM" src="https://github.com/RajeshGoyal13/Comparing-Classifiers/assets/161057282/7e57f36b-6e43-4c39-b234-ac92a6bb779d">
<img width="496" alt="Screenshot 2024-06-10 at 3 37 37 PM" src="https://github.com/RajeshGoyal13/Comparing-Classifiers/assets/161057282/76534725-f49b-4f93-bffc-410127dd41c7">

<img width="496" alt="Screenshot 2024-06-10 at 3 37 15 PM" src="https://github.com/RajeshGoyal13/Comparing-Classifiers/assets/161057282/54d0e515-de15-4b2d-a6b0-02086d50f3ea">
<img width="496" alt="Screenshot 2024-06-10 at 3 37 46 PM" src="https://github.com/RajeshGoyal13/Comparing-Classifiers/assets/161057282/759b050f-effa-4e6a-9e89-b188f061b266">

<img width="496" alt="Screenshot 2024-06-10 at 3 37 25 PM" src="https://github.com/RajeshGoyal13/Comparing-Classifiers/assets/161057282/8d498a2e-c6aa-4dd2-a96b-77a01f1ab094">
<img width="496" alt="Screenshot 2024-06-10 at 3 37 56 PM" src="https://github.com/RajeshGoyal13/Comparing-Classifiers/assets/161057282/68cf3d5f-6233-48fa-8408-16ae685483b6">

Further found that many columns have multiple values - "job", "education","contact","month", "marital",and "poutcome".So using pd dummies, created seperate column for each feature's value.

<img width="874" alt="Screenshot 2024-06-10 at 3 44 14 PM" src="https://github.com/RajeshGoyal13/Comparing-Classifiers/assets/161057282/18edde10-b5b8-4bfb-aaa6-1848ae7b551b">

## Modeling:
Once the data set is ready. Next step is to create models.Created the Pipelines for 4 four models (kNN, Decision Trees, Logistic Regression, and SVM)

<img width="426" alt="Screenshot 2024-06-10 at 3 48 05 PM" src="https://github.com/RajeshGoyal13/Comparing-Classifiers/assets/161057282/cbd80967-4ab5-4f29-99ef-c611c92c5e74">
<img width="426" alt="Screenshot 2024-06-10 at 3 48 16 PM" src="https://github.com/RajeshGoyal13/Comparing-Classifiers/assets/161057282/f8b1eac5-2139-42f1-991c-73c821ac8364">


<img width="426" alt="Screenshot 2024-06-10 at 3 48 24 PM" src="https://github.com/RajeshGoyal13/Comparing-Classifiers/assets/161057282/1c542373-3ce3-495b-b7d5-b565050d519b">
<img width="426" alt="Screenshot 2024-06-10 at 3 48 30 PM" src="https://github.com/RajeshGoyal13/Comparing-Classifiers/assets/161057282/00139675-b56c-4247-8440-e00bcf4e1c69">


Compared all the models and found that there is slight variation in the Train and Test scores.

<img width="426" alt="Screenshot 2024-06-10 at 3 50 08 PM" src="https://github.com/RajeshGoyal13/Comparing-Classifiers/assets/161057282/c7b72ee5-69b6-45d7-be2c-57a932cefca4">

For better undersating created the Precision Recall Curve. It shows that upto 0.2 recall value there is varation among all the clssifiers but after 0.2, all the four clssifier models shows the same trend of the data.This type of curve works much better for moderate to large imbalanced data than the ROC-curve. This curve indicates that the best model is Logistic Regression model (red line) by slighlty margin over KNN model.It also indicates that the worst model seems to be the Decision Tree.

<img width="606" alt="Screenshot 2024-06-10 at 3 50 24 PM" src="https://github.com/RajeshGoyal13/Comparing-Classifiers/assets/161057282/ad14896b-88c7-4690-940d-97f64e7391d7">

## Findings  and recommendations
1. Some of the columns have more data for a particular feature. e.g. Credit in default - Most counts were No as compared to Yes. Has personal Loan, Most counts were No as compared to Yes. Ssome of the columns have "unknown" also. So, such irregularties in the data, may not help in getting the correct models.

2. In Target coulmn also, distribution of the data was not uniform. Users with term deposit - No were almost twice then the users with the term deposit Yes.
   
3. Have to drop of column "Days" as it was creating 30 columns. It was slowing down the models.
   
4. Looking at the models, SVC model was the slowest model. Average Fit time was very high as compared to KNN and Logistic regression. Descision tree was also higher but not so high as compared to SVC.










