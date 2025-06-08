# Racketminster Booking and Management System – Conceptual and Logical Data Models

## Overview

This repository contains the full conceptual and logical data models for the **Racketminster Booking and Court Management System**, created as part of the 5COSC020W Database Systems module at the University of Westminster.

The data models were developed using **Draw.io** and presented in PDF format. These models aim to accurately represent the data requirements, relationships, and business logic outlined in the project brief, with a focus on clarity, specialization, and real-world mapping.

## Contents

- `W2044381BOTHERRD.drawio.pdf`: The full Draw.io diagram including the conceptual and logical models.
- `W2044381ERRDCW+(1).pdf`: The written coursework report explaining the modelling choices, entity justifications, attributes, specializations, and relationship multiplicities.

## Conceptual Model

The **conceptual model** outlines the high-level structure of the system by identifying the main entities and relationships without diving into detailed attributes or constraints. It provides a clear visual of the overall system architecture, including:

- Core entities such as:  
  - `Person`  
  - `Player`  
  - `Instructor`  
  - `Caretaker`  
  - `Court`  
  - `Park`  
  - `Playing Session`  
  - `Booking`  
  - `Maintenance Log`  
  - `Equipment`
- Use of generalization/specialization to define sub-entities:
  - `Court` → `Tennis`, `Pickleball`, `Multipurpose`
  - `Playing Session` → `Supervised`, `Unsupervised`
  - `Caretaker` → `Park Caretaker`, `Court Caretaker`
  - `Person` → `Player`, `Instructor`, `Caretaker`
- Important relationships like:
  - Supervision of sessions by instructors
  - Participation of players in sessions
  - Maintenance responsibilities
  - Equipment assignment to courts
  - Booking and block-booking logic

## Logical Model

The **logical model** builds upon the conceptual model by including:

- Detailed entity attributes and primary keys (e.g., `Instructor_ID`, `Court_Condition`, `Booking_Status`)
- Relationship multiplicities, constraints, and roles
- Ternary and recursive relationships where applicable (e.g., Player–Session–Court attendance)
- Realistic data modelling assumptions such as:
  - A playing session can only be held on one court at a time
  - Block bookings only apply to unsupervised sessions
  - Maintenance logs are tied to both equipment and caretakers
  - Referral tracking includes incentives and player-to-player promotion

## Key Features and Improvements

- Specialization used extensively to reflect real-world distinctions
- Clear and descriptive attribute design across all entities
- Logical constraints and multiplicities carefully matched to business rules
- Inclusion of ternary relationships for complex participation tracking
- Recursive modelling to represent follow-up sessions
- Modular and extensible entity structure supporting future growth

## How to View

- Use the `W2044381BOTHERRD.drawio.pdf` file to view the full diagram with both conceptual and logical components
- Refer to `W2044381ERRDCW+(1).pdf` for detailed descriptions of each entity, relationship, and design decision

## Author

- **Hamza Hassan**  
- University of Westminster  
- Module: 5COSC020W Database Systems  
- Coursework Part A – Tuesday Tutorial Group (4 PM – 6 PM)  
- Module Leader: Dr Francois Roubert  

## License

This project was developed for academic purposes. Please do not reuse or redistribute without permission from the author or the University of Westminster.
