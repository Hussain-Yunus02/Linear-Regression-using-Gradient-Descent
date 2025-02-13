
# **Linear Regression from Scratch using Gradient Descent**  

## **Overview**  
This project implements **Linear Regression** from scratch using **Gradient Descent** to predict **student final exam marks** based on midterm marks. By manually deriving and coding the optimization process, we gain a deeper understanding of:
- **Feature Standardization**
- **Cost Function Optimization**
- **Gradient Computation**
- **Learning Rate Impact**
- **Error Reduction over Iterations**

This hands-on approach builds intuition around **machine learning optimization techniques** and serves as a foundation for more advanced predictive modeling.

---

## **Dataset**  
We use a **Student Marks Dataset** consisting of:
- **Midterm Marks (Feature X)**
- **Final Marks (Target Y)**  
Our goal is to train a **linear regression model** that predicts **final marks given midterm marks**.

🔗 **Dataset URL:** [Student Marks Dataset](https://raw.githubusercontent.com/yoga-suhas-km/Intelligent_systems/main/marks_dataset.csv)

---

## **Mathematical Foundation**  
A linear regression model is represented by the equation:  

\[
y = mx + b
\]

Where:  
- \( m \) is the **slope (weight/parameter)**  
- \( b \) is the **y-intercept (bias)**  
- \( x \) is the **input feature (midterm marks)**  
- \( y \) is the **predicted output (final marks)**  

### **Cost Function (Mean Squared Error - MSE)**  
To measure how well the regression line fits the data, we use the **Mean Squared Error (MSE)**:

\[
E(m, b) = \frac{1}{N} \sum_{i=1}^{N} (y_i - (m x_i + b))^2
\]

Our objective is to find **optimal values of m and b** that minimize this error.

### **Gradient Descent Algorithm**  
To optimize \( m \) and \( b \), we compute their **partial derivatives** and iteratively update them:

\[
\frac{\partial E}{\partial m} = -\frac{2}{N} \sum_{i=1}^{N} x_i (y_i - (m x_i + b))
\]

\[
\frac{\partial E}{\partial b} = -\frac{2}{N} \sum_{i=1}^{N} (y_i - (m x_i + b))
\]

We update the values using a **learning rate (α)**:

\[
m_{new} = m_{old} - \alpha \frac{\partial E}{\partial m}
\]

\[
b_{new} = b_{old} - \alpha \frac{\partial E}{\partial b}
\]

---
## **Implementation Steps**
### **1. Data Preparation & Exploratory Data Analysis (EDA)**
- Load the dataset
- Compute **mean (μ) and standard deviation (σ)**
- Visualize the **data distribution**

### **2. Feature Standardization**
Since gradient descent is sensitive to scale differences, we standardize the data:

\[
x' = \frac{x - \mu}{\sigma}
\]

### **3. Implement Gradient Descent**
- Initialize parameters:
  - **m = -0.5, b = 0, learning rate (α) = 0.0001**
- Perform **100 iterations** and visualize:
  - Initial regression line
  - Updated regression line after optimization
- Extend to **2000 iterations** to observe convergence

### **4. Plotting Results**
- **Data Points & Regression Line**
- **Error Reduction over Iterations** (Loss function visualization)
- **Comparison: Standardized vs. Non-Standardized Features**

### **5. Verification with scikit-learn**
- Compare our custom implementation against **scikit-learn's `LinearRegression` API**.

---
## **Results & Analysis**
📌 **Expected Observations:**
- The **error decreases** as iterations increase, proving that gradient descent is optimizing the parameters.
- A **too-large learning rate (α)** might overshoot the minimum, while a **too-small α** leads to slow convergence.
- **Standardization significantly improves convergence speed**.

📊 **Generated Plots:**
1. **Scatter Plot** of Midterm vs. Final Marks
2. **Initial Regression Line** (before optimization)
3. **Final Regression Line** (after optimization)
4. **Error vs. Iterations Graph** (for 100 and 2000 iterations)

---
## **Key Learnings & Takeaways**
✅ Understanding **how regression models minimize errors**  
✅ Practical implementation of **Gradient Descent**  
✅ Importance of **Feature Scaling** in optimization  
✅ Visualizing **convergence of parameters over iterations**  

---
## **Further Enhancements**
🔹 **Extend to Multiple Linear Regression** (multiple features)  
🔹 **Implement Stochastic Gradient Descent (SGD)**  
🔹 **Use Adaptive Learning Rates (Adam, RMSprop)**  
🔹 **Compare with advanced optimizers (L-BFGS, Newton’s Method)**  

---
## **References**
- 🔗 [Gradient Descent Explained](https://en.wikipedia.org/wiki/Gradient_descent)  
- 🔗 [Scikit-learn Linear Regression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html)  

---
## **Author**
👨‍💻 **Husain Yunus Maudiwala**  


---
