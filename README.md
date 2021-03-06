# Automating-Feature-Engineering
In this project, we present the Feature Engineering Machine (FEM), which automates the feature engineering process in classification and regression problems. It is a meta-learning approach that learns from over a hundred meta-training datasets about the usefulness of a transformation
in enhancing the relationship between a feature and response variable to improve model performance. FEM is trained to provide the most suitable recommendations
for transforming the original features in a new dataset, based on learning from past feature engineering experiences.

This project addresses how meta-learning can be used to automate feature engineering. It also analyzes different techniques to achieve informative representation of feature-response distributions that would improve its mapping with the usefulness of transformations. In addition, it extends the notion of learning feature engineering from past experiences in Classification problems to Regression problems and assesses the implications of generalizing this concept.


FEM is trained using Random Forest and Logistic Regression as Classification models, and Linear Regression as a Regression model. Quantile Sketch Array(QSA), Percentile Binning(PB), and Conditional Probability(CP) are numerous techniques that are used to capture the feature-response distribution. The main function of FEM is to improve the predictive performance of the models by applying different transformations to the features in a dataset. For Classification and Regression Problems, model performance is evaluated using F1-score and R-squared score respectively. FEM includes 5 unary and 3 binary transformations. Every transformation has a corresponding Multi-Layer Perceptron (MLP) which is a binary classifier that predicts the usefulness of a transformation on a feature.


The test results show that when unary transformations are applied
on the Classification datasets then for Logistic Regression 68% of the
datasets showed an improvement in the model performance score (F1-
score). Out of these datasets, 70.58% and 76.47% showed performance
improvement corresponding to QSA and PB approaches respectively. In
the case of Random Forest, 64% of the datasets showed an improvement in the F1-score. Among these datasets, 81.25% and 88.23% showed
performance improvement for QSA and PB methods respectively. Similarly when unary transformations are applied on the Regression datasets
then for Linear Regression Model 77.28% of the datasets showed an improvement in the R-squared score. 47.18%, 41.17%, and 88.23% of these
datasets showed performance improvement corresponding to PB, QSA,
and CP approaches respectively. It is also observed that the use of binary
transformations enhances the F1-score for only 31.57%, 53.33%, 50% of
the test datasets for Logistic Regression, Random Forest, and Linear
Regression Models respectively.


In Classification problems, for the Logistic Regression model, FEM
achieves an average predictive performance improvement of 2.1% and
3.4% and maximal performance improvement of 8.3% and 18.3% for QSA
and PB respectively on the datasets. For the Random Forest model, the
average performance improvement achieved is 1.9% and 0.9% and the
maximum improvement achieved is 5.9% and 4% using QSA and PB
respectively. In Regression problems, the average rise in the predictive
score is 2.3%, 1.8%, and 3.6%, and the maximum rise is 6.5%, 11.7%,and 11.4% with respect to QSA, PB, and CP.

**NOTE**
1. The folder 'Creating training datasets for MLPs' contains two files, which have the code that we used to create training datasets for MLPs corresponding to different feature transformation techniques like QSA and Percentile Binning.
2. The folder 'MLP models' contains two files which have the code for creating MLPs for Regression Problems corresponding to a particular feature transformation techniques. In this project, we had created around around 60 MLPs in total for both classification and regression problem with respect to different thresholds, feature representation techniques and ML models. All the MLPS had a similar architecture with variation in parameters and the number of layers.
3. The folder 'Testing' contains files which have the code for testing our model for both Regression and Classification tasks with respect to different feature transformation techniques.
