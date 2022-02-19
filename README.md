# Predicting Heart Disease using Machine Learning
Repo for Heart Disease Prediction model - Classification

This notebook looks into using various Python-based machine learning & data science libraries in an attempt to build a machine learning model capable of predicting whether or not someone has heart disease based on their medical attributes.

Data Attributes:
1. age
2. sex
3. chest pain type (4 values)
4. resting blood pressure
5. serum cholestoral in mg/dl
6. fasting blood sugar > 120 mg/dl
7. resting electrocardiographic results (values 0,1,2)
8. maximum heart rate achieved
9. exercise induced angina
10. oldpeak = ST depression induced by exercise relative to rest
11. the slope of the peak exercise ST segment
12. number of major vessels (0-3) colored by flourosopy
13. thal: 3 = normal; 6 = fixed defect; 7 = reversable defect

Approach:
1. Problem definition
2. Data
3. Evaluation
4. Features
5. Modelling
6. Experimentation

Problem Definition
In a statement,
Given clinical parameters about a patient,can we predict whether or not they have heart disease?

Data
The original data came from the Cleveland data from the UCI Machine Learning Repository.
There is also a version of it available on Kaggle. https://www.kaggle.com/ronitf/heart-disease-uci

Evaluation
If we can reach 95% of at predicting whether or not a patient has heart disease during the proof of concept, we'll pursue the project.

Features
* age - age in years
* sex - (1 = male; 0 = female)
* cp - chest pain type
  * 0: Typical angina: chest pain related decrease blood supply to the heart
  * 1: Atypical angina: chest pain not related to heart
  * 2: Non-anginal pain: typically esophageal spasms (non heart related)
  * 3: Asymptomatic: chest pain not showing signs of disease
* trestbps - resting blood pressure (in mm Hg on admission to the hospital)
  anything above 130-140 is typically cause for concern
* chol - serum cholestoral in mg/dl
  serum = LDL + HDL + .2 * triglycerides
  above 200 is cause for concern
* fbs - (fasting blood sugar > 120 mg/dl) (1 = true; 0 = false)
  '>126' mg/dL signals diabetes
* restecg - resting electrocardiographic results
  * 0: Nothing to note
  * 1: ST-T Wave abnormality
    can range from mild symptoms to severe problems
    signals non-normal heart beat
  * 2: Possible or definite left ventricular hypertrophy
       Enlarged heart's main pumping chamber
* thalach - maximum heart rate achieved
* exang - exercise induced angina (1 = yes; 0 = no)
* oldpeak - ST depression induced by exercise relative to rest
  looks at stress of heart during excercise
  unhealthy heart will stress more
* slope - the slope of the peak exercise ST segment
  * 0: Upsloping: better heart rate with excercise (uncommon)
  * 1: Flatsloping: minimal change (typical healthy heart)
  * 2: Downslopins: signs of unhealthy heart
* ca - number of major vessels (0-3) colored by flourosopy
colored vessel means the doctor can see the blood passing through
the more blood movement the better (no clots)
* thal - thalium stress result
  * 1,3: normal
  * 6: fixed defect: used to be defect but ok now
  * 7: reversable defect: no proper blood movement when excercising
* target - have disease or not (1=yes, 0=no) (= the predicted attribute)
