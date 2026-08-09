<div align="center">

<h1>🥬 Green Technology Job Market Analysis</h1>

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas"/>
  <img src="https://img.shields.io/badge/Scikit_Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit-Learn"/>
  <img src="https://img.shields.io/badge/Matplotlib-ffffff?style=for-the-badge&logo=pandas&logoColor=black" alt="Matplotlib"/>
</p>

<i>An end-to-end Exploratory Data Analysis (EDA) and Predictive Modeling project mapping the workforce of the sustainable future.</i>

</div>

---

## Project Overview

The transition towards a sustainable economy is rapidly reshaping the global job market. This project performs an end-to-end Exploratory Data Analysis (EDA) and Predictive Modeling on a synthesized dataset (10,000 global job postings for 2025) to map structural hiring trends, technical skill requirements, and compensation frameworks specifically within the Green Technology sector.

## Tools & Technologies Used

* **Programming Language:** Python
* **Data Manipulation & Preprocessing:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn (Random Forest Regressor)
* **Text Processing:** Natural Language Processing (Basic Tokenization)

## Methodology & Execution

1. **Data Preprocessing:** Filtered the dataset to isolate Green Tech roles. Handled missing numerical values via median imputation.
2. **Feature Engineering (NLP):** Processed the multi-valued, comma-separated `skills_required` strings using Pandas dummy encoding to create sparse binary matrices for individual skill analysis.
3. **Exploratory Data Analysis (EDA):** Designed univariate and bivariate visualizations to understand salary distributions, remote work trends, and company size impacts.
4. **Predictive Modeling:** Deployed a Random Forest Regressor to forecast annual salaries based on job titles, locations, and extracted skill vectors.

## Key Insights from EDA
* **Data Generation Anomaly Detected:** The EDA revealed an exact 1:1 frequency match (2,490 counts each) for 'Climate Data Analysis' and 'Energy Modeling'. This statistical impossibility in real-world scenarios further confirms the limitations of the synthetic data generation script, which uniformly assigned both skills to every single Green Tech job posting without variance.

* **Skill Demand:** The analysis revealed that 'Climate Data Analysis' and 'Energy Modeling' are the foundational technical prerequisites for modern sustainability roles.
* **Remote Work:** The data indicated distinct structural variations in compensation bands when comparing strictly on-site roles versus remote flexibilities. 
* **Corporate Scaling:** Salary distributions showed varying medians depending on organizational sizing (Small, Medium, Large enterprises).

<table>
  <tr>
    <td align="center">
      <strong>Salary Distribution in Green Tech</strong><br>
      <img src="https://github.com/user-attachments/assets/a48b4802-410e-4c65-a912-ab2cb71a8145"  alt="Salary Distribution" width="100%">
    </td>
    <td align="center">
      <strong>Remote vs On-site Salary</strong><br>
      <img src="https://github.com/user-attachments/assets/c27568dd-0941-4273-8af7-322886af4f23" alt="Remote vs On-site Salary" width="100%">
    </td>
  </tr>
  <tr>
    <td align="center">
      <strong>Salary vs Company Size</strong><br>
      <img src="https://github.com/user-attachments/assets/96f11e19-4751-4ac6-8188-a04f9c6230ab"  alt="Salary vs Company Size" width="100%">
    </td>
    <td align="center">
      <strong>Most Demanded Skills</strong><br>
      <img src="https://github.com/user-attachments/assets/64b93cb0-8be8-47ea-beee-da777a0bf723"  alt="Most Demanded Skills" width="100%">
    </td>
  </tr>
</table>
---



## Machine Learning Conclusion (The Synthetic Data Anomaly)

> **Analytical Discovery:** The Random Forest Regressor yielded a Root Mean Squared Error (RMSE) of ~$56,487 and a negative R-squared score (-0.0114). 

Rather than indicating a code failure, these metrics successfully proved the **synthetic nature of the dataset**. The model exposed that the target variable (`salary_usd`) was generated using a uniform random distribution without any mathematical correlation to the underlying features (skills, location, or company size). 

This phase successfully demonstrated the critical importance of data validation and highlighted the limitations of utilizing randomly generated dummy data for predictive analytics.
