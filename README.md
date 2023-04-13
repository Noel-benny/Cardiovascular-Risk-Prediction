# Cardiovascular-Risk-Prediction
Cardiovascular Risk Prediction

Cardiovascular disease is a group of diseases affecting your heart and blood vessels. These diseases can affect one or many parts of your heart and/or blood vessels. A person may be symptomatic (physically experiencing the disease) or asymptomatic (not feeling anything at all).

Cardiovascular disease includes heart or blood vessel issues, including:

Narrowing of the blood vessels in your heart, other organs or throughout your body.
Heart and blood vessel problems present at birth.
Irregular heart rhythms.
The given dataset is from an ongoing cardiovascular study on residents of the town of Framingham, Massachusetts. The classification goal is to predict whether the patient has a 10-year risk of future coronary heart disease (CHD). The dataset provides the patients’ information. It includes over 4,000 records and 15 attributes. Variables Each attribute is a potential risk factor. There are both demographic, behavioral, and medical risk factors.

## Data Description:
The dataset provides the patients’ information. It includes over 4,000 records and 15 attributes. Variables Each attribute is a potential risk factor. There are both demographic, behavioural, and medical risk factors

### Demographic:
•	*Sex:* male or female("M" or "F")

•	*Age:* Age of the patient

### Behavioral:

•	*is_smoking:* whether or not the patient is a current smoker ("YES" or "NO")

•	*Cigs Per Day:* the number of cigarettes that the person smoked on average in one day

### Medical(History):

•	*BP Meds:* whether or not the patient was on blood pressure medication

•	*Prevalent Stroke:* whether or not the patient had previously had a stroke

•	*Prevalent Hyp:* whether or not the patient was hypertensive

•	*Diabetes:* whether or not the patient had diabetes (Nominal) Medical(current)

•	*Tot Chol:* total cholesterol level

•	*Sys BP:* systolic blood pressure

•	*Dia BP:* diastolic blood pressure

•	*BMI:* Body Mass Index

•	*Heart Rate:* heart rate

•	*Glucose:* glucose level

•	*CHD:* 10-year risk of coronary heart disease CHD(binary: “1”, means “Yes”, “0” means “No”)


## Approach:-
### Data preparation:
•	Removed null values from the dataset

•	Removed duplicate entries

•	Used SMOTE and random under sampling to get a balanced dataset

### Feature engineering:
•	Extracted feature ‘Hypertension’ from systolic and diastolic blood pressure data

•	Extracted feature ‘Diabetese severity’ from diabetes and glucose column

•	Constructed new feature ‘Smoking Factor’ from number of cigarettes consumption


First, we performed data cleaning for the raw data. Asking right question to dataset is always considered as great approach so we asked some very meaningful questions and plotted graphs and other visualization entities to get insights from data and I come with following conclusions:

Over 85% of patients has not having 10-year risk of future coronary heart disease (CHD) and 15% of patients has 10-year risk.
Most of the patients having 10-year risk of CHD are males. Around 18% of males having risk and 12% of females has 10-year futur risk of CHD.

Patients of age 45-55 chance of having 10-year risk of CHD are initiated.

we get between 45-60 of age patients who are smoking getting a chance of 10-year risk of future CHD are high.

Patients who are having diabetes are more vulnerable to the 10-year future risk.

most studies show a greater risk of stroke and heart disease related to higher systolic pressures compared with elevated diastolic pressures.

As we can see a person who had a stroke earlier more prone to CHD.

We can able to see over 32% of patients are prone to future heart disease who had prevalent hypertension and 69% of people who has hypertension are not much vulnerable to disease.

Next, We implemented 4 machine learning algorithms logistic classifier, Random Forest, XGboost and naive bayes classifier. we did hyperparameter tuning to improve our model performance. The results of our evaluation are: Finally for training set accuaracy from xg boost model is 96% and testing accuracy is 81% and No overfitting is seen. So, we have chosen XGBoost as the final prdiction model which should be deployed for real user interaction. Now, patients got an idea about which all health factors affecting directly to the heart disease and steps to take care of thier health in a proper way.
