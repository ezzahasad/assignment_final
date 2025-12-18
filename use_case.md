# Medication Understanding and Reconciliation Support Tool

## Overview
This project designs a cloud based application that organizes patient medication lists and explains what each medication is for, helping reduce patient confusion and improve medication reconciliation during clinical visits.

## Problem Statement
Patients often do not understand what their medications are prescribed for or why they need to take them, especially when they feel asymptomatic. As a result, patients may report that they are not taking medications for certain conditions, even though their medication list shows active prescriptions.

This confusion can lead to poor medication adherence, inaccurate medication histories, and inefficient medication reconciliation during clinical visits. A system that clearly organizes medications by purpose and highlights common side effects can help improve patient understanding and support more productive discussions with clinicians. This is especially important for patients managing chronic conditions that require long term medication use.


## Data Sources
The system works with synthetic medication data to avoid the use of real patient information. Data sources include CSV files or form based entries that contain patient medication lists, including medication name, dose, frequency, and intended condition. 

Additional reference data may include a simple lookup table describing common medication purposes and frequently reported side effects. All raw submissions are treated as input data and stored for traceability.

## Basic Workflow
1. A patient or clinic staff member submits a medication list through a form or uploads a CSV file.
2. The system stores the raw submission in cloud storage.
3. A serverless process validates the data format and required fields.
4. Clean medication records are stored in a managed SQL database.
5. The system organizes medications by condition and highlights common side effects and potential interactions for patient education.
6. Clinicians view a summarized medication list during visits to support efficient medication reconciliation.
