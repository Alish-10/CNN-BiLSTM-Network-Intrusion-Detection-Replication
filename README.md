# **Efficient CNN-BiLSTM Model Replication for Network Intrusion Detection**

## **Project Overview**
This repository contains the replication of Jay Sinha's research project, where an Efficient CNN-BiLSTM Model was implemented for Network Intrusion Detection using NSL-KDD and UNSW-NB15 datasets. This replication involved re-running the model on the same datasets to verify the results and gain insights into the research process. The project was undertaken to explore machine learning research methodologies, understand the research process, and analyze the results.



## **Datasets Used**

- **NSL-KDD**: A refined version of the KDDCup’99 dataset with reduced redundancy and improved training/testing sets for Network Intrusion Detection Systems (NIDS).
- **UNSW-NB15**: A comprehensive dataset with more diverse attack categories, used to test the robustness of the model.

## **Methodologies**

- **Data Preparation**:
  - **Normalization**: Min-Max Normalization is applied to rescale data to the range [0,1].
  - **One-Hot Encoding**: It is used to encode categorical variables to avoid model misinterpretation of data order.
  - **Oversampling**: It is applied to the UNSW-NB15 dataset to handle class imbalance issues especially in categories like Worms and Fuzzers.
  - **Stratified K-Fold Cross Validation**: It ensures robust parameter tuning and classification.

- **Model Architecture**:
  The model integrates a 1-Dimensional Convolutional Neural Network (1-D CNN) with multiple Bi-LSTM layers, including Reshape and Batch Normalization layers to optimize feature extraction and reduce overfitting.
  - **1-D CNN Layers**: For spatial feature extraction.
  - **BiLSTM Layers**: For capturing temporal dependencies in the data.
  - **Batch Normalization and Max Pooling**: Used to prevent overfitting and optimize model performance.
  - **Dropout Layer**: Incorporated to further reduce overfitting risks.
  - **Fully Connected Dense Layer**: Served as the output layer for final predictions.

## **Evaluation Metrics**

- **Accuracy (ACC)**
- **Detection Rate (DR)**
- **False Positive Rate (FPR)**
- **F1-Score**
- **ROC-AUC Curve**

## **Results**

### **Binary Classification:**
- **NSL-KDD**:
  - **Accuracy**: 99.03% on average
  - **Highest Accuracy**: 99.42%
  - **Detection Rate**: 98.02%
  - **False Positive Rate**: 0.24%

- **UNSW-NB15**:
  - **Accuracy**: 91.95% on average
  - **Highest Accuracy**: 92.71%
  - **Detection Rate**: 93.36%
  - **False Positive Rate**: 7.23%

### **Multi-class Classification:**
- **NSL-KDD**:
  - **Accuracy**: 99.02% on average
  - **Highest Accuracy**: 99.62%
  - **F1-Score**: 0.96

- **UNSW-NB15**:
  - **Accuracy**: 81.9% on average
  - **F1-Score**: 0.53
  - **Discrepancy**: The original research reported a detection rate of 92.51% and an F1-Score of 0.74, indicating a significant difference in the results of this replication.

## **Learning and Insights**

This project was conducted to deepen understanding of machine learning research processes, including data preparation, model training, and result analysis. The discrepancies observed, especially in the UNSW-NB15 multi-class classification results, highlight the importance of rigorous experimentation and validation in research. This experience provided valuable insights into the challenges of replicating complex models and the potential variability in outcomes due to dataset characteristics and model tuning.

## **Resources**

- **Colab Notebook NSL-KDD**: [Link to Colab Notebook]( https://colab.research.google.com/drive/1Ryte-kEg1aOQDYcl_xF-veaJOPcAh1et?usp=sharing)  
- **Colab Notebook UNSW-NB15**: [Link to Colab Notebook]( https://colab.research.google.com/drive/1cD-A-ToovakbDmrzdCf-1TXyQD86hF-n?usp=sharing)  

- **Datasets**:
  - [NSL-KDD Dataset](https://drive.google.com/drive/folders/1oXg_AxHPREXxL-jsX6gj5hSsjIrV6l4c?usp=sharing)
  - [UNSW-NB15 Dataset](https://drive.google.com/drive/folders/1QzqHQFLDzERSL9fBP0rDsCzjKVhK0YTT?usp=sharing)
- **Project Summary PDF**: [Link to PDF Summary](https://drive.google.com/file/d/1ek4QS35fSlhIva2OOt1PPOrn-f_b27gR/view?usp=sharing)
