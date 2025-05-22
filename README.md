# HR-Analytics-Dashboard

## 🔍 Problem Statement 

Employee attrition poses a significant challenge to organizational stability and productivity. The Human Resources department seeks a deeper understanding of workforce dynamics — including employee demographics, departmental distributions, and reasons for termination — in order to identify trends that contribute to high attrition rates.

This dashboard addresses the need to:

- 📊 Monitor key HR metrics such as total employees, average salary, and attrition rate.
- 🧑‍🤝‍🧑 Analyze employee distribution by gender, age, race, citizenship, department, and marital status.
- 🏢 Identify departments and demographics with higher attrition rates.
- ❗ Examine reasons behind employee terminations for better decision-making.
- 📝 Provide detailed employee-level insights for targeted HR interventions.


---


## 🛠️ Steps Taken to Build the HR Analytics Dashboard

1. **Background Design**
   - Designed a custom **dashboard background using PowerPoint** to enhance visual appeal and layout consistency.
   - Imported the background into Power BI for use on all report pages.

2. **Data Loading and Cleaning**
   - Uploaded the HR dataset into **Power BI Power Query**.
   - Reviewed each table individually to ensure:
     - Column headers were correctly placed.
     - Data types were properly assigned (dates, numbers, text).
     - Understood the meaning and context of each column.

3. **Data Modelling**
   - Performed **data modeling** to define relationships between tables.
   - Created a **Date Table** using DAX to enable time-based filtering and slicing.
   - Established **many-to-one relationships**:
     - Between `HRdataset[DateofHire]` and `Date[Date]`
     - Between `HRdataset[DateofTermination]` and `Date[Date]`
   - Managed inactive relationships using `USERELATIONSHIP()` in relevant DAX measures for terminated employees or attrition-specific KPIs.

## 🧩 Data Modelling

<img src="Data%20Modelling.png" width="800">

4. **DAX Measures and Calculations**
   - Created custom **DAX measures** to calculate KPIs:
     - `Total Employees`
     - `Active Employees`
     - `Terminated Employees`
     - `Attrition Rate`
     - `Average Salary`
   - Applied DAX functions like:
     - `CALCULATE()`, `FILTER()`, `DIVIDE()`, `AVERAGE()`, `USERELATIONSHIP()`, `DISTINCTCOUNT()`.

5. **Data Visualization**
   - Designed an interactive and user-friendly dashboard using:
     - **KPI cards** for quick metric highlights.
     - **Donut and bar charts** to show distribution by gender, department, race, marital status, and more.
     - **Line charts** to track attrition trends by department.
     - **Tables with conditional formatting** to display employee-level details (e.g., EmpID, Age Band, Citizenship).
     - **Slicers and filters** for Year, Department, and Position for better interactivity.

6. **Final Touches**
   - Applied consistent formatting, custom themes, and color schemes.
   - Added **navigation buttons** (Overview, Attrition, Employee Details) for smooth report interaction.


---


## 📊 Dashboard Insights

### 🟦 Overview Page 1:
- **Total Employees**: 311
- **Average Salary**: $69.02K
- **Attrition Rate**: 50.24% ⚠️ 

#### 📌 Employee Demographics:
- **Sex**: Slightly more males (43.41%) than females (56.59%)
- **Citizenship**: Overwhelmingly U.S. Citizens (94.86%)
- **Marital Status**:
  - Single: 44.0%
  - Married: 39.87%
  - Divorced: 9.65%
- **Department**:
  - Production is the largest department with 209 employees
  - IT/IS follows with 50 employees
- **Race**: White (187) is the dominant race category
- **Age Band**: 40–49 is the largest group with 128 employees


### 🟥 Attrition Page 2:
- **Terminated Employees**: 104
- **Active Employees**: 207
- **Attrition Rate**: 50.24% (consistent with the overview page)
- **Terminated Employees By Sex**: 
  - FeMales: 57.69%
  - males: 42.31%
- **By Department**:
  - Production has the highest attrition rate: 65.87%
  - Software Engineering follows with 57.14%
- **By Termination Reason**:
  - Top reason: "Another Position" (20 terminations)
  - Second: "Unhappy" (14 terminations)


### 🟩 Employee Details Page 3:
- Provides a detailed view of individual employees:
  - Employee ID, Name, Gender, Date of Birth, Citizenship, Department, Date of Hire, Age Band, Employment Status
- Useful for deep-dive analysis and identifying patterns at an individual level
- Supports targeted HR actions and investigation into specific attrition cases

  
---


## ✅ Suggestions and Recommendations

1. **Keep Employee Engagement Top of Mind**  
   Implement regular feedback sessions, recognition programs, select the right managers, and conduct team-building activities to foster a positive work environment and increase employee satisfaction.

2. **Career Development Opportunities**  
   Provide clear paths for career advancement, training programs, and mentorship opportunities to help employees grow professionally and feel invested in their future with the organization.

3. **Discuss Compensation and Benefits**  
   Offer competitive compensation packages, performance bonuses, and additional perks to attract and retain top talent in the organization.

4. **Evaluate Feedback from Employee Exit Interviews**  
   Conduct exit interviews to gather feedback from departing employees and use this information to identify trends, patterns, and areas for improvement. Before someone leaves the organization, ask:
   
   - **(i)** What is the primary reason the employee is leaving?  
   - **(ii)** What does the company do well?  
   - **(iii)** What could the company improve to increase employee satisfaction?


---
  

## 📊 Dashboard Preview

<img src="Overview%20Page%201.png" width="800">

<img src="Attrition%20Page%202.png" width="800">

<img src="Employee%20Details%20Page%203.png" width="800">

---

