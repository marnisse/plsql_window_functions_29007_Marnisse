# plsql_window_functions_29007_Marnisse
Business Context: A national pharmacy chain managing thousands of daily prescriptions across multiple urban and rural branches. 

Data Challenge: The pharmacy struggles to identify which high-value medications (like specialty biologics) have the most consistent demand and which pharmacists are processing the highest volume of error-free claims. They also need to spot "at-risk" patients who might be falling behind on their chronic medication refills. 

Expected Outcome: Develop a reporting dashboard that ranks top-performing branches, segments patients by adherence levels, and identifies seasonal trends in medication dispensing to optimize inventory. 
1. Descriptive — What happened?
Based on the SQL analysis of the pharmacy database, we observed a steady volume of prescriptions across the North and South regions. The RANK() function highlighted Amoxicillin and Metformin as the highest revenue-generating medications for the current quarter. Additionally, our LEFT JOIN analysis identified that approximately 15% of the registered patient base (e.g., Sarah Inactive) has not yet fulfilled a prescription, indicating a gap between registration and actual sales.

2. Diagnostic 
By applying the LAG() navigation function, we discovered that while some patients maintain consistent refill schedules, others have irregular gaps between dispense_date entries, suggesting potential medication non-adherence. The NTILE(4) distribution analysis shows that the top 25% of patients contribute to over 60% of the total revenue, primarily driven by high-cost chronic medications like Lisinopril and Forxiga. The "Empty Set" results found during initial testing were diagnosed as a lack of transactional records in the Prescriptions table, despite having established master data in Patients and Medications.

3. Prescriptive 
To optimize pharmacy operations and patient health outcomes, the following actions are recommended
