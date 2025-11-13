# INSY6112 FINAL EXAM SUBMISSION  
**Student:** Coherence Tasimba Mlambo  
**Student Number:** ST10448252  

---

## Table of Contents
1. [Question 1 – Surrogate Keys and Relationships](#question-1)
2. [Question 2 – Database Normalization](#question-2)
3. [Question 3 – SQL Table Creation and Queries](#question-3)
4. [Question 4 – MongoDB Operations](#question-4)

---

## Question 1 – Surrogate Keys and Relationships

### Surrogate Primary Keys
| Table | Primary Key | Attributes |
|-------|------------|------------|
| Faculty | faculty_id | faculty_name |
| Qualification | qualification_id | qualification_name |
| Module | module_id | module_name |
| NQF_Level | nqf_level_id | level_description |
| Qualification_Module | qualification_module_id | module_code |

### Relationships Implemented
- **Faculty (1) → Qualification (Many)** via `faculty_id` (FK)  
- **Qualification (Many) → Module (Many)** resolved using `Qualification_Module` junction table  
- **NQF_Level (1) → Module (Many)** via `nqf_level_id` (FK)  

### Many-to-Many Relationship Resolution
- The M:N relationship between Qualification and Module is resolved using the `Qualification_Module` table, which stores the specific `module_code` for each qualification-module combination.

---

## Question 2 – Database Normalization

### Step 1: Analysis of 1NF Table
- The table is in **1NF** (no repeating groups, each cell has a single value).  
- **Composite Primary Key:** `(ChefID, Restaurant)`  
- **Partial Dependency:** `ChefID → ChefName` (violates 2NF)  

### Q2.1: Normalization to Second Normal Form (2NF)
- **Solution:** Remove partial dependencies by splitting the table.

**Tables in 2NF:**  
1. **CHEF**  
   | ChefID (PK) | ChefName |
   |------------|----------|  
2. **CHEF_RESTAURANT**  
   | ChefID (FK, PK) | Restaurant (PK) |

**Dependency Diagram:**  
