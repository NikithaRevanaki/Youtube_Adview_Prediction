# YouTube Ad View Prediction

> A machine learning regression model to predict YouTube advertisement views based on video metrics like engagement (likes, comments, dislikes) and video characteristics.

## 📋 Problem Statement

YouTube advertisers pay content creators based on ad views and clicks for marketed goods and services. Accurately predicting ad view counts is essential for:
- **Advertisers** to estimate ROI and campaign performance
- **Content creators** to optimize monetization strategies
- **Platform analytics** to forecast revenue potential

This project builds and compares multiple regression models to predict YouTube ad view counts from video engagement and metadata.

## 📊 Dataset

**Source:** Training dataset contains ~15,000 YouTube videos with comprehensive metrics

**File Structure:**
- `train.csv` - Training data with 15,000+ video records
- `test.csv` - Test data for model evaluation
- `predictions.csv` - Model predictions on test set

**Data Quality:** Raw data contains anomalies and inconsistencies that are cleaned during preprocessing (e.g., character 'F' in numeric fields).

## 📈 Features

| Feature | Description | Data Type |
|---------|-------------|-----------|
| `vidid` | Unique video identification ID | Numeric (encoded) |
| `views` | Number of unique video views | Integer |
| `likes` | Number of video likes | Integer |
| `dislikes` | Number of video dislikes | Integer |
| `comment` | Number of unique comments | Integer |
| `adview` | **[TARGET]** Number of ad views | Integer |
| `published` | Video publication date | Categorical (encoded) |
| `duration` | Video length in seconds | Integer |
| `category` | Video category/niche | Categorical (A-H) |

## 🎯 Objective

Build and evaluate multiple regression models to predict YouTube ad view counts with high accuracy, then select the best-performing model based on evaluation metrics.

## 🛠️ Tech Stack

- **Python 3.x**
- **Data Processing:** Pandas, NumPy
- **Machine Learning:** scikit-learn
- **Visualization:** Matplotlib

## 📝 Methodology

1. **Data Cleaning & Preprocessing**
   - Remove anomalies and invalid entries
   - Convert data types appropriately
   - Handle categorical variables (Label Encoding)
   - Convert duration format to seconds

2. **Feature Engineering**
   - Encode categorical variables (Category, Duration, Published date)
   - Normalize/scale features as needed

3. **Model Training**
   - Train multiple regression models
   - Perform hyperparameter tuning
   - Evaluate using appropriate metrics

4. **Model Evaluation**
   - Compare model performance
   - Select best-performing model

## 🚀 Usage

1. Clone the repository
2. Install dependencies: `pip install pandas numpy scikit-learn matplotlib`
3. Open `Youtube_Adview_Prediction.ipynb` in Jupyter Notebook
4. Run cells sequentially to:
   - Load and explore data
   - Clean and preprocess data
   - Train regression models
   - Generate predictions on test data

## 📌 Key Steps in Notebook

- Data loading and exploration
- Handling invalid values and data type conversion
- Categorical encoding (categories A-H mapped to 1-8)
- Duration format conversion (HH:MM:SS → seconds)
- Model training and comparison
- Prediction generation

## 💡 Results

Model predictions are saved in `predictions.csv` for submission and evaluation.

## 🔄 Future Improvements

- Implement additional regression algorithms (XGBoost, LightGBM, Neural Networks)
- Perform hyperparameter optimization
- Feature selection and engineering refinement
- Cross-validation for robust model evaluation
- Visualization of feature importance
- Model explainability analysis (SHAP values)

## 📄 License

This project is open source and available for educational and research purposes.

## 🤝 Contributing

Contributions are welcome! Feel free to fork, improve, and submit pull requests.
