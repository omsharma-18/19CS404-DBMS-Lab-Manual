# Experiment 1: Entity-Relationship (ER) Diagram

## 🎯 Objective:
To understand and apply the concepts of ER modeling by creating an ER diagram for a real-world application.

## 📚 Purpose:
The purpose of this workshop is to gain hands-on experience in designing ER diagrams that visually represent the structure of a database including entities, relationships, attributes, and constraints.

---

## 🧪 Choose One Scenario:

### 🔹 Scenario 1: University Database
Design a database to manage students, instructors, programs, courses, and student enrollments. Include prerequisites for courses.

**User Requirements:**
- Academic programs grouped under departments.
- Students have admission number, name, DOB, contact info.
- Instructors with staff number, contact info, etc.
- Courses have number, name, credits.
- Track course enrollments by students and enrollment date.
- Add support for prerequisites (some courses require others).

---

### 🔹 Scenario 2: Hospital Database
Design a database for patient management, appointments, medical records, and billing.

**User Requirements:**
- Patient details including contact and insurance.
- Doctors and their departments, contact info, specialization.
- Appointments with reason, time, patient-doctor link.
- Medical records with treatments, diagnosis, test results.
- Billing and payment details for each appointment.

---

## 📝 Tasks:
1. Identify entities, relationships, and attributes.
2. Draw the ER diagram using any tool (draw.io, dbdiagram.io, hand-drawn and scanned).
3. Include:
   - Cardinality & participation constraints
   - Prerequisites for University OR Billing for Hospital
4. Explain:
   - Why you chose the entities and relationships.
   - How you modeled prerequisites or billing.

# ER Diagram Submission - Student Name

## Scenario Chosen:
University / Hospital (choose one)

## ER Diagram:
![ER Diagram](https://github.com/user-attachments/assets/b1d55303-fef8-435f-822f-ad437942b10e)


## Entities and Attributes:
- Academic Programs:Identifier,Name,Governing Departments
- Instructors:Staff Number,Name,Contact
- Departments:Department ID,Department Name
- Catalog of Courses:Number,Name,Number of Credits
- Students:Admission Number,Name,Contact,Date of Birth

## Relationships and Constraints:
- Relationship 1: Teaching(Cardinality: Many-to-Many,Participation: Partial–Partial)
- Relationship 2: Offered(Cardinality: Many-to-Many,Participation: Total–Partial)
- Relationship 3: Offers(Cardinality: One-to-Many,Participation: Total–Partial)
- Relationship 4: Register(Cardinality: Many-to-Many,Participation: Partial–Partial)
- Relationship 5: Enrolled(Cardinality: Many-to-One,Participation: Total–Partial)

## Extension (Prerequisite / Billing):
- To model prerequisites:
     - Add a relationship called "Prerequisite" between the same course entity (Catalog of Courses → Catalog of Courses).
     - This shows that one course depends on another.
- To model billing:
     - Add a new entity called "Billing" with attributes like Amount and Due Date.
     - Connect it to Students using a relationship like "Pays".
     - This shows that students receive bills and make payments.


## Design Choices:
- Entities like Students, Instructors, Programs, Courses, and Departments were chosen because they are the main parts of a university system.
- Relationships were added to show how these parts connect:
  - Students enroll in programs and register for courses.
  - Programs offer courses.
  - Instructors teach programs.
  - Departments offer programs.
- Assumptions:
  - A student can take many courses and belong to one or more programs.
  - A course can be part of different programs.
  - Not all instructors teach all the time.
  - Every entity has a unique ID to identify it.

## RESULT
   This the ER diagram for the University Problem.
