# 📘 ABAP Company Master – Data Dictionary Project  

## 🔹 Short Description  
SAP ABAP Data Dictionary project demonstrating **Domains, Data Elements, Transparent Table, Search Help, and Lock Object** for a **Company Master database**.  

---

## 📂 Project Overview  
This project showcases the **ABAP Data Dictionary lifecycle** by creating a **Company Master** table and related dictionary objects.  
It covers:  
- ✅ Domains  
- ✅ Data Elements  
- ✅ Transparent Table  
- ✅ Search Help  
- ✅ Lock Object  
- ✅ Table Maintenance (SM30)  

---

## 📑 Data Dictionary Objects  

### 🔹 Domains  
- `ZCOM_ID_DOM` → NUMC(5) → Company ID  
- `ZCOM_NAME_DOM` → CHAR(40) → Company Name  
- `ZCITY_DOM` → CHAR(20) → City  
- `ZSTATE_DOM` → CHAR(20) → State  
- `ZCOUNTRY_DOM` → CHAR(20) → Country  
- `ZINDUSTRY_DOM` → CHAR(30) → Industry  
- `ZCONTACT_DOM` → NUMC(10) → Contact Number  
- `ZEMAIL_DOM` → CHAR(50) → Email Address  

### 🔹 Data Elements  
- `ZCOM_ID_DE` → Refers `ZCOM_ID_DOM`  
- `ZCOM_NAME_DE` → Refers `ZCOM_NAME_DOM`  
- `ZCITY_DE` → Refers `ZCITY_DOM`  
- `ZSTATE_DE` → Refers `ZSTATE_DOM`  
- `ZCOUNTRY_DE` → Refers `ZCOUNTRY_DOM`  
- `ZINDUSTRY_DE` → Refers `ZINDUSTRY_DOM`  
- `ZCONTACT_DE` → Refers `ZCONTACT_DOM`  
- `ZEMAIL_DE` → Refers `ZEMAIL_DOM`  

### 🔹 Transparent Table  
`ZCOMPANY_MASTER`  
- COMPANY_ID (Key)  
- COMPANY_NAME  
- CITY  
- STATE  
- COUNTRY  
- INDUSTRY  
- CONTACT_NO  
- EMAIL  

### 🔹 Search Help  
- `ZCOMPANY_SH` → enables search on **Company ID, Company Name, City**  

### 🔹 Lock Object  
- `EZCOMPANY_LOCK` → prevents parallel update on same **COMPANY_ID**  
---

## 📊 Sample Data  

| COMPANY_ID | COMPANY_NAME        | CITY      | STATE       | COUNTRY | INDUSTRY        | CONTACT_NO | EMAIL                  |
|------------|---------------------|-----------|-------------|---------|-----------------|------------|------------------------|
| 00001      | Alpha Tech Pvt Ltd  | Mumbai    | Maharashtra | India   | IT Services     | 9876543210 | contact@alphatech.com  |
| 00002      | Beta Solutions Ltd  | Delhi     | Delhi       | India   | Consulting      | 9812345678 | info@betasolutions.com |
| 00003      | Gamma Industries    | Bangalore | Karnataka   | India   | Manufacturing   | 9823456789 | sales@gammaind.com     |
| 00004      | Delta Foods Pvt Ltd | Pune      | Maharashtra | India   | FMCG            | 9845678901 | hello@deltafoods.com   |
| 00005      | Epsilon Textiles    | Surat     | Gujarat     | India   | Textile         | 9876501234 | contact@epsilontex.com |

*(Full dataset contains 15 companies — see `sample_data/company_master.csv`)*  

---

## ▶️ Run Instructions  

To run and test this project inside **SAP ABAP System**:  

1. **Create Domains**  
   - Go to `SE11` → Domain → Create  
   - Example: `ZCOM_ID_DOM`, `ZCOM_NAME_DOM`, `ZCITY_DOM`  

2. **Create Data Elements**  
   - Go to `SE11` → Data Element → Create  
   - Example: `ZCOM_ID_DE`, `ZCOM_NAME_DE`, etc.  

3. **Create Transparent Table**  
   - Go to `SE11` → Table → `ZCOMPANY_MASTER`  
   - Assign Data Elements to fields.  

4. **Create Search Help**  
   - Go to `SE11` → Search Help → `ZCOMPANY_SH`  
   - Attach it to `COMPANY_ID`.  

5. **Create Lock Object**  
   - Go to `SE11` → Lock Object → `EZCOMPANY_LOCK`.  

6. **Generate Table Maintenance**  
   - Use `SE11 → Utilities → Table Maintenance Generator`.  
   - Table editable via `SM30`.  

---

## 📊 Sample Data (15 Companies)  

| COMPANY_ID | COMPANY_NAME        | CITY      | STATE       | COUNTRY | INDUSTRY        | CONTACT_NO | EMAIL                        |
|------------|--------------------|-----------|-------------|---------|-----------------|------------|------------------------------|
| 00001      | Alpha Tech Pvt Ltd | Mumbai    | Maharashtra | India   | IT Services     | 9876543210 | contact@alphatech.com        |
| 00002      | Beta Solutions Ltd | Delhi     | Delhi       | India   | Consulting      | 9812345678 | info@betasolutions.com       |
| 00003      | Gamma Industries   | Bangalore | Karnataka   | India   | Manufacturing   | 9823456789 | sales@gammaind.com           |
| 00004      | Delta Foods Pvt Ltd| Pune      | Maharashtra | India   | FMCG            | 9845678901 | hello@deltafoods.com         |
| 00005      | Epsilon Textiles   | Surat     | Gujarat     | India   | Textile         | 9876501234 | contact@epsilontex.com       |
| 00006      | Zeta Motors        | Chennai   | Tamil Nadu  | India   | Automotive      | 9901234567 | info@zetamotors.com          |
| 00007      | Eta Pharma Ltd     | Hyderabad | Telangana   | India   | Pharmaceuticals | 9811122233 | contact@etapharma.com        |
| 00008      | Theta Electronics  | Noida     | UP          | India   | Electronics     | 9812233445 | sales@thetaelec.com          |
| 00009      | Iota Construction  | Jaipur    | Rajasthan   | India   | Construction    | 9823344556 | info@iotaconstruct.com       |
| 00010      | Kappa Energy       | Ahmedabad | Gujarat     | India   | Energy          | 9834455667 | contact@kappaenergy.com      |
| 00011      | Lambda Finance Ltd | Kolkata   | WB          | India   | Finance         | 9845566778 | hello@lambdafin.com          |
| 00012      | Mu Education Pvt Ltd| Lucknow  | UP          | India   | Education       | 9856677889 | info@muedu.com               |
| 00013      | Nu Hospitality     | Goa       | Goa         | India   | Hospitality     | 9867788990 | contact@nuhotel.com          |
| 00014      | Xi Agro Pvt Ltd    | Indore    | MP          | India   | Agriculture     | 9878899001 | hello@xiagro.com             |
| 00015      | Omicron Retail Ltd | Bhopal    | MP          | India   | Retail          | 9889900112 | sales@omicronretail.com      |

---
## 📌 Display Output  

### 1️⃣ Transparent Table Data (ZCOMPANY_MASTER)  

Below is how company master data looks in the transparent table:  

| COMPANY_ID | COMPANY_NAME        | CITY      | STATE       | COUNTRY | INDUSTRY        | CONTACT_NO | EMAIL                  |
|------------|---------------------|-----------|-------------|---------|-----------------|------------|------------------------|
| 00001      | Alpha Tech Pvt Ltd  | Mumbai    | Maharashtra | India   | IT Services     | 9876543210 | contact@alphatech.com  |
| 00002      | Beta Solutions Ltd  | Delhi     | Delhi       | India   | Consulting      | 9812345678 | info@betasolutions.com |
| 00003      | Gamma Industries    | Bangalore | Karnataka   | India   | Manufacturing   | 9823456789 | sales@gammaind.com     |

📸 Example screenshot:  
![Company Master Table](./assets/company_table.png)  

---

### 2️⃣ Selection Screen (Report Execution)  

When executing the report, the **Selection Screen** allows filtering by Company ID, City, or Industry.  

📸 Example screenshot:  
![Selection Screen](./assets/selection_screen.png)  

---

### 3️⃣ Search Help (F4 Functionality)  

On the **Company ID** field, a **Search Help (ZCOMPANY_SH)** is attached.  
When the user presses `F4`, a popup displays a list of companies for easy selection.  

📸 Example screenshot:  
![Search Help](./assets/search_help.png)  
  
---

## 👨‍💻 Author  
**Parveen Kumar**  
SAP Certified Associate – Back-End Developer – ABAP Cloud  
📧 parveen.email@example.com  
🌐 [LinkedIn](https://www.linkedin.com/in/parveen) | [GitHub](https://github.com/parveen)
