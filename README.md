# VIR_AJL_Team-Exfoliant

## 👥 Team Members
- **Jenylee Diaz Munoz | @beelee115**  
- **Sara Abdulla | @oreo-cake**
- **Rohitha Sanka | @rsanka12**
- **Naseeha Masub | @**
- **Waverly Souvannachack | @**
- **Muskaan Thapar | @**

## 🌟 Project Highlights
* Achieved an F1 score of 0.06269 and a ranking of 56 on the final Kaggle Leaderboard

🔗 [Equitable AI for Dermatology | Kaggle Competition Page](https://www.kaggle.com/competitions/bttai-ajl-2025/overview)

## ⚙️ Setup & Execution
Follow these steps to set up your environment and run the code for the Kaggle competition.

**1️⃣ Clone the Repository**

git clone <repository-url>
cd VIR_AJL_Team-Exfoliant

Replace <repository-url> with the actual URL of your GitHub repository.

**2️⃣ Install Dependencies**

Ensure you have Python installed. Then, install the required dependencies:

pip install -r requirements.txt

If you do not have a requirements.txt file, manually install the necessary libraries:

pip install pandas numpy scikit-learn matplotlib seaborn kaggle

**3️⃣ Set Up the Environment**

Ensure you have the necessary environment set up for running Python scripts. You may use a virtual environment:

python -m venv env
source env/bin/activate  # On macOS/Linux
env\Scripts\activate  # On Windows

**4️⃣ Access the Dataset**

The dataset files (train.csv and test.csv) are already included in the repository. Ensure they are in the root directory:

project-folder/
│── train.csv
│── test.csv
│── exfoliant.py
│── vir-ajl-team-exfoliant-sub-2.py
│── README.md

**5️⃣ Run the Script**

Execute the script in the command line:

python vir-ajl-team-exfoliant-sub-2.py

Replace vir-ajl-team-exfoliant-sub-2.py with the appropriate script name if needed.
## 📌 Project Overview
**🏆 The Competition & Break Through Tech AI**

This project is part of the Break Through Tech AI/ML Fellowship, where we are competing in the Equitable AI for Dermatology Build Competition on Kaggle. Hosted in collaboration with the Algorithmic Justice League (AJL), the challenge brings together AI fellows to develop machine learning solutions that promote fairness and inclusivity in dermatological AI.

**🎯 Objective of the Challenge**

Our goal is to build a machine learning model that accurately classifies 21 different skin conditions across diverse skin tones. Traditional dermatology AI tools often struggle with misdiagnosis for people with darker skin due to biased datasets. By improving model performance for underrepresented groups, we aim to create a more equitable and inclusive AI system.

**🌱 Real-World Impact**

Misdiagnosis in dermatology can lead to delayed treatments, poor health outcomes, and systemic disparities in healthcare. By ensuring our model works well across all skin tones, we contribute to advancing AI fairness and reducing bias in medical AI tools. Our work aligns with AJL’s mission to illuminate AI harms and promote ethical, responsible AI development.

## 📊 Data Exploration

**🗂 Dataset Overview**

Our dataset consists of dermatological images categorized into 21 different skin conditions, with metadata such as Fitzpatrick skin type, Dermatological Diversity Index scale (ddi_scale), and Quality Control scores (qc scores). 

**🔍 Key Insights & Challenges**

Class Imbalance: Some skin conditions are significantly underrepresented, which may impact model performance.

Outliers in ddi_scale: Potential anomalies in the dataset require careful handling.

Missing & Duplicate Data: Preprocessing includes checking for and addressing any inconsistencies.

**📊 Visualizations & Analysis**

Class Distribution: Understanding the prevalence of each skin condition in the dataset.
![image](https://github.com/user-attachments/assets/611c3090-002d-49d7-ba45-76803b351a80)

Outlier Detection: Identifying unusual values in metadata like ddi_scale.
![image](https://github.com/user-attachments/assets/eec3e56e-f970-43da-b96c-23fe695d81f8)

Skin Tone Representation: Ensuring fair inclusion across different skin types
![image](https://github.com/user-attachments/assets/35dd9b12-19a0-4bef-9880-c9ca66f2bcce)

## 🧠 Model Development
Our submission contains a Convolutional Neural Network (CNN) which is used for multi-class image classification. Our team utilized TensorFlow, an open-source machine learning framework, that also integreates Keras, a highl-level networks API to make the model easier to build. Team Exfoliant decided to select a CNN architecture for its effectiveness in image classification. We made three convolutional layers with RELU activation and max pooling and fully connected the layers with dropout for regularization. With many of our projects, we also used train_test_split for dataset partitioning to ensure our model works with different kinds of data (generalization). Below are some of the hyperparameters and why we decided to use these specific values.
Hyperparameter Tuning:

Filter Sizes & Layers: A progressive increase in convolutional filters (32 → 64 → 128) enhances feature extraction. We progressively increased the number of kernels (filters) to allow the network to learn hierarchical representations.

Dropout (0.5): It is a regulariztion technique that randomly deactivations some neurons while the model is training. This was so that our model didn't have to rely on just specific neurons to learn, but rather allows 50% of the neurons to train and reduce overfitting. We chose 0.5 because it is a good balance to maintain enough information but also reduce overfitting.

Optimizer (Adam): Adam adapts the learning rate individually for each parameter as it helps speed up convergence and adjust the learning rate for different parameters. We used Adam as it is widely used in CNNs in difficult/complex feature spaces.

Batch Size (32) & Epochs (10): Achieve sufficient model training while avoiding overfitting. We wanted a model that didn't run for too long but was able to test out a good amount of data.

For our training pipeline, our data is split into training and validation sets using a 80/20 split which is a balanced split that allows us to train on different parts of the data.

## 📈 Results & Key Findings
**Model Performance Overview**
Leaderboard Score: Achieved a Kaggle leaderboard score of 60, reflecting decent overall performance with room for improvement. The model demonstrated steady learning but showed variability in validation accuracy.

**Fairness & Inclusivity**
Skin Tone Evaluation: The model currently lacks explicit evaluation across different skin tones. We recognize the importance of fairness and bias testing in our model, especially for dermatological applications where skin tone diversity is crucial.

Next Steps: Future work will include evaluating model performance using fairness metrics like demographic parity and equalized odds, as well as ensuring equal accuracy across skin tone groups to promote inclusivity.

**Model Evaluation Insights**
Performance Variability: The model shows potential but struggles with generalization. Future improvements will focus on enhancing robustness and fairness across all demographic groups.

Future Goals: Plans to implement fairness-aware techniques, data augmentation, and better hyperparameter tuning to address performance gaps and reduce bias.

**Next Steps**
If we had more time, we would include:

Confusion Matrix: To better understand misclassifications.

Fairness Metrics: To evaluate performance across skin tones and mitigate potential bias.

Feature Importance & Explainability: To enhance transparency and model trustworthiness.

## 🖼️ Impact Narrative
**🌍 Advancing Fair & Inclusive AI in Dermatology**

Our machine learning model aims to classify 21 skin conditions while addressing bias in dermatology AI. Traditional models often misdiagnose darker skin tones due to biased datasets. By improving fairness, we strive for a more equitable AI system.

**📊 Addressing Model Fairness**

Used diverse data sources to improve representation but recognize the need for explicit fairness testing.

Plan to implement fairness metrics like demographic parity and equalized odds to assess model performance across skin tones.

Future improvements will focus on fairness-aware techniques, data augmentation, and hyperparameter tuning to mitigate bias.

**🌱 Broader Impact**

Reducing AI bias in dermatology can improve diagnostic accuracy for underrepresented groups, leading to better health outcomes.

Promotes ethical AI development and aligns with efforts to create more inclusive medical tools.

Enhancing model transparency through fairness testing can increase trust in AI-driven healthcare solutions.

By prioritizing fairness and inclusivity, we take a step toward responsible AI in healthcare. 🚀
## 🚀 Next Steps & Future Improvements
As a team, for our next steps we think that communication and more efforts could result in a higher accuracy. As we make those changes, our tool would make a higher impact. 
