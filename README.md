# centella_kaggle
👥 Team: centella_kaggle
 | **Name**         
|------------------
| kaylee Nguyen          
| Lorena Milian        
| Jack Le
| India Easton
| Melody Enwerem


🎯 Project Highlights
Model Development: Built a Convolutional Neural Network (CNN) with transfer learning to classify dermatological images based on the Equitable AI for Dermatology Kaggle Challenge.

Performance: Achieved an F1 score of XX.XX and placed in the top X% on the Kaggle Leaderboard.

Explainability: Employed LIME to interpret how the CNN makes predictions, providing insights into key regions in each image.

Fairness Focus: Incorporated data augmentation strategies to address potential biases and improve performance across diverse skin tones (in line with the AJL requirements).

👩🏽‍💻 Setup & Execution
To reproduce our results, follow these steps:

Clone the Repository

git clone https://github.com/username/equitable-dermatology.git
cd equitable-dermatology
Set Up Environment

We recommend creating a new Python virtual environment using venv or conda:
 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
Install required packages:



pip install -r requirements.txt
Access the Dataset

Download the competition data from the Kaggle Competition Page.

Place the dataset files (e.g., images, CSVs) into the data/ directory or update paths accordingly in the notebook.


🏗️ Project Overview
The Equitable AI for Dermatology competition is part of the Break Through Tech AI Program. The challenge focuses on improving machine learning models for dermatological image classification across varying skin tones to ensure equitable healthcare solutions. By developing robust and fair models, this project aims to:

Reduce biases in dermatological diagnoses.

Enhance the reach and quality of AI-based healthcare for underrepresented groups.

Provide insights into model behavior through explainability techniques.



📊 Data Exploration
Dataset:

Provided training images with associated metadata (e.g., skin type labels, demographic info).

Additional open-source images were used to augment the dataset for more diverse representation.

Data Exploration:

Computed basic statistics (mean, median, class distribution).

Detected missing values in patient metadata and imputed them using domain-informed approaches.

Conducted Exploratory Data Analysis (EDA) with histograms, box plots, and correlation heatmaps to identify potential trends or biases.

Key Takeaways:

Skin-tone distribution was initially skewed toward lighter tones.

Disease class distribution was slightly imbalanced, prompting oversampling and data augmentation.



🧠 Model Development
Model Architecture

Implemented a CNN (ResNet50 backbone) with transfer learning from ImageNet weights.

Fine-tuned the last few layers to adapt to dermatological features.

Hyperparameter Tuning

Used grid search over learning rates and batch sizes.

Experimented with early stopping and dropout to mitigate overfitting.

Data Splits & Evaluation

Training/Validation split of 80/20.

Tracked performance using F1-score and AUC on the validation set.

Employed K-fold cross-validation (5 folds) to ensure robust performance estimates.

Fairness-Driven Data Augmentation (AJL)

Applied targeted augmentation on underrepresented skin types, balancing the distribution without overfitting.




📈 Results & Key Findings
Overall Performance

F1-score: XX.XX

Precision: YY.YY | Recall: ZZ.ZZ

Kaggle Leaderboard rank: Top X% (out of N teams)

Performance Across Different Skin Tones

Minimal performance gap (~2-3% F1-score difference) between lighter and darker skin tones after augmentation.

Provided promising evidence that our fairness-focused methods helped reduce bias.

Explainability Insights

LIME heatmaps revealed consistent focus on lesion areas across varying skin tones.

Model occasionally struggled with images in poor lighting conditions, suggesting a need for improved data collection standards.



🖼️ Impact Narrative
Algorithmic Justice League (AJL) Perspective
Fairness Steps

We specifically augmented images from underrepresented skin tones, ensuring the model sees a more balanced dataset.

We maintained a separate validation set to regularly assess fairness metrics (e.g., F1 by skin tone group).

Broader Impact

A more equitable dermatological classification model could aid clinicians in diagnosing skin conditions across diverse populations.

It highlights the importance of representation in medical imaging datasets and how targeted augmentation can mitigate biases.



🚀 Next Steps & Future Improvements
Enhance Model Complexity: Explore Vision Transformer (ViT)-based approaches for potentially better feature extraction.

Incorporate Additional Data: Gather more real-world, diverse datasets to improve the generalizability of the model.

Refine Fairness Metrics: Investigate more granular fairness metrics (e.g., Equalized Odds, demographic parity) and integrate them into the training loop.

Domain-Specific Preprocessing: Use clinically relevant data cleaning and standardization (e.g., removing artifacts, standardizing lighting conditions).



📄 References & Additional Resources
Algorithmic Justice League: Fairness Guide

LIME for Explainability: GitHub Repository

ResNet Paper: He, K. et al. (2015)

Break Through Tech AI Program: Official Website


