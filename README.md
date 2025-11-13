# INSY6112 Final Exam Submission  
**Student:** Coherence Tasimba Mlambo  
**Student Number:** ST10448252  

---

## Summary of Submission

### Question 1 – Surrogate Keys & Relationships
- Created surrogate primary keys for Faculty, Qualification, Module, NQF_Level, and Qualification_Module.  
- Implemented relationships:  
  - Faculty → Qualification (1:M)  
  - Qualification ↔ Module (M:N) via Qualification_Module  
  - NQF_Level → Module (1:M)  
- Resolved the many-to-many relationship between Qualification and Module using a junction table.

---

### Question 2 – Database Normalization
- **1NF → 2NF:** Removed partial dependencies by creating CHEF and CHEF_RESTAURANT tables.  
- **2NF → 3NF:** Checked for transitive dependencies; tables already in 3NF.  
- **Extended 3NF:** Introduced RESTAURANT and RESTAURANT_GROUP tables to remove transitive dependencies.

---

### Question 3 – SQL Tables & Queries
- Created **Patient, Doctor, and Appointment** tables with proper primary and foreign keys.  
- Inserted sample data.  
- Queries implemented:  
  - Display appointments within a date range.  
  - Count total appointments per patient.  
  - View patients assigned to a specific doctor (Doctor ID = 2).

---

### Question 4 – MongoDB Operations
- Created database `members_st10448252` and `members` collection.  
- Inserted sample member documents.  
- Queries implemented:  
  - Display all documents.  
  - List members born after 1979-01-12.

---

**End of Submission**  
**Submitted by:** Coherence Tasimba Mlambo (ST10448252)
