# Optimize Scheduling

## Description
This repository contains a VBA project for optimizing the scheduling of operations in an operating theatre. The goal is to efficiently schedule operations to minimize the number of days needed while ensuring surgeons do not exceed their working hour limits.

## Project Specifications
The operating theatre manager needs to schedule operations for a list of patients, ensuring that:
- Operations are scheduled over as few days as possible.
- Two surgeons work in separate operating theatres, with a preference for 6-hour working days and a maximum of 7.5 hours.

### Greedy Heuristic Approach
1. Select a surgeon whose schedule has not been planned.
2. Create an ordered list of patients requiring treatment by that surgeon, sorted by expected operation duration (descending).
3. Schedule the patient with the longest expected duration into the earliest acceptable day for the surgeon.
4. Continue scheduling patients until all are assigned.

### Ties in Scheduling
- Ties are broken by selecting the patient with the higher standard deviation for operation duration.
- If expected durations and standard deviations are identical, the patient with the smaller index is chosen first.

## Features
- **Data Input**: Reads any sized data table from an Excel file.
- **Heuristic Execution**: Implements the greedy heuristic to schedule operations.
- **Result Output**: Displays the schedule creatively using buttons, tables, and charts.

## Sample Data
Sample data for testing is provided in an Excel file named `TestData.xlsx`.
