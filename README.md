# Oracle Pluggable Database Assignment II

**Student Name:** Derrick  
**Student ID:** 29366  
**Repository Name:** oracle_pdb_ass_II_29366_derrick  

## 📖 Overview
This repository documents the completion of Assignment II, focusing on Oracle Pluggable Databases (PDBs). The tasks involved creating a persistent PDB, managing user privileges, and demonstrating the lifecycle of a temporary PDB using Oracle Database 23ai Free in a Docker container.

## 🛠 Oracle Environment Used
- **Database Version:** Oracle Database 23ai Free
- **Containerization:** Docker
- **OS:** macOS
- **Tools:** SQL*Plus, SQL Developer

## 📝 Task Explanations

### Task 1: Main PDB and User Creation
I created a persistent Pluggable Database named **`DE_PDB_29366`**. Inside this PDB, I created a user **`DERRICK_PLSQLAUCA_29366`** and granted them `CONNECT`, `RESOURCE`, and `DBA` privileges.

**Evidence:**
![User Creation](screenshots/task1_user_creation.png)

### Task 2: Temporary PDB Lifecycle
I demonstrated the ability to create and delete PDBs.
1. Created a temporary PDB named **`DE_TO_DELETE_PDB_29366`**.
2. Verified its existence (`MOUNTED` state).
3. Dropped the PDB including datafiles.
4. Verified it was removed from the PDB list.

**Evidence:**
![Temp PDB Lifecycle](screenshots/task2_temp_pdb.png)

### Task 3: OEM / GUI Dashboard
I connected to the database using a GUI tool to verify the schemas and data files.

**Evidence:**
![OEM Dashboard](screenshots/task3_oem_dashboard.png)

## 🧩 Challenges & Solutions
- **Challenge:** Initial issues with file permissions when creating PDBs.
- **Solution:** Ensured the Docker container had the correct volume mounts and used standard Oracle naming conventions.
- **Challenge:** Correctly identifying the PDB state (Mounted vs Read/Write).
- **Solution:** Used `SHOW PDBS` frequently to verify the status before running commands.

## 📜 Integrity Statement
I certify that this work is my own and complies with the assignment's ethical guidelines. The screenshots and code provided are result of my own execution.

---
*Assignment completed on February 17, 2026.*
