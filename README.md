# HCPCS_Cd  
Analyzing HCPCS codes to find gaps between hospital charges and what Medicare allows.

## 📂 Project Overview  
This project looks at how much hospitals are charging for different services (HCPCS codes) and how that compares with what Medicare allows. The goal is to find if there is any big gap between them.

## 📌 Data Source  
The data is taken from [data.cms.gov](https://data.cms.gov/), and the original dataset had over **1 million rows**.  
I used **SQL Server** and **SSIS** to upload the data, and then selected **100,000 rows** to analyze in Python.

## 🧰 Tools Used  
- Python (Pandas, NumPy)  
- SQL Server  
- Matplotlib & Seaborn  
- Plotly (for better visuals)  
- KMeans Clustering (from sklearn)

## 📊 Project Steps  

### 1. Understanding the Dataset  
Looked at the columns, values, and checked data types.

### 2. Remove Irrelevant Columns and Renaming Rest for Better Understanding  
Kept only the useful columns and gave them simpler names.

### 3. Changing the Data Types to Relevant One  
Fixed the datatypes like float, int, and string.

### 4. Checking the Value Counts and Describing the Data  
Used `.describe()` and `value_counts()` to understand ranges and frequent values.

### 5. Top 10 Code by Services  
Grouped by HCPCS code to find the most used codes.

### 6. Top HCPCS Code Compared to Hospital Charges, Medicare Allowed, and What Medicare Paid  
Made a side-by-side bar chart for better comparison.

### 7. Gap, Gap Percent Between Submitted Charges and Medicare Allowed  
Calculated how much higher hospitals are charging than what Medicare allows.

### 8. Recalculating the Gap and Gap Percentage (After Removing Outliers)  
Filtered out very high values to get a better picture.

### 9. Checking the Highest Gap Percentage Code  
Found the code where hospitals are charging the most over Medicare rates.

### 10. Checking Which Provider Type Charges the Most for the Highest Gap Percentage HCPCS Code  
Filtered on the provider type for deeper insight.

### 11. Checking Rest of the Data for Provider Type Who Charges the Most for Other HCPCS Codes  
Looked at whether this provider type is overcharging in other codes too.

### 12. Creating Cluster of Provider Type Using K-Means Clustering  
Grouped provider types based on their charging pattern.

### 13. Visualize the Scatter Plot  
Used Plotly to make it more interactive and readable.

## 📈 Key Insight  
- Some provider types are charging **much more** than what Medicare allows.  
- One provider type charged **300% or more** in 57 different codes.  
- One code had a gap percent of **399,999%**, which looks like an outlier.  

## 💡 What Can Be Improved  
- This project doesn't have a stakeholder, so everything is based on my own ideas.  
- With a domain expert or doctor, this can be more accurate.  
- Future work can include **time trend**, **geographical mapping**,


## 📬 Final Note  
This is a portfolio project. I used real government data, applied what I know, and tried to ask meaningful questions.  
If you're looking for someone who can clean data, ask the right questions, and turn them into insights — I’m available and ready to grow with your team.


📌 **Note:** Plotly charts are interactive and may not appear properly on GitHub.  
👉 **[Click here to view the full notebook with interactive visuals.]([https://nbviewer.org/github/your-username/your-repo-name/blob/main/your-notebook.ipynb](https://nbviewer.org/github/vikramnigam/HCPCS_Cd/blob/a80c93ea7f0bdfcb1929d07e32c9e4663d115350/HCPCS_Cd%20%26%20Bills.ipynb))**


