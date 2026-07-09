# Red Hat Enterprise Linux (RHEL 9.3) Core Competency: Command Line File Management & Stream Redirection

## 🎯Project Overview
This project validates core system administration competencies in POSIX file system manipulation, text-stream processing, and I/O redirection within a Red Hat Enterprise Linux 9.3 environment. The objective is to demonstrate absolute command over the Bash shell by systematically organizing directories, manipulating files, executing complex line-extraction routines, and managing persistent file system links.  

## 💻Environments and Technologies Used
* Operating System Environment: Red Hat Enterprise Linux 9.3 (RHEL) 
* Shell Environment: Bash 
* Core Utilities Demanded: `mkdir`, `touch`, `cp`, `head`, `tail`, `ln`, `ls`, `vim`

## 📋Objectives and Scenario
The scenario simulates standard production tasks where an administrator must isolate log data, maintain backups, modify software configuration lines, and establish symbolic pointers.  

### Technical Specification Requirements:
* **Directory Provisioning**: Establish an administrative /home/student/grading directory. 
* **File Initialization**: Generate empty tracker files (grade1, grade2, grade3).
* **Text Processing & I/O Isolation**: Extract a precise block of header lines (first 5 lines) and footer lines (last 3 lines) from a source bin file and cleanly merge them into a single file without resource loss or collision. 
* **Configuration Editing**: Perform hot-patches on a duplicated configuration file to duplicate targeted lines, strip specific variables, and inject custom configuration text.  
* **Link Architecture Deployment**: Map explicit hard and soft (symbolic) structural linkages across the user profile. 
* **Metadata Auditing**: Capture a clean, long-form directory manifest excluding hidden vectors.  

## 🛠️ High-Level Deployment and Configuration Steps

**Step 1: Directory Provisioning & Target Initialization**

Initialize the lab environment and provision the structured file workspace under the user home directory.  

* Prepare the lab environment
  * `lab rhcsa-rh124-review1 start`
   
* Connect to target server node
  * `ssh student@serverb`
   
* Provision workspace and initialize files
  * `mkdir /home/student/grading`
  * `touch /home/student/grading/{grade1,grade2,grade3}`
  
<img width="665" height="388" alt="image" src="https://github.com/user-attachments/assets/0451f0b4-530d-483c-9d92-75fc07a190f4" />





## 📊 Verification and Testing













