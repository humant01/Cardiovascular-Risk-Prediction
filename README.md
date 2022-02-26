# Cardiovascular-Risk-Prediction
## Data Discription
The dataset is from an ongoing cardiovascular study on residents of the town of Framingham,
Massachusetts. The classification goal is to predict whether the patient has a 10-year risk of
future coronary heart disease (CHD). The dataset provides the patients’ information. It includes
over 4,000 records and 15 attributes.
Variables
Each attribute is a potential risk factor. There are both demographic, behavioral, and medical risk
factors.
Data Description
Demographic:
• Sex: male or female("M" or "F")

• Age: Age of the patient;(Continuous - Although the recorded ages have been truncated to
whole numbers, the concept of age is continuous)

Behavioral

• is_smoking: whether or not the patient is a current smoker ("YES" or "NO")

• Cigs Per Day: the number of cigarettes that the person smoked on average in one day.(can be
considered continuous as one can have any number of cigarettes, even half a cigarette.)

Medical( history)

• BP Meds: whether or not the patient was on blood pressure medication (Nominal)

• Prevalent Stroke: whether or not the patient had previously had a stroke (Nominal)

• Prevalent Hyp: whether or not the patient was hypertensive (Nominal)

• Diabetes: whether or not the patient had diabetes (Nominal)

Medical(current)

• Tot Chol: total cholesterol level (Continuous)

• Sys BP: systolic blood pressure (Continuous)

• Dia BP: diastolic blood pressure (Continuous)

• BMI: Body Mass Index (Continuous)

• Heart Rate: heart rate (Continuous - In medical research, variables such as heart rate though in
fact discrete, yet are considered continuous because of large number of possible values.)

• Glucose: glucose level (Continuous)

Predict variable (desired target)

• 10-year risk of coronary heart disease CHD(binary: “1”, means “Yes”, “0” means “No”) -
DV

## What is the business use case of project?
Consider a case in Healthcare where a Machine Learning (ML) system is asked to predict the risk of a patient developing cardiovascular disease in a given time frame, say within the next one year.The output expected from the model is a risk score which if equal to or above a chosen threshold indicates that patient has a risk of developing cardiovascular disease and if it were below the threshold, indicates no risk.

## What is the potential impact of your project?
The correct prediction of heart disease can prevent life threats, and incorrect prediction can prove to be fatal at the same time. ML model will help to predict future risk of Cardiovascular Diseases.

## HOW and WHY have you approached the problem statement? 
I started the study by handling missing values, our dataset was having many columns with null entities I have removed null values using KNN Imputer and Simple imputer I've seen how smoking, systolic BP, diastolic BP, BMI, Heart rate, glucose, hypertensive, cholesterol, diabetes, etc affects the person.
Factors like Blood Pressure, Glucose Level, Age had created a huge impact on a person's heart condition. We checked the correlations between the factors. Handled the class Imbalance using SMOTE and experimented with a combination of SMOTE + Tomek links. SMOTE gave a good result of 50-50 class balanced data.
Then I started building classification models. I started with Logistic regression with default parameters but I did not get a good score.
Then I used a Support Vector Machine with various Kernel tricks with respective hyperparameters. I have used linear kernel,  polynomial kernel and gaussian radial based kernel. Polynomial and rbf kernel gave good scores though it took a large amount of time in rendering.
Then I tried a neural network with a single hidden layer there we got decent numbers but less as compared to the rbf poly kernel.
Then I tried the Random Forest Classifier and I got great Scores. Random Forest Classifier performed well.
And at last I've tried XGBoost Classifier and it had performed really well and I got the best scores with XGBoost Classifier as compared to other Models, so i conclude XGBoost is my optimal model for use and we can use this model for further in predicting Cardiovascular risk.







