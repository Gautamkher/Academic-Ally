![Python](https://img.shields.io/badge/Python-Flask-blue)
![React](https://img.shields.io/badge/Frontend-React-61DAFB)
![MySQL](https://img.shields.io/badge/Database-MySQL-orange)
![SQL](https://img.shields.io/badge/SQL-Stored%20Procedures-green)

# Academic Ally

Academic Ally is a **full-stack academic analytics platform** designed to help students track academic performance while giving instructors actionable insights into course outcomes.

The system allows students to submit assignments, receive feedback, and visualize performance analytics. Faculty members can create assignments, evaluate submissions, and analyze class-level trends.

This project was developed as part of **CS411: Database Systems at the University of Illinois Urbana-Champaign**.

---

## Project Overview

Academic Ally focuses on transforming academic data into meaningful insights.

The platform collects assignment responses and computes performance metrics that allow both students and instructors to better understand academic progress.

Students can identify weak topics and track improvement over time, while instructors can evaluate the effectiveness of assignments and teaching methods.

---

## Key Features

### Student Features

- Submit assignments
- Update or resubmit assignments before deadlines
- View assignment grades
- Track upcoming assignments
- View personal performance analytics
- Provide feedback to instructors

### Faculty Features

- Create assignments
- Grade student submissions
- Monitor class performance trends
- View aggregated student feedback
- Analyze assignment difficulty vs student performance

---

## Database Design

The system is built on a relational database modeling academic entities such as:

- Students  
- Faculty  
- Courses  
- Classes  
- Assignments  
- Questions  
- Submissions  

The schema ensures **data integrity and normalization up to BCNF**, preventing redundancy and ensuring efficient querying.

The database supports relationships such as:

- Students submitting assignments
- Faculty creating and grading assignments
- Courses containing multiple assignments
- Classes containing multiple students

---

## Advanced SQL Features

### Stored Procedures

Stored procedures automate grading logic by comparing student responses with correct answers and computing assignment scores.

These procedures:

- Evaluate objective responses
- Calculate total assignment scores
- Store incorrect response topics for analytics

### Triggers

Database triggers automatically update total scores when subjective grades are added.

This ensures **consistent grading calculations at the database level**.

---

## Data Analytics

Academic Ally derives insights from stored academic data to support decision making.

Examples include:

- Average class performance per assignment
- Topic-level performance analysis
- Identification of weak topics for students
- Assignment difficulty trends
- Student performance compared to peers

These analytics help both students and faculty make informed academic decisions.

---

## System Architecture

The platform consists of three primary components.

**Frontend**
- Interactive UI for students and faculty
- Dashboard visualizations

**Backend**
- REST APIs handling assignment submission and grading workflows

**Database**
- Relational database storing academic data
- SQL queries powering analytics and dashboards

---

## Technologies Used

**Frontend**
- React

**Backend**
- REST APIs

**Database**
- MySQL
- Stored Procedures
- Triggers
- Complex SQL Queries

**Visualization**
- Chart.js
- Analytics dashboards

---

## Example Insights Generated

Academic Ally can automatically generate insights such as:

- Students performing below class average
- Topics where the majority of students struggle
- Assignment difficulty vs class performance
- Performance trends across assignments

These insights help instructors refine teaching strategies and help students focus on areas needing improvement.

---

## My Contributions

My primary contributions to the project included:

- Faculty-related CRUD operations
- Development of stored procedures for automated grading
- Implementation of database triggers for score calculations
- Backend logic for analytics queries
- UI integration for analytics dashboards

---

## Repository Structure

```
Academic-Ally
│
├── academic-ally
│   ├── BE
│   │   ├── app
│   │   │   ├── databases.py        # Database configuration and connection setup
│   │   │   ├── blueprints          # API route blueprints
│   │   │   ├── faculty             # Faculty related endpoints and logic
│   │   │   ├── feedback            # Feedback processing modules
│   │   │   └── student             # Student related endpoints and analytics
│   │   │
│   │   └── main.py                 # Backend application entry point
│   │
│   └── FE
│       └── academic-ally
│           ├── public              # Static assets
│           └── src                 # Frontend source code (React components)
│
└── docs
    ├── Database Design Document
    ├── SQL Commands
    ├── ER Diagram
    └── Project Description
```

---

## Team

This project was developed as part of a team for the CS411 Database Systems course.

- Gautam Kher
- Vaibhav Bhandari
- Aditya Jhunjhunwala
- Bhuvanesh Shukla

---

## Future Improvements

Potential extensions to the system include:

- plagiarism detection for subjective answers
- AI-generated feedback aggregation
- recommendation systems for study resources
- collaborative learning tools
