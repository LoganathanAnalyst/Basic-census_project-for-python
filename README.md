# 🇮🇳 India Census 2011 – Python Data Analysis Project  
### A Beginner-Friendly Real-Time Data Analysis Project using Pandas  

---

## 📌 Overview  
This is a **basic, beginner-friendly Python project** built using the **India Census 2011 Dataset**, downloaded from Kaggle.  
The dataset contains complete demographic and socio-economic information of **all districts of India**, including population, literacy, religion, workers, education levels, and age groups.

Using **Pandas DataFrames**, we perform multiple real-time data analysis tasks that help learners practice Python, understand data handling, and work with large datasets effectively.

---

## 📂 Dataset Description  
The dataset represents district-wise Census 2011 information with **25 columns**, including:

- State & District Details  
- Population (Total, Male, Female)  
- Literacy  
- Workers (Male/Female)  
- Religion Counts  
- Cultivators & Agricultural Workers  
- Education Levels (Secondary, Higher, Graduate)  
- Age Groups (0–29, 30–49, 50+)

Source: **Kaggle – India Census 2011 Dataset (CSV file)**  
Total Rows: **640 districts**

---

## 🛠️ Technologies Used  
- **Python**
- **Pandas**
- **NumPy**
- **Jupyter Notebook**

---

## 📥 Importing Required Libraries  
```python
import pandas as pd
```

---

## 📘 Reading the Dataset  
```python
data = pd.read_csv("census.csv")
data.head(5)
```

---

## 🧹 Basic Data Styling  
### 1️⃣ Hide Index of DataFrame  
```python
data.style.hide(axis="index")
```

### 2️⃣ Add Caption / Title to DataFrame  
```python
data.style.set_caption("India Census 2011 Dataset")
```

---

## 🔍 Key Analysis Performed  

### **3️⃣ State-wise Religious Population (Sum of all Religions)**  
```python
data.groupby('State_name')[
    ['Hindus','Muslims','Christians','Sikhs','Buddhists','Jains']
].sum().sort_values(by='Hindus')
```

---

### **4️⃣ Number of Male Workers in Maharashtra**  
```python
data[data.State_name == 'MAHARASHTRA']['Male_Workers'].sum()
```

Output:  
`32616875`

---

### **5️⃣ Setting a Column as Index**  
```python
data.set_index('District_code')
```

---

## 📈 What You Will Learn  
✔ Reading and analyzing real government data  
✔ Using Pandas for grouping, filtering, and summarization  
✔ Handling large datasets (640 rows × 25 columns)  
✔ Performing demographic & socio-economic analysis  
✔ Writing clean and organized Python code  
✔ Building beginner-friendly data analysis projects  

---

## 📁 Project Structure  
```
📦 India-Census-2011-Analysis
 ┣ 📜 census.csv
 ┣ 📜 India_Census_Analysis.ipynb
 ┗ 📜 README.md
```

---

## 🚀 Future Enhancements  
- Add visualizations using Matplotlib & Seaborn  
- Create state-level dashboards  
- Build an interactive Power BI dashboard  
- Add machine learning (population prediction)

---

## 👨‍💻 Author  
**Loganathan**  


---

⭐ *If you found this project helpful, please star the repository!*

