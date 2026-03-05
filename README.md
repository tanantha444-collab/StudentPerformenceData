 Student Performance Prediction – Project Report
1️⃣ Project Title

Student Performance Prediction using Logistic Regression

2️⃣ Objective :
The objective of this project is to analyze student data and predict their academic performance using a machine learning model.

This project uses different factors such as:

Study time

Absences

Parental support

Tutoring

Extracurricular activities

These factors are used to predict the student's GradeClass using the Logistic Regression algorithm.

The goal is to understand which factors influence student performance and build a model that can predict student outcomes based on their behavior and study habits.

Machine Learning algorithm:
➡️ Scikit-learn
➡️ Model: Logistic Regression

3️⃣ Dataset Description

Dataset columns:

Column	Description
StudentID	Student ID
Age	Student age
Gender	Male / Female
Ethnicity	Student ethnicity
ParentalEducation	Parent education level
StudyTimeWeekly	Weekly study hours
Absences	Absence count
Tutoring	Extra tuition
ParentalSupport	Parent support level
Extracurricular	Activities
Sports	Sports participation
Music	Music participation
Volunteering	Social work
GPA	Grade point average
GradeClass	Final grade class (Target variable)

Target Variable
 GradeClass

4️⃣ Data Cleaning

Steps performed:

1️⃣ Missing values check

df.isnull().sum()

2️⃣ Categorical columns encoding
Example:

df = pd.get_dummies(df, drop_first=True)

3️⃣ Features & Target split

X = df.drop("GradeClass", axis=1)
y = df["GradeClass"]
5️⃣ Train Test Split

Dataset split into training and testing data.

from sklearn.model_selection import train_test_split

X_train,X_test,y_train,y_test = train_test_split(
X,y,test_size=0.2,random_state=42)
6️⃣ Model Building

Algorithm used

➡️ Logistic Regression

from sklearn.linear_model import LogisticRegression

model = LogisticRegression()
model.fit(X_train,y_train)
7️⃣ Prediction
y_pred = model.predict(X_test)
8️⃣ Model Evaluation

Accuracy score:

from sklearn.metrics import accuracy_score

accuracy_score(y_test,y_pred)

Result

📈 Accuracy = 0.64 (64%)

9️⃣ Exploratory Data Analysis (EDA)

Some important graphs created.

1️⃣ Study Time vs GPA
sns.scatterplot(x="StudyTimeWeekly",y="GPA",data=df)



2️⃣ Absences Distribution
sns.histplot(df["Absences"])



3️⃣ GPA Distribution
sns.histplot(df["GPA"])




🔟 Conclusion

in this project used to:

✔ Student behaviour data
✔ Logistic Regression model building
✔ Model accuracy 64%

Important factors affecting performance:

StudyTimeWeekly

Absences

ParentalSupport

Tutoring

Future improvement:

More data

Feature engineering

Advanced models

Example:

Random Forest

Gradient Boosting

 Skills Used:

Python

Pandas

NumPy

Matplotlib

Seaborn

Scikit-learn


இந்த 3யும் செய்து தருவேன்.
அது Data Analyst job-க்கு useful இருக்கும்.
