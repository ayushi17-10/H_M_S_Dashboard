# H_M_S_Dashboard
# 🏥 Hospital Management System Dashboard - Power BI

A comprehensive Power BI dashboard that provides **operational insights** into key hospital functions including doctors, patients, rooms, billing, attendance, lab tests, payroll, branches, medicines, tasks, and departments.

---

## 📊 Dashboard Highlights

### 🔹 Operational Modules Included:
- 👨‍⚕️ **Doctors & Patients**
- 🏨 **Room Occupancy & Assignment**
- 🧾 **Billing: Paid vs Due Analysis**
- 📅 **Attendance: Doctor and Staff Trends**
- 🧪 **Lab Tests: Status & Revenue**
- 🏥 **Branch Management**
- 💼 **Payroll Overview**
- 💊 **Medicine Stock & Expiry Monitoring**
- ✅ **Task and To-Do Management**
- 🏖️ **Leave Reports**
- 🏢 **Departmental Performance**

---

## 📌 Key Visuals & KPIs

| 📁 Module     | 🔍 Visuals/Insights                                      |
|--------------|-----------------------------------------------------------|
| Doctors       | Patients per Doctor (Bar), Attendance % (Gauge)         |
| Billing       | Paid vs Due (Stacked Column), Top 5 Bills               |
| Lab Tests     | Test Status Funnel, Revenue over Time (Line Chart)      |
| Staff         | Leave Types (Donut), Payroll by Department              |
| Medicines     | Expiring Soon (Table), Stock by Category (Bar)          |
| Tasks         | Task Completion % (Gauge), Tasks by Priority (Column)   |
| Departments   | Staff per Department, Active/Inactive Count             |

---

## 🧮 DAX Measures Used

```DAX
Total Net Pay = SUM(Payroll[NetPay])
Expiring % = 
DIVIDE(COUNTROWS(FILTER(MedicineList, MedicineList[ExpiryDate] <= TODAY() + 30)), COUNTROWS(MedicineList)) * 100

Birth % = 
DIVIDE(COUNT(BirthRecord[PatientID]), COUNT(BirthRecord[PatientID]) + COUNT(DeathRecord[PatientID])) * 100

🛠️ Tools Used
Power BI Desktop

DAX (Data Analysis Expressions)

Power Query (ETL)

Excel/CSV for base data sources

🚀 How to Use
Clone/download this repo

Open the .pbix file in Power BI Desktop

Connect to your local or sample dataset if needed

Customize visuals or extend modules as required

🧑‍💻 Author
Ayushi Singh
