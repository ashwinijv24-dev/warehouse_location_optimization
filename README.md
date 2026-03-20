# 📦 Warehouse Location Optimization using Data Analysis

## 📌 Objective
The objective of this project is to determine the optimal warehouse location in the Netherlands that minimizes the overall delivery distance for customers, based on their locations and package volumes.

---

## 🧠 Problem Statement
We are given data for 10 customers located in different regions of the Netherlands, each with a varying number of packages. The goal is to identify the best warehouse location (4-digit postal code) such that the total delivery distance is minimized.

---

## 🚀 Approach

1. **Data Understanding**
   - Analyzed customer data including postal codes and number of packages.
   - Identified that both **location** and **package volume** influence the solution.

2. **Data Enrichment**
   - Postal codes do not provide direct distance information.
   - Mapped postal codes to their corresponding **latitude and longitude** using a geolocation dataset.

3. **Weighted Centroid Calculation**
   - Applied a weighted centroid approach where:
     - Each location contributes proportionally based on the number of packages.
   - Formula used:
     - Weighted Latitude = Σ(latitude × packages) / Σ(packages)
     - Weighted Longitude = Σ(longitude × packages) / Σ(packages)

4. **Distance Calculation**
   - Calculated the distance between the weighted centroid and each customer location using the Euclidean distance formula.

5. **Optimal Location Selection**
   - Selected the postal code with the **minimum distance** from the centroid as the optimal warehouse location.

---

## 🧮 Solution

- The weighted centroid was computed based on customer distribution and package volume.
- Distances were calculated for all locations.
- The location with the **minimum distance** was chosen.

### ✅ Final Result:
**Optimal Warehouse Location: Postal Code 9448 (Dalfsen)**

---

## 🛠️ Tools & Technologies Used

- **SQL (MySQL)**  
  - Data joining  
  - Weighted centroid calculation  
  - Distance computation using mathematical functions  
  - CTE (Common Table Expressions)

- **Microsoft Excel**  
  - Data preparation  
  - Validation of calculations  
  - Visualization of results  

- **Python (Pandas & SQLAlchemy)** *(Optional Enhancement)*  
  - Data loading into SQL  
  - Handling file import limitations  

---

## 📂 Project Structure

```
warehouse-location-optimization/
│
├── data/
│ ├── customers.xlsx
│ └── postal_coordinates.xlsx
│
├── sql/
│ └── casestudy(warehouse_optimization).sql
│
├── excel/
│ └── casestudy(warehouse_optimization).xlsx
│
├── docs/
│ └── detailoriented_casestudy.pdf
│
└── README.md

```

## 💡 Key Learnings

- Importance of **data enrichment** for geospatial problems  
- Application of **weighted centroid for optimization**  
- Translating business problems into **analytical solutions**  
- Writing efficient and structured SQL queries  

---

## 🚀 Future Enhancements

- Extend solution for **multiple warehouses using clustering (K-Means)**  
- Use **Haversine formula** for more accurate distance calculation  
- Visualize locations using **maps (Power BI / Python)**  

---

## 🤝 Acknowledgment

This project was completed as part of a case study for a SQL and Power BI Developer role. It provided valuable insights into real-world problem-solving and analytical thinking.


