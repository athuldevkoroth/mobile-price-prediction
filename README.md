# 📱 Mobile Phone Price Prediction

Predicting the price range of a mobile phone based on its hardware specifications using Machine Learning.

### 📘 Business Problem

Bob has started his own mobile phone company and wants to compete with major brands such as Apple and Samsung. However, he struggles to determine the correct price for the mobile phones his company produces.

In today's highly competitive smartphone market, pricing cannot be based on assumptions or guesswork. To make informed decisions, Bob collects sales data from various mobile companies, including important features such as RAM, internal memory, battery capacity, screen dimensions, pixel resolution, and more.

His goal is to discover how these hardware specifications influence the price range of a mobile phone. But since Bob is not familiar with Machine Learning, he needs an intelligent model that can analyze these features and accurately predict the appropriate price category.

Your task is to build a machine learning solution that helps Bob estimate the correct **price range** for his new mobile phones based on their specifications.

### 📌 Project Overview

The goal of this project is to build a machine learning model that predicts the price range of a mobile phone (0 = Low, 1 = Medium, 2 = High, 3 = Very High) using its technical specifications.

The dataset contains mobile features such as battery power, internal memory, RAM, screen size, pixel resolution, camera specs, and various network-related features.

This is a multi-class classification problem, and several machine learning models were trained and compared to identify the best-performing model.

### 💾 Saved Files

- **cellphone_price_model.pkl** → Final trained machine learning model  
- **cellphone_scaler.pkl** → StandardScaler used for feature scaling during training  
- **cellphone-price.csv** → Original dataset  
- **final_cellphone_price.ipynb** → Complete Jupyter Notebook containing the entire project workflow  
- **domain analysis.pdf** → Documented domain understanding and feature study  
- **requirements.txt** → List of required Python libraries and dependencies 

### 🧠 Domain Analysis

**Target / Dependent Feature:**  
`price_range`

**Input / Independent Features:**  
`battery_power`, `blue`, `clock_speed`, `dual_sim`, `fc`, `four_g`,  
`int_memory`, `m_dep`, `mobile_wt`, `n_cores`, `pc`, `px_height`,  
`px_width`, `ram`, `sc_h`, `sc_w`, `talk_time`, `three_g`,  
`touch_screen`, `wifi`

This data helps us predict the **phone price category** based on various hardware specifications and mobile features.

### 🧹 Initial Data Checks & Cleaning

- Verified dataset shape and column types  
- No missing values found  
- No duplicate rows  
- All features were numeric → no encoding required  
- Binary features validated (0/1)  
- Outlier inspection performed (no removal necessary)  

**Feature engineering added:**
- `pixel_area` = px_height × px_width  
- `aspect_ratio` = px_width / px_height  

After these checks and preprocessing steps, the dataset was ready for **Exploratory Data Analysis (EDA)** and model building.

---

### 📊 Exploratory Data Analysis (EDA)

**Key Findings:**

- **RAM** is the strongest predictor of price range  
- Larger **battery power** and higher **pixel resolution** generally lead to higher price categories  
- Features like **Bluetooth**, **WiFi**, and **touch screen** show minimal impact  
- Price categories are evenly balanced (500 samples each)  

**Visualizations included:**
- Histograms  
- Boxplots  
- Correlation heatmap  
- Category vs feature comparisons  

---

### ⚙️ Modeling

**Models Trained:**
- Logistic Regression  
- Support Vector Classifier (SVC)  
- Random Forest Classifier  
- Gradient Boosting Classifier  

### 🏆 Model Comparison

| Model                             | Accuracy |
|----------------------------------|----------|
| Random Forest Classifier         | 0.9500   |
| **Logistic Regression**          | **0.9627** |
| Support Vector Classifier (SVC)  | 0.8800   |
| Gradient Boosting Classifier     | 0.9175   |

✔ **Final Selected Model:** Logistic Regression  
It provided the highest accuracy and excellent class-wise performance.

### ⚠️ Limitations

- The dataset is synthetic and may not represent real-world mobile markets.  
- Only hardware specifications are considered; factors like brand value, build quality, software optimization, and market trends are not included.  
- No hyperparameter tuning was performed for the models, which may limit maximum accuracy.  
- Feature interactions were not deeply explored (e.g., RAM vs processor cores).  
- The model predicts only 4 fixed price categories and cannot output an exact price.  
- External factors like marketing, seasonal demand, and competition are not reflected in the dataset.  

### 🔮 Future Enhancements

- Add real-world datasets containing brand names, OS type, release year, and market value.   
- Deploy the model as a web app using Streamlit or Flask for real-time predictions.      
- Create a mobile-friendly UI where users can input phone specifications and get instant predictions.  
- Expand prediction capability from price *range* to actual *price regression*.  

### 📬 Contact

If you have any questions, suggestions, or feedback regarding this project, feel free to reach out through the channels below:

**👤 Author:** Athuldev K  
**📧 Email:** athuldevkoroth@gmail.com  
**🔗 GitHub:** https://github.com/athuldevkoroth  
**💼 LinkedIn:** https://www.linkedin.com/in/athuldev-k  
  


