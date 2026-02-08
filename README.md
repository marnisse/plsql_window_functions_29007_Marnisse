<img width="1920" height="1080" alt="table of medication and patients" src="https://github.com/user-attachments/assets/b5ba8530-23d0-41b9-a270-9d74224521bf" />
<img width="1920" height="1080" alt="Screenshot (19)" src="https://github.com/user-attachments/assets/349673e9-99d6-41e9-8fb0-07e395a7e895" />
<img width="1920" height="1080" alt="Screenshot (18)" src="https://github.com/user-attachments/assets/d0b35b95-8887-4620-9b22-a5cd8f60004c" />
<img width="1920" height="1080" alt="running total" src="https://github.com/user-attachments/assets/8cf818d0-9de7-4124-b0df-0f97bffd4f53" />
<img width="1920" height="1080" alt="prescription" src="https://github.com/user-attachments/assets/d67ffcb1-0db9-44c7-9bbc-a89dc0229e30" />
<img width="1920" height="1080" alt="patients paid" src="https://github.com/user-attachments/assets/9a350cce-7b24-43ad-a0bd-7205db8272a7" />
<img width="1920" height="1080" alt="ERD" src="https://github.com/user-attachments/assets/d280297b-f35b-4a96-9a59-04e012a03751" />
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
