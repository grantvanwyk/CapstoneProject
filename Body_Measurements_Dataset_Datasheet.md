
# Datasheet for Body Measurements Dataset

## 1. Motivation

- **Purpose**: This dataset was created to support machine learning research in body classification, health analytics, biometric modeling, and clothing size prediction.
- **Intended Tasks**: Classification tasks (e.g., gender prediction), regression tasks (e.g., height, age estimation), and exploratory body feature modeling.
- **Creators**: The dataset was uploaded to Kaggle by Saurabh Shahane. There is no affiliation explicitly stated.
- **Funding**: No formal funding disclosed on Kaggle.

## 2. Composition

- **Instances Represented**: Each row in the dataset represents a single individual described by 13 body measurement attributes.
- **Number of Instances**: 716 individuals.
- **Sampling Method**: Not disclosed.
- **Representativeness**: Dataset includes both males (391) and females (324); ethnic or geographic diversity is not mentioned.
- **Data Types**:
  - Gender (M=1, F=2)
  - Age (1 year and above)
  - HeadCircumference
  - ShoulderWidth
  - ChestWidth
  - Belly
  - Waist
  - Hips
  - ArmLength
  - ShoulderToWaist
  - WaistToKnee
  - LegLength
  - TotalHeight (Head to toe)
- All measurements are in inches.
- **Label**: No specific target label defined; dataset is open to exploratory modeling.
- **Missing Data**: None reported.
- **Confidential or Sensitive Data**: Dataset appears anonymized and does not include any direct identifiers.

## 3. Collection Process

- **How Was Data Collected?**: Not specified. Likely via manual measurement from subjects.
- **Sampling Strategy**: Not disclosed.
- **Timeframe**: Unknown.

## 4. Preprocessing/Cleaning/Labeling

- **Preprocessing Done**: Data appears clean and numeric with no missing values.
- **Raw Data Availability**: No indication of whether raw unprocessed data was saved.
- **Labeling**: No specific class label defined; "Class Label" column exists but not documented.

## 5. Uses

- **Intended Uses**: Predictive modeling, health analytics, biometric modeling, clothing fit prediction.
- **Other Potential Uses**: Ergonomics, fitness, child growth analysis.
- **Ethical Considerations**: Avoid misuse for discriminatory profiling; ensure fairness in health-related applications.
- **Tasks It Should Not Be Used For**: Critical medical diagnostics or policy decisions without extensive validation.

## 6. Distribution

- **Availability**: Publicly available on [Kaggle](https://www.kaggle.com/datasets/saurabhshahane/body-measurements-dataset/data).
- **License**: No explicit license mentioned.
- **Access Restrictions**: None for registered Kaggle users.

## 7. Maintenance

- **Support Contact**: Via Kaggle comments directed to uploader Saurabh Shahane.
- **Updates**: No updates or changelogs noted.
- **Ongoing Maintenance**: Dataset appears static.

## 8. Synthetic Data

- **Was synthetic data used?** Yes. The original dataset consists entirely of real, manually collected anthropometric measurements from human subjects. However the amount of samples was low and therefore Synthetic data was also used to train the models. 
- **Could synthetic data be beneficial?** Yes. Synthetic data could be used to augment this dataset, especially to balance underrepresented subgroups (e.g., certain age ranges or body types) or simulate more diverse demographic distributions.
- **Risks of using synthetic data**: If not carefully generated, synthetic data may introduce unrealistic correlations or reinforce biases present in the original data. Proper validation would be necessary.
- **Recommended Applications**: Use synthetic augmentation for robustness testing, privacy-preserving modeling, or to support deep learning model training where sample sizes are limited.
- **How was the Synthetic Data Generated**: Synthetic data was generated using the CTGAN (Conditional Tabular GAN) model from the SDV library, which was trained on a cleaned dataset with metadata automatically detected, enabling the synthesizer to learn the statistical structure of the original data and produce 1,000 synthetic samples that preserve the original data's distributions and constraints.
