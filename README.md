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

  

