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
- **Attrition Rate**: 50.24% ⚠️ *(This is a very high number and a key area to highlight)*

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
  

