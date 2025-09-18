# Automated Invoice Processing and Anomaly Detection

## Setup Instructions
1. Install Python 3.8 or later.
2. Install the required libraries:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn transformers
   ```
   (Modules like `datetime`, `random`, and `re` are part of Python standard library and do not need installation.)
3. Open the Jupyter Notebook:
   ```bash
   pip install notebook
   jupyter notebook
   ```
4. Run the notebook `Automated Invoice Processing and Anomaly Detection model.ipynb` step by step.

## Project Overview
This project focuses on automating invoice text generation, extraction of key fields, and anomaly detection.  
The steps include:
- Generating synthetic invoices with vendor, invoice number, date, items, and total.
- Extracting and preprocessing structured data from invoice text.
- Applying anomaly detection models to identify unusual or fraudulent invoices.

## Models and Results
1. **Isolation Forest**  
   Initially, Isolation Forest was used to detect anomalies in invoices. While it provided some insights, the overall accuracy and detection reliability were not sufficient for production use.

2. **Random Forest**  
   After labeling anomalies, Random Forest was applied as a supervised model. It delivered much better accuracy, with higher precision, recall, and F1 scores compared to Isolation Forest.  
   This made Random Forest the preferred model for final anomaly detection.

## Key Notes
- Use Isolation Forest for quick, unsupervised anomaly detection.  
- Switch to Random Forest when labeled data is available to achieve more reliable results.
