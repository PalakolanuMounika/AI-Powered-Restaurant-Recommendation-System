
# Restaurant Order Prediction

## 📌 Project Overview
This project predicts **which restaurant (vendor) a customer is most likely to order from** using historical order data, customer details, and vendor information.  
It works as a **personalized recommendation system** that estimates the probability of an order between a customer and a vendor.

## 🎯 Goal
The main goal is to:
1. Learn from historical order patterns to understand customer preferences.
2. Predict the most likely vendor for each customer in the test set.
3. Output the **top recommended vendor** for each customer in the required submission format:
   ```
   CID X LOC_NUM X VENDOR
   ```

## 📂 Dataset
The project uses:
- **train_customers.csv** – Customer details
- **train_locations.csv** – Customer location data
- **orders.csv** – Historical orders
- **vendors.csv** – Vendor details
- **test_customers.csv** – Test set customer details
- **test_locations.csv** – Test set locations

## 🔍 Features Used
Some key features used for prediction:
- **Customer Age**
- **Account Age in Days**
- **Vendor Popularity** (number of past orders)
- **Day of Week & Hour of Order**
- **Order Amount & Item Count**
- **Preparation Time**
- *(Planned)* Distance between customer and vendor

## 🛠️ Methodology
1. **Data Preprocessing**
   - Merge customer, vendor, and order data
   - Handle missing values
   - Encode categorical variables

2. **Feature Engineering**
   - Create numerical and categorical features
   - Calculate popularity metrics
   - *(Planned)* Calculate geodesic distance between customer and vendor

3. **Model Training**
   - Train a **LightGBM Classifier** on positive and negative samples
   - Use **AUC** as the evaluation metric

4. **Prediction & Recommendation**
   - Generate all possible customer–vendor pairs for the test set
   - Predict probability of ordering for each pair
   - Select the **highest probability vendor** per customer

## 🚀 Tech Stack
- Python
- Pandas, NumPy
- scikit-learn
- LightGBM
- Geopy (for distance calculation)

## 📜 Output
- A `submission.csv` file containing the top vendor recommendation for each customer.

## 📈 Use Cases
- Personalized restaurant recommendations
- Targeted promotions and marketing
- Delivery resource optimization

---
**Author:** Palakolanu Mounika  
**Year:** 2025
