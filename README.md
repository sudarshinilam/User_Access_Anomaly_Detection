# User_Access_Anomaly_Detection
## Project Overview
This project focuses on detecting anomalous user access patterns in a system using machine learning. Identifying unusual access helps organizations prevent potential security breaches, insider threats, and unauthorized account usage.

## Dataset
- **Format:** CSV file (`user_access_logs.csv`)
- **Number of Records:** 1,000 (sample dataset, can be scaled)
- **Features Include:**
  - `UserID` – Unique identifier for each user
  - `LoginTime`, `LogoutTime` – Access timestamps
  - `IP_Address` – Source IP of access
  - `DeviceType` – Desktop, Mobile, Tablet
  - `Location` – Geographical location of login
  - `FailedLoginAttempts` – Number of consecutive failed logins
  - `SessionDuration` – Duration of the session in minutes
  - `ResourceAccessed` – Resource accessed by the user
- **Target Variable:** `CLASS_LABEL` (0 = Normal, 1 = Anomalous)

## Project Methodology
1. **Data Preprocessing**
   - Handling missing values
   - Encoding categorical features
   - Scaling numerical features

2. **Feature Engineering**
   - Calculate session duration
   - Count failed login attempts
   - Track access frequency and unusual patterns

3. **Modeling**
   - **Supervised Approach:** Random Forest Classifier, Logistic Regression, XGBoost (if labels are available)
   - **Unsupervised Approach:** Isolation Forest, One-Class SVM, Autoencoder (if labels are not available)

4. **Evaluation**
   - Metrics: Accuracy, Precision, Recall, F1-score
   - Confusion matrix
