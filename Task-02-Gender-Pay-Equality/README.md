# Task 2 – Gender Pay Equality Classification

This task is part of the **Deloitte Technology Consulting Job Simulation** on [Forage](https://www.theforage.com/).  
The client, **Daikibo Industrials**, reported multiple internal complaints of **gender-based salary inequality**.  
The Forensic Tech team pre-processed compensation data and asked us to extend their analysis.

---

## 📊 Project Overview
The dataset (`Equality Table.xlsx`) contained 3 columns:
- **Factory** – company location  
- **Job Role** – employee role/title  
- **Equality Score** – integer score ranging from -100 to +100  
  - `0` = perfect equality  
  - Positive/negative values = bias magnitude/direction  

The task was to classify each job role into **3 categories** based on its Equality Score.

---

## ⚙️ Approach

1. **Created New Column – Equality Class**  
   Classification logic applied:  

   - **Fair**: -10 ≤ Equality Score ≤ +10  
   - **Unfair**: (-20 ≤ Equality Score < -10) or (10 < Equality Score ≤ 20)  
   - **Highly Discriminative**: Equality Score < -20 or Equality Score > 20  

2. **Examples**  
   - `10 → Fair`  
   - `-9 → Fair`  
   - `-15 → Unfair`  
   - `30 → Highly Discriminative`  

3. **Output**  
   - Produced an updated Excel file with the 4th column **Equality Class** appended.  

---

## Excel Dataset
[Task 5 Equality Table](./Task 5 Equality Table.xlsx)
– Final version with Equality Class column 

## 🛠️ Tools & Skills
- Microsoft Excel (formulas & classification)  
- Data Cleaning & Categorization  
- Forensic / HR Analytics  

---

