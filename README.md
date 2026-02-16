# Oracle PDB Assignment II - Derrick

## Overview
This assignment focused on creating, managing, and reporting Oracle Pluggable Databases (PDBs) using Oracle Database 21c running in Docker. The objectives were to demonstrate practical skills in:

- Creating a new PDB
- Managing users within a PDB
- Creating and deleting a temporary PDB
- Accessing Oracle Enterprise Manager (OEM)
- Documenting the tasks and reporting via GitHub

---

## Oracle Environment
- **Database:** Oracle Database 21c Enterprise Edition  
- **Platform:** Docker container on MacBook  
- **CLI Tool:** SQL*Plus  
- **GUI Tool:** Oracle Enterprise Manager (OEM) 21c  

---

## Task Explanations

### Task 1: Create a New Pluggable Database (PDB)
- **PDB Name:** `de_pdb_2026101`  
- **User Created:** `Derrick_plsqlauca_2026101`  
- **Password:** `SimplePwd123`  
- **Steps:**
  1. Connected to the Oracle container using SQL*Plus as SYSDBA.
  2. Created the PDB using `CREATE PLUGGABLE DATABASE` command.
  3. Opened the PDB with `ALTER PLUGGABLE DATABASE ... OPEN`.
  4. Verified the user exists inside the PDB.
- **Screenshots:** `screenshots/pdb_creation.png`

---

### Task 2: Create and Delete a Temporary PDB
- **Temporary PDB Name:** `de_to_delete_pdb_2026101`  
- **Steps:**
  1. Created a temporary PDB with a separate admin user.
  2. Verified that the PDB exists using `SHOW PDBS`.
  3. Dropped the PDB completely using `DROP PLUGGABLE DATABASE ... INCLUDING DATAFILES`.
  4. Confirmed that the PDB no longer exists.
- **Screenshots:** `screenshots/pdb_deletion.png`

---

### Task 3: Oracle Enterprise Manager (OEM)
- **URL:** [https://localhost:5500/em](https://localhost:5500/em)  
- **Login:** SYS / SYSDBA  
- **Steps:**
  1. Accessed OEM dashboard through a browser.
  2. Confirmed all PDBs (created and deleted) were reflected in the dashboard.
  3. Verified that my username and PDB details are visible.
- **Screenshots:** `screenshots/oem_dashboard.png`

---

## Challenges & Solutions
- **Challenge:** Docker container authentication for Oracle registry was initially failing.  
- **Solution:** Logged into Oracle Container Registry with a valid Oracle account and successfully pulled the image.

- **Challenge:** File path errors during PDB creation.  
- **Solution:** Used the correct `FILE_NAME_CONVERT` paths to copy from `PDB$SEED` to new PDB directories.

---

## Integrity Statement
I confirm that this work is entirely my own. All PDB creation, deletion, and OEM configuration steps were performed personally, and screenshots provided are genuine evidence of my work.

---

## Repository Structure
