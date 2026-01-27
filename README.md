# Mental-Diagnosis-and-Treatment-Monitoring (Interactive Dashboard using Power BI)
## Project Overview
This project focuses on the analysis and visualization of mental health diagnosis and treatment data using Power BI. The dataset contained detailed records of hundreds of patient including demographic information (age,gender), clinical diagnosis, sympton severity, treatment types, adherence rates and outcomes.

## Dataset used
- <a href="https://github.com/aochristianah/Mental-Diagnosis-and-Treatment/blob/main/mental_health_diagnosis_treatment_.csv">Dataset</a>

## Data Description
- Patient ID: Unique identifier.
- Age: Age of the patient.
- Gender: Male or Female.
- Diagnosis: Mental health condition (e.g., Anxiety, Depression).
- Symptom Severity (1-10): Severity of symptoms.
- Mood Score (1-10): Mood rating during treatment.
- Sleep Quality (1-10): Patient-reported sleep quality.
- Physical Activity: Hours per week of activity.
- Medication: Medications prescribed (e.g., SSRIs, Antidepressants).
- Therapy Type: Type of therapy (e.g., Cognitive Behavioral Therapy, Dialectical Behavioral Therapy).
- Treatment Start Date: Date treatment started.
- Treatment Duration: Duration of treatment in weeks.
- Stress Level (1-10): Patient's stress level.
- Outcome: Treatment outcome (e.g., Improved, Deteriorated).
- Treatment Progress (1-10): Progress made during treatment.
- AI-Detected Emotional State: AI-detected emotional state (e.g., Happy, Anxious).
- Adherence to Treatment (%): Percentage of adherence to treatment plan.

## KPI's Requirement
- Diagnosis Classification: Classify patients based on their mental health condition.
- Outcome Prediction: Predict treatment outcomes based on patient data.
- Adherence Monitoring: Analyze treatment adherence and its effect on outcomes.
- Emotional State Detection: Use AI to track and predict emotional states.
- Treatment Effectiveness: Evaluate the impact of different therapies on progress.
- Age group distribution: distribution of patients across age groups for each diagnosis
- Overall Improvement Rate.

## Analysis Steps
- Defined the problem and set the objective.
- Understood the data: The data used was reviewed to understand its structure, variables and data types.
- Import data.
- Data cleaning and prepation: Removed duplicate, checked for blanks, standardized categorical values and created consistent age group.
- Data Transformation: New metrics and calculate feilds were created to support analysis.
- Exploratory Data Analysis: EDA was conducted to identify patterns and trends: Analyzed patient count distribution across diagnosis, compared age group distributions across mental health conditions. analysed symptom level by diagnosis.
- KPI Definition and Validation.
- Dashboard design and Visualization.

## DAX Formulas used
- Number of Patients

Count of Patient ID = COUNT('in'[Patient ID])
- Improvement Rate

Improvement Rate = DIVIDE(CALCULATE(COUNTROWS('in'),'in'[Outcome]= "Improved"), COUNTROWS('in')) 
- Average Adherence 

Average Adherence = AVERAGE('in'[Adherence to Treatment (%)]) 
- Average Age

Average Age = AVERAGE('in'[Age]) 
- Age Group 

Age Group = SWITCH(TRUE(), 'in'[Age]<20,"0-19", 'in'[Age]<40, "20-39", 'in'[Age]<60, "40-59", "60+")
  
## Power BI Dasshboard
<img width="1281" height="727" alt="Screenshot (11)" src="https://github.com/user-attachments/assets/1ec967be-804e-4456-95cd-0a78ad5be329" />

## Project Insights
- Generalised Anxiety Disorder has the highest number of patient in the dataset, making it the most common mental health condition among patients.
- Only about one-third patients showed improvement after treatment, while the rest experienced no change or their condition worsened.
- Patient who adhered more closely to thier treatment plans were more likely to fall into the "Improved" outcome category.
- Among the therapy type analyzed, Interpersonal Therapy recorded the highest average treatment progress score.
- Negative emotional states such as anxiety, stress and depression are highly common among patients.
- Most patients fall withi the age range of 20-59, showing that mental health issues are most concentrated among working-age individuals.
- Some patients recieved long-term treatment and still showed no improvement or even deterioration, indicating inefficiencies in treatment plans.

## Recommendations
-

## Conclusion
Overall, this dashboard shows that mental health outcome depend heavily on treatment type, patient adherence, personalization of care and regularly evaluating treatment effectiveness can significantly improve patient outcomes.
