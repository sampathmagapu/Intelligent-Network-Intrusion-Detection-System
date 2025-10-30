# Intelligent Network Intrusion Detection System (INIDS)

## Author
**Sampath Magapu**  
Email: [sampathmagapu11@gmail.com](mailto:sampathmagapu11@gmail.com)  
LinkedIn: [https://www.linkedin.com/in/sampath-magapu-9b5102253/](https://www.linkedin.com/in/sampath-magapu-9b5102253/)

## Overview
INIDS is a leakage-aware, tunable hybrid network intrusion detection system developed on the UNSW-NB15 benchmark dataset. It combines a supervised XGBoost model and an anomaly detection ensemble composed of PCA and Isolation Forest. The system provides explicit operating-point control via a tunable fusion parameter (alpha), allowing flexible balancing between detection sensitivity and alert precision without retraining.

## Features
- Leakage prevention by removing label proxy features and strictly adhering to official train/test splits.
- Supervised learning using XGBoost with class imbalance handling.
- Anomaly detection using PCA reconstruction errors and Isolation Forest outlier scores.
- Tunable convex fusion with two interpretable parameters: fusion weight (alpha) and alert threshold (tau).
- Comprehensive evaluation metrics: Accuracy, Precision, Recall, F1-score, ROC-AUC, PR-AUC.
- Operational analytics with hourly attack-rate curves and OLAP-style multidimensional rollups.
- Automated HTML/PDF reporting of detection results and analytics.
- Reproducible pipeline with saved model checkpoints and fusion parameters.

## Dataset
This project uses the public UNSW-NB15 dataset for network intrusion detection research.  
Dataset link: [https://research.unsw.edu.au/projects/unsw-nb15-dataset](https://research.unsw.edu.au/projects/unsw-nb15-dataset)  

Please download the official training and testing CSV files from above and place them in the `data/` directory before running the project.

## Installation
```
git clone https://github.com/yourusername/INIDS.git
cd INIDS
pip install -r requirements.txt
```

## Usage
1. Prepare the UNSW-NB15 dataset as described above.
2. Run the Jupyter Notebook `INIDS.ipynb` for preprocessing, training, fusion tuning, and evaluation.
3. Outputs including model artifacts, evaluation metrics, OLAP rollups, and automated HTML/PDF reports will be saved to the `output/` folder.

## Requirements
- Python 3.8+
- scikit-learn
- xgboost
- pandas
- numpy
- matplotlib
- jupyter

## References
- N. Moustafa and J. Slay, "UNSW-NB15: A comprehensive data set for network intrusion detection systems," MilCIS, 2015.
- T. Chen and C. Guestrin, "XGBoost: A scalable tree boosting system," KDD, 2016.
- I. T. Jolliffe, *Principal Component Analysis*, 2nd ed., Springer, 2002.
- F. T. Liu et al., "Isolation Forest," ICDM, 2008.

## License
Specify your license here (e.g., MIT, Apache 2.0).

## Contact
For questions or collaboration, feel free to contact Sampath Magapu at [sampathmagapu11@gmail.com](mailto:sampathmagapu11@gmail.com).
