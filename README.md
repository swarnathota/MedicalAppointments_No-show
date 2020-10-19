# Medical Appointments No-Shows

##Overview

The goal of this project is to investigate a dataset of appointment records for Brazil public hospitals. The data includes some attributes of patients and using those variables I tried to predict No-Show. The analysis is focused on finding trends influencing patients to show or not show up at the time of appointment.

##Exploratory Data Analysis

####Questions needed to be answered to find any patterns

- Who skipped most of the appointments male or female?

- How many No-shows by age?

- Are No-shows affected by wait times?

- How many skipped appointments even after an SMS reminder?

- Having any medical history such as Hypertension affected No-show?

- What Weekday most of the appointments are skipped?

- What Neighborhood most likely to skip an appointment?

## Feature Engineering

#####1) Weekday Appointment

Process date time object and extract new features such as from it - scheduling day or appointment day of the week. Weekday appointments might not be convenient for the patients but it appears to be their only option that might lead to no-show.

#####2) previous appointments

How many appointments were taken by the patient before current scheduling day?

#####3) Missed appointments

How many appointments are missed by the individual patient before current scheduling day. This tells the pattern of the individual patient that they are likely to miss future appointments too.

##### 4) Neighborhood

 Certain neighborhoods can be a demographic barrier to miss an appointment. Categorize neighborhoods into groups based on the number of appointments in that area.

#####5) previous disease

 Usually having any kind of ailments can cause anxiety or fear that can result in a patient no-show.

## Modeling

In the EDA I found 25% of the patients missed the appointments and this finding aligns with research by Forbes and Pits burgh where they mentioned yearly 25% of patients miss their appointments. Patient no-shows cost the health care industry 150 billion annually. For a primary care physician, each missed appointment costs roughly 150-200 dollars in lost revenue and for surgeons, this is close to 500 dollars.

 Predicting show or no-show of an appointment makes it a classification problem and the ratio of no show to show is 3:1 that makes the data imbalanced.

 Logistic Regression is performed to predict classes appointment "show" and "no-show" with:

- An accuracy of 93%

- Since our data is imbalanced, a better evaluation metric would be F1-score which is around 86%. It implies that the more the F1 score the less chances of predicting false positives and false negatives.

##Model usage

This model would help to find who the patients are likely to skip doctor’s appointments and we can always double book the appointment or send reminders. In that way the financial burden on the health care system can be answered. This model saves time as well as money to the care physicians and healthcare system overall.

 Sometimes patients  fail to show up for their appointments inspite of sending reminders and they require more expensive emergency care later on. In such cases we need to conduct extensive interviews with the patients and know why they are not appearing. Using interview materials as text we can apply ML techniques such as Natural Language Processing, find answers, and provide the help needed.

 

















