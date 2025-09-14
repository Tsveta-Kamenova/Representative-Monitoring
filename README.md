# Representative Monitoring Dashboard

We need to build a report to monitor our representative’s activity.  

Data:

1. Customers  
2. Territory  
3. Interactions  
4. Plan Data  

---

### What we need to analyze in our report is the following:

1. **Total interactions per month for each territory**  
2. **Total plan calls per month for each territory**  
3. **Coverage** – How many customers that are on our plan were contacted per territory.  
   - What is the percentage compared to the total planned customers?  
4. **Compliance** – How many customers that are on our plan were contacted at least the planned number of interactions.  
   - What is the percentage compared to the total targeted customers?  

---

### Example

| Territory | Plan | Interactions | Customer             |
|-----------|------|--------------|----------------------|
| ITSF1101  | 5    | 3            | Gatta, Giulia        |
| ITSF1101  | 5    | 4            | Cotti Piccinelli, Stefano |
| ITSF1101  | 5    | 5            | Galiano, Paolo       |
| ITSF1101  | 5    | 0            | Mordente, Ines       |

**Coverage**: 4 in plan, 3 seen → 3 / 4 = 75%  
**Compliance**: 4 in plan, 1 achieved → 1 / 4 = 25%  

---


## ✅ Solution

### 1. Power BI Dashboard

The Power BI report includes:  
- KPI cards for **Total Planned Calls, Total Interactions, Coverage %, Compliance %**  
- Territory-level summary table  
- Top 3 Territories by Coverage and Compliance  
- Monthly trend analysis (planned vs. actual vs. compliance/coverage)  
- Slicers for **Month** and **Territory Code**  

📷 Preview:  
<img width="963" height="544" alt="image" src="https://github.com/user-attachments/assets/7376f84b-d5b7-4aa9-909f-28a09824059b" />


---

### 2. Excel Power Pivot

A Power Pivot model was also created to reproduce the same calculations in Excel.  
- Measures for interactions, planned calls, coverage, and compliance  
- Pivot tables with **territory as rows** and **months as columns**

## Insights

- Planned calls significantly exceed actual interactions → low compliance overall  
- Coverage is higher than compliance, meaning most customers are contacted but not always at the planned frequency  
- Strong variation across territories → top/bottom performers are highlighted  
