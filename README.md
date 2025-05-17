## Data Preparation
1. Download the Kuairec dataset.
2. The EDA notebook will load these files and output cleaned CSVs in `processed_data/`.

## Usage

### 1. Exploratory Data Analysis (`eda.ipynb`)
This notebook covers:
- **Data Loading**: Importing libraries and reading the raw dataset  
- **Quick Data Inspection**: Initial look at dimensions and missing values  
- **Data Cleaning**: Handling missing values, formatting, and consistency checks  
- **Data Analysis per File**: Univariate and bivariate analyses, including a “Big Matrix” overview  
- **Clean Data Saving**: Exporting cleaned data to `processed_data/`  

### 2. Feature Engineering & Model Development (`feature_engineering_and_model.ipynb`)
This notebook assumes you have already run the EDA notebook. It covers:
- **Data Loading**: Reading cleaned CSVs  
- **Categorical Data Preprocessing**: Encoding multi-label features with `MultiLabelBinarizer`  
- **Definition of Feature Groups**: Organizing user and video attributes  
- **Extraction & Encoding of Daily Video Features**  
- **User Feature Selection & Formatting**  
- **Train/Test Set Preparation**: User–video interaction splits  
- **Feature Extraction for Training/Test Sets**  
- **Normalization**: Standard scaling of features and targets  
- **Dimensionality Reduction**: PCA on feature sets  
- **Neural Network Construction**:  
  - Item tower  
  - User tower  
  - Two-tower combined model  
- **Model Training**: With early stopping callbacks  
- **Predictions & Rescaling**: Generating and adjusting output scores  
- **Top-K Evaluation Prep**: Formatting data for ranking metrics  
- **Final Evaluation**: Computing NDCG, Precision@K, Recall@K and comparing to baseline  

## Results
- Trained model files are stored in root.  
- Evaluation metrics (NDCG, Precision@K, Recall@K) are available at the end of the notebook.  
