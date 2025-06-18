
# Capstone Project: Human Body Measurement Estimation from 2D Data

This capstone project explores the use of machine learning models to estimate human body measurements, with a focus on waist prediction, using 2D anthropometric data. The project involves data analysis, synthetic data generation, model training, evaluation, and documentation.

## 🗣️ Non-Technical Summary

This project uses machine learning to predict a person’s waist measurement based on other body dimensions like shoulder width, chest size, and leg length. By analyzing patterns in physical measurements from over 700 individuals, the model can estimate waist size without needing direct measurement. We tested four different algorithms and found that the Random Forest model gave the most accurate results. This kind of model can support applications in fashion, fitness, or health, offering sizing suggestions or tracking changes in body shape — all without needing expensive equipment or intrusive methods.

## 📁 Project Structure

- `Body_Measurements_Dataset_Datasheet.md`: Datasheet describing the Kaggle dataset used.
- `Waist_Prediction_Model_Card.md`: Model card summarizing four regression models.
- `Body_Measurements_Dataset_Datasheet_Revised_With_Synthetic.md`: Updated datasheet including synthetic data context.
- `Body Measurements _ original_CSV.csv`: Original dataset containing physical body measurements.

## 📊 Dataset

- **Source**: [Kaggle: Body Measurements Dataset](https://www.kaggle.com/datasets/saurabhshahane/body-measurements-dataset)
- **Size**: 716 records
- **Features**: Age, Gender, Head Circumference, Shoulder Width, Chest Width, Belly, Waist, Hips, Arm Length, Leg Length, etc.
- **Target**: Waist circumference

## 🧪 Methods

### Data Preparation
- Data cleaning and standardization
- Bootstrapping to enhance training volume

### Synthetic Data Generation
- Used `CTGANSynthesizer` from the SDV library to create synthetic data samples for data augmentation and testing

### Models Used
- **Random Forest Regressor**
- **Linear Regression**
- **Support Vector Regressor (SVR)**
- **Decision Tree Regressor**

### Evaluation Metrics
- Mean Squared Error (MSE)
- Mean Absolute Error (MAE)
- R² Score
- Cross-Validation Score (5-Fold)

## 📈 Results

Random Forest outperformed other models in both R² and cross-validation accuracy. SVR had the lowest performance, likely due to scaling and kernel limitations on this dataset.

## ⚠️ Limitations

- Small and possibly non-diverse dataset
- Absence of demographic attributes (e.g., ethnicity, geographic location)
- Focuses only on waist prediction

## 📌 Future Work

- Expand to multi-output predictions (e.g., predicting multiple measurements)
- Incorporate deep learning architectures (e.g., CNN with image silhouettes)
- Address bias through synthetic data balancing

## 👤 Author

Capstone Project by Grant Van Wyk  
Course - Professional Certificate in Machine Learning and AI  
Imperial College London

## 📅 Date

June 2025
