# Predictive Maintenance Classifier (Sample Project) 

Built a time-boxed (~4 hrs) multi-class machine failure prediction model using the [UCI AI4I 2020 dataset](https://archive.ics.uci.edu/dataset/601/ai4i+2020+predictive+maintenance+dataset), achieving 98.5% accuracy and 0.90 ROC AUC. 

## Explanation
This project demonstrates how predictive analytics can support Quality Engineering workflows such as nonconformance triage, MRB investigations, and RCCA documentation.

## Deliverables

### 🧾 [Jupyter Notebook](https://github.com/gvo27/predictive-maintenance/blob/main/main.ipynb)

Step-by-step data exploration, preprocessing, and model training.

Multi-class Random Forest classifier trained to detect TWF, HDF, PWF, OSF, RNF, and NONE outcomes.

Includes confusion matrix, per-class metrics, feature importance analysis, and ROC AUC.

Interprets feature drivers (e.g., Torque, Tool Wear, Temperature Delta) in the context of root cause analysis.


### 🧾 [PowerPoint](https://github.com/gvo27/predictive-maintenance/blob/main/Quality_Model_Report.pptx)

Model performance, key predictors, and stakeholder significance.

Quality Clinic triage, MRB coordination, and Supplier Quality discussions.


### 🧾 [Predicted NCR Simulation](https://github.com/gvo27/predictive-maintenance/blob/main/predicted_ncr_simulation.csv)

CSV output mapping predicted failure type → recommended disposition action.

Example:

TWF → Replace tool; open NCR; escalate to Tooling

HDF → Investigate cooling; collect temp sensors; open NCR

OSF → Inspect mechanical stress; review torque logs

## Model Results
* Accuracy: 98.5%
* ROC AUC (macro): 0.90
* Strong performance for HDF and NONE classes.
* Lower recall for rare classes (TWF, RNF) → flagged as areas for data augmentation (SMOTE, additional data collection)

## Next Steps
* Interactive Power BI dashboard 
* Improve detection of TWF and RNF via oversampling and rare-class focus.
* Integrate with QMS/ERP systems (e.g., SAP, Windchill, or NCR trackers).
