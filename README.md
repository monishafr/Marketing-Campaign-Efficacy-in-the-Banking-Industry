# 🏦 Marketing Campaign Efficacy in the Banking Industry

### **Project Overview**
This project analyzes real-world marketing campaign data from a Portuguese bank to identify **key drivers of customer subscription** and optimize future marketing strategies.  
The goal is to determine **which marketing approaches, contact patterns, and customer segments** yield the highest success rates for term deposit subscriptions.

The dataset comes from the [UCI Machine Learning Repository – Bank Marketing Dataset](https://archive.ics.uci.edu/dataset/222/bank+marketing), containing over 41,000 records of customer interactions during multiple marketing campaigns.

---

## 🚀 Objectives
1. Analyze campaign data to uncover factors influencing customer subscriptions.  
2. Identify the **optimal contact frequency, call duration, and communication channel** for maximizing conversions.  
3. Evaluate customer demographics (age, education, job, marital status) to determine **high-potential target segments**.  
4. Derive actionable recommendations to improve future campaign performance using **data-driven insights**.

---

## 🧩 Dataset Information
- **Name:** `bank-additional-full.csv`  
- **Records:** 41,188  
- **Features:** 20 independent variables + 1 target (`y`)  
- **Target Variable:**  
  - `y = yes` → Customer subscribed to term deposit  
  - `y = no` → Customer did not subscribe  

### **Feature Categories**
- **Demographic Attributes:** age, job, marital, education  
- **Financial Attributes:** housing loan, personal loan, default status  
- **Campaign Interaction Attributes:** contact type, month, day of week, duration, campaign count, previous outcomes  
- **Economic Indicators:** employment variation rate, consumer price/confidence index, Euribor3m rate, number of employees  

---

## 🧠 Methodology

### 1. **Data Exploration and Cleaning**
- Checked dataset shape and column types → *(41,188 rows × 21 columns)*  
- Verified no missing values and examined categorical value distributions.  
- Identified and retained “unknown” entries, since they were minimal and removing them would have led to loss of valuable records.

### 2. **Feature Importance Analysis**
- Used a **Random Forest Classifier** to estimate preliminary feature importance.  
- Top predictors influencing customer subscription:
  - **Duration** of the call  
  - **Previous campaign outcomes**  
  - **Number of past contacts (previous)**  

These features were then explored in depth through visualizations and statistical analysis.

### 3. **Exploratory Data Analysis (EDA)**
Performed segmentation and visualization to understand patterns in subscription behavior:

- **Age Group Analysis:**  
  Older age groups (66–100 years) showed the **highest subscription rate**, possibly due to stronger savings behavior or long-term financial planning.

- **Marital Status:**  
  Married customers subscribed more frequently, reflecting financial security and long-term planning tendencies.

- **Education Level:**  
  Campaign success improved as education level increased.  
  However, a small “illiterate” group had an unusually high success rate due to limited data points (data imbalance).

- **Job Profile:**  
  Retired individuals and students had the **highest conversion rates**, suggesting personalized offers (student loans, retirement savings) are key to better engagement.

- **Loan Status:**  
  Customers **without personal loans** were significantly more likely to subscribe to new deposit products.

- **Contact Type:**  
  **Cellular contacts outperformed telephone calls** in both reach and success rate — indicating that modern communication channels are more effective.

- **Call Duration:**  
  The most successful calls lasted **0–20 minutes**, proving that short, focused conversations are more effective than long or drawn-out interactions.

- **Number of Contacts:**  
  Customers contacted **0–5 times** showed the **highest conversion rates**, while repeated contact attempts led to declining success — showing the need to limit outreach frequency.

- **Previous Campaign Outcome:**  
  Even customers who had a **failed previous campaign** were more likely to subscribe than those who were never contacted before — demonstrating the long-term brand impact of consistent marketing efforts.

---

## 📊 Key Insights and Findings

| Focus Area | Key Finding | Business Interpretation |
|-------------|--------------|--------------------------|
| **Call Duration** | 0–20 minutes yields the best results | Keep interactions concise and impactful |
| **Contact Frequency** | More than 5 contacts reduce success | Avoid over-contacting customers |
| **Education Level** | Higher education → higher subscriptions | Use financial education-oriented messaging |
| **Loan Status** | Customers without loans convert more | Target financially stable segments |
| **Job Profile** | Retired and students respond best | Personalize offers to their life stage |
| **Previous Campaigns** | Even failed past contacts improve conversion | Maintain brand awareness through follow-up |
| **Communication Type** | Cellular > Telephone | Prioritize mobile-first communication strategies |

---

## 🧮 Modeling Approach
To understand feature influence:
- Performed **One-Hot Encoding** on categorical data.  
- Used **Random Forest Classifier** and **Logistic Regression** models to test feature importance and relationships.  
- Achieved **AUC score of 0.798**, showing strong predictive performance.  
- Validated findings with cross-validation and correlation checks.

---

## 💡 Strategic Recommendations
1. **Focus on concise, well-structured calls** (under 20 minutes).  
2. **Limit campaign frequency** to a maximum of bi-weekly contact per client.  
3. **Prioritize customers without existing personal loans** or financial obligations.  
4. **Target educated, retired, or student segments** with personalized offers.  
5. **Continue engaging customers from past campaigns**, even if previous attempts failed.  
6. **Adopt mobile-first outreach** for higher efficiency and lower cost per conversion.  

---

## 🔍 Tools and Libraries Used
- **Python**  
- **Pandas, NumPy** – Data manipulation  
- **Matplotlib, Seaborn, Bokeh** – Visualization  
- **Scikit-learn** – Modeling and evaluation  
- **Google Colab** – Development environment  

---

## 📈 Business Impact
This analysis equips financial institutions with data-backed insights to **refine their marketing strategy**, **reduce campaign waste**, and **increase ROI**.  
By optimizing contact duration, communication channels, and target segmentation, banks can achieve **higher customer conversion rates** with fewer resources and greater personalization.

---

## 🧾 Conclusion
The project demonstrates how structured marketing data can be transformed into actionable intelligence.  
By analyzing behavioral, demographic, and communication features, the study uncovered the strongest drivers of customer engagement and subscription success.  
These insights enable financial institutions to shift from intuition-based marketing to **data-driven decision-making**, ensuring efficient outreach and improved customer satisfaction.

---

## 📚 Future Scope
- Integrate **predictive modeling** to forecast campaign success for upcoming customer lists.  
- Expand analysis across **multiple banks or regions** to generalize insights.  
- Incorporate **real-time data pipelines** for adaptive marketing strategy updates.  
- Explore **NLP-based sentiment analysis** on call transcripts or messages for deeper personalization.  

---

## 🧠 Author
**Monisha Patro**  
M.S. in Data Science – Indiana University Bloomington  
📧 [GitHub Portfolio](https://github.com/monishafr) | [LinkedIn](https://www.linkedin.com/in/monisha-patro/)
