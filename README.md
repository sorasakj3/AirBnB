# Enhancing Airbnb Hosting Strategies Through Sentiment Analysis

This project applies machine learning and text analytics to analyze Airbnb customer reviews and booking data, with the goal of helping Airbnb hosts optimize their listings, pricing, and guest experience. We built a sentiment analysis model and an interactive application that classifies customer reviews in real time and generates insights to guide business strategies.

---

## Objective

To develop a comprehensive analytics solution that helps Airbnb hosts:

- Understand guest sentiment and satisfaction drivers using NLP
- Segment host types and customer behaviors through clustering and pattern analysis
- Identify key pricing sensitivities and booking trends
- Automate review classification via a machine learning-based sentiment analysis tool
- Provide actionable recommendations based on data-driven insights

---

## Dataset

**Source**: Kaggle – *Airbnb Listings 2016 Dataset*  
**Files Used**:
- `listings.csv`: 3,818 listings with 92 attributes (e.g., price, location, room type)
- `calendar.csv`: 1,048,575 records of nightly availability and pricing
- `reviews.csv`: 84,849 reviews linked to listings and user IDs

---

## Technical Approach and Skills Applied

### Data Engineering & Preprocessing

- Cleaned missing review entries and irrelevant columns
- Tokenized and cleaned textual data for NLP (stop word removal, lemmatization)
- Transformed calendar and pricing data into booking pattern indicators
- Merged multi-source data for unified modeling

### Exploratory Data Analysis (EDA)

- Used **scatter plots**, **histograms**, **correlation heatmaps**, and **word clouds** to visualize trends
- Analyzed host engagement, listing volume, and pricing clusters
- Used `matplotlib`, `seaborn`, `pandas`, and `numpy` for statistical and visual insights

---

## Machine Learning Models

### 1. **Sentiment Classification on Reviews**

- **Text Vectorization**: Applied TF-IDF to convert reviews into numerical features
- **Models Trained**:
  - **XGBoost Classifier**
  - **Random Forest Classifier**
- **Evaluation Metrics**: Accuracy, Precision, Recall, F1-score

> Best results were obtained with **XGBoost**, with high precision on positive reviews and robust classification performance

### 2. **Clustering Hosts for Behavioral Segmentation**

- Applied **K-Means Clustering** on listings based on price, review frequency, and volume of listings
- Identified 3 key host segments:
  - **Individual/Budget Hosts**: High review frequency, lower pricing
  - **Mid-Range Hosts**: Balanced pricing and guest engagement
  - **Commercial/Luxury Hosts**: Low interaction, high pricing

---

## Application: Airbnb Review Sentiment Tool

Developed a **fully functional Python-based review sentiment application** with the following features:

- **User Input Interface**: Accepts bulk customer reviews
- **Model Output**:
  - Sentiment label (Positive/Negative)
  - Confidence score
  - User feedback (Correct, Incorrect, Unsure)
- **Visualization Tools**:
  - Sentiment distribution bar chart
  - Word clouds of positive and negative keywords
- **Supervised Feedback Loop**:
  - Exports corrected classifications for future model tuning
  - Supports iterative model improvement

> Tool was developed in **PyCharm** and is optimized for future integration into host dashboards

---

## Business Insights and Outcomes

### 1. **Guest Engagement Impacts Review Quality**
- Hosts managing fewer listings received more frequent and higher review scores
- Review frequency positively correlates with satisfaction scores

### 2. **Price vs Review Tradeoffs**
- Listings in higher price brackets receive fewer reviews
- Budget and mid-range listings tend to drive guest interaction and visibility

### 3. **Review Text Themes**
- Positive sentiment is driven by location convenience and host responsiveness
- Negative sentiment clusters around cleanliness and host unavailability

### 4. **Data-Backed Recommendations for Hosts**
- **Automate** personalized follow-ups to improve review engagement
- **Highlight cleanliness, location, and host availability** in listings
- **Tailor pricing strategies** based on review behavior by segment
- **Use the review sentiment classifier** as an operational tool to monitor guest feedback at scale

---

## Tools and Technologies

- **Languages**: Python (Pandas, NumPy, Sklearn, XGBoost, NLTK, TextBlob, VADER)
- **Visualization**: Seaborn, Matplotlib, Wordcloud
- **Model Evaluation**: Confusion Matrices, F1 Score, Precision/Recall
- **Development Environment**: Jupyter Notebook, PyCharm

---

## Key Takeaways

- Integrating **machine learning with customer sentiment** provides a scalable method for hosts to improve service quality and decision-making
- NLP techniques like **TF-IDF** and **sentiment scoring** (TextBlob, VADER) are effective for modeling guest satisfaction
- Hosts benefit from **understanding behavioral clusters**, and adjusting pricing, availability, and messaging accordingly
- This project demonstrates the power of combining structured and unstructured data in a real-world hospitality business setting

---

## Authors

**Sorasak Joshi** – Business Analytics, UC Irvine  
**Yiwei Lu, Yi-En Liu, Wan-Lun Tsai, Dennis Wu, Eunhye Kim**  
