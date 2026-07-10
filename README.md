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
  
<img width="665" height="388" alt="image" src="https://github.com/user-attachments/assets/7a0b8b4a-a503-4e3f-8771-edc3002ed86f" />

---

**Step 2: Stream Extraction & I/O Appending**


Isolate distinct sections of the target binary file using standard output and append redirections without destroying existing structural content.  

* Isolate the leading 5 lines into the target configuration manifest
   * `head -n 5 /home/student/bin/manage > /home/student/grading/review.txt`

* Append the trailing 3 lines securely without overwriting file contents
   * `tail -n 3 /home/student/bin/manage >> /home/student/grading/review.txt`

<img width="760" height="264" alt="image" src="https://github.com/user-attachments/assets/f7d60ad9-2c03-4ad9-9642-441c7318ebd6" />

---

**Step 3: Text Manipulation & In-Line Patching**


Duplicate the tracking log and utilize a CLI text editor (Vim) to simulate modifying specific parameters within a staging configuration.  

* Duplicate file for staging
   * cp /home/student/grading/review.txt /home/student/grading/review-copy.txt

* Execute vim editing operations
   * vi /home/student/grading/review-copy.txt
      * Vim operations applied:
      * Duplicated the line containing `Test JJ`.
      * Purged the string containing `Test HH`.
      * Appended `A new line` precisely between the `Test BB` and `Test CC` boundaries.
    
<img width="774" height="413" alt="image" src="https://github.com/user-attachments/assets/92bf7416-67c2-434c-8f93-9692e5273baa" />

 <img width="591" height="250" alt="image" src="https://github.com/user-attachments/assets/2060c9db-448e-46e8-a8c4-044698122cd4" />

---

**Step 4: Link Engineering & Metadata Auditing**


Establish architectural shortcuts (hard and soft links) across storage paths and export an untainted system directory manifest.  

* Map an immutable hard link to the grade1 asset
   * `ln /home/student/grading/grade1 /home/student/hardcopy`

* Map a flexible symbolic pointer to the grade2 asset
   * `ln -s /home/student/grading/grade2 /home/student/softcopy`

* Export long-listing metadata attributes omitting hidden files
   * `ls -l /boot > /home/student/grading/longlisting.txt`

<img width="725" height="308" alt="image" src="https://github.com/user-attachments/assets/7ac0dacd-42f2-4f70-95d5-9fb3eae15b18" />

---

**Step 1: Laboratory Compliance Execution**


Return to the workstation context and trigger the programmatic laboratory script to evaluate configuration alignment against the technical constraints.  

<img width="625" height="460" alt="image" src="https://github.com/user-attachments/assets/9685d254-2ef1-4cad-be4e-96ace3872c3b" />


**Step 2: Workspace Environment Teardown**


De-provision local tracking mechanisms to return the deployment sandbox back to baseline conditions.  

<img width="591" height="226" alt="image" src="https://github.com/user-attachments/assets/7f933a25-8c2c-4e5b-b8da-c408f5d243eb" />










## 📊 Verification and Testing













