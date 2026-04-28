### Capstone Assignment: Initial Report and Exploratory Data Analysis

**Aidan Caldararo**

#### Executive summary
This project explores how machine learning can be used to detect malicious network activity based on patterns in network traffic data. Through exploratory data analysis and a baseline classification model, the goal is to identify key features that distinguish normal traffic from potential cyber threats. The findings aim to support faster and more accurate threat detection in real-world cybersecurity environments.

#### Rationale
Cyberattacks continue to increase in both frequency and complexity, making it difficult for traditional rule-based security systems to detect new or evolving threats. Security teams are often overwhelmed with large volumes of alerts, many of which are false positives. If malicious activity is not identified quickly, organizations risk data breaches, financial loss, and operational downtime.

This project matters because it explores how machine learning can help security teams focus on the most critical threats by identifying patterns in network traffic that may not be obvious through manual analysis. Improving detection accuracy and reducing false alarms can lead to faster response times and better protection of organizational assets.

#### Research Question
Can machine learning models accurately classify network traffic as benign or malicious based on network flow features?

#### Data Sources
This project will use publicly available intrusion detection datasets such as:

CIC-IDS2017 dataset
UNSW-NB15 dataset

These datasets include labeled network traffic data with features such as IP addresses, ports, protocols, packet sizes, flow duration, and attack classifications.

#### Methodology
The approach for this project includes:

- Data Cleaning: Handling missing values, removing duplicates, encoding categorical variables, and preparing the dataset for analysis
- Exploratory Data Analysis (EDA):
  - Visualizing class distributions (benign vs. malicious)
  - Analyzing feature distributions (packet size, duration, byte counts)
  - Using correlation heatmaps to identify relationships between variables
  - Comparing feature behavior across attack types
- Feature Engineering: Scaling numeric features and selecting relevant variables
- Baseline Model:
  - Logistic Regression classifier
  - Train/test split for validation
- Evaluation Metrics:
  - Accuracy
  - Precision
  - Recall
  - F1-score
  - Confusion matrix

#### Results
The exploratory data analysis showed that malicious and benign traffic are not evenly distributed, which is important because class imbalance can affect model performance. Several network traffic features appear to differ between benign and malicious activity, including duration, packet counts, byte counts, and connection-related variables.

The baseline Logistic Regression model provides an initial benchmark for performance. For cybersecurity use cases, recall is especially important because a false negative means malicious traffic was missed. Precision is also important because too many false positives can overwhelm security analysts.


#### Next steps
To improve performance and expand the analysis, the following steps are recommended:

Test additional models such as Random Forest, Decision Trees, KNN, and SVM
Perform hyperparameter tuning to optimize model performance
Explore dimensionality reduction or feature selection techniques
Address class imbalance using resampling methods if necessary
Incorporate anomaly detection techniques for unknown or zero-day attacks
Translate findings into actionable insights for security teams (e.g., alert prioritization strategies)
