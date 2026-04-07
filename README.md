# Online Fitness Coaching Platform — ER Diagram

## exaclidraw => -https://excalidraw.com/#json=3FodnR5qnQJ_jfLGOmrSZ,bYFoeNMz0UlAw9c--Gt8RA
## blog => https://x.com/hiteshdhayall/status/2041568461613322396?s=20

This project designs the **Entity Relationship (ER) diagram** for an **online fitness coaching platform**. The goal of the platform is to allow fitness influencers or trainers to manage their online coaching business. Trainers can create coaching programs, onboard clients, schedule sessions, track progress, and maintain regular check-ins.

The system models a real-world scenario where clients may purchase different coaching plans, attend consultations, submit weekly updates, and receive feedback from their trainer.

This repository contains the **ER diagram and database design** for this platform.

---

# Problem Statement

A fitness influencer initially manages clients through **Instagram DMs and video calls**. As the business grows, they need a structured platform where they can:

* onboard new clients
* sell fitness programs
* manage subscriptions
* schedule consultations
* track progress
* record client check-ins
* maintain trainer feedback

The objective of this project is to **design a database structure that supports this ecosystem**.

---

# Key Features Modeled in the Database

The ER diagram supports the following functionality:

### User Management

The platform has two main types of users:

* **Trainer** – creates programs and coaches clients
* **Client** – purchases programs and receives coaching

---

### Coaching Programs / Plans

Trainers can create structured fitness plans such as:

* Fat loss program
* Muscle gain program
* Consultation sessions
* Workout + diet coaching

Multiple clients can enroll in the same program.

---

### Subscriptions

When a client purchases a program, the system creates a **subscription** record.

The subscription stores:

* which client purchased the plan
* which plan was purchased
* start and end dates
* subscription status
* associated payment

---

### Payments

All payments made by clients are recorded in the **Payment entity**, including:

* amount
* payment method
* payment status
* transaction details

---

### Sessions / Consultations

Some programs include **live coaching sessions** or consultations.

The system tracks:

* trainer
* client
* session time
* session type
* meeting status

---

### Weekly Check-ins

Clients submit weekly progress reports during their program.

Check-ins can contain:

* body weight
* body fat
* notes
* weekly progress updates

---

### Progress Tracking

The system records body measurements over time to track improvements.

Examples:

* weight
* chest
* waist
* hips
* body fat

This allows the platform to visualize long-term progress.

---

### Trainer Notes

Trainers can leave feedback on client progress.

Examples:

* diet adjustments
* workout modifications
* coaching feedback

These notes help guide the client through their fitness journey.

---

# Core Entities in the ER Diagram

| Entity          | Description                                        |
| --------------- | -------------------------------------------------- |
| USER            | Stores information about people using the platform |
| TRAINER_PROFILE | Additional information specific to trainers        |
| PLAN            | Coaching programs created by trainers              |
| SUBSCRIPTION    | Records when a client purchases a plan             |
| PAYMENT         | Stores payment transactions                        |
| SESSION         | Consultation or live coaching sessions             |
| CHECK_IN        | Weekly updates submitted by clients                |
| PROGRESS_LOG    | Tracks body measurements and progress              |
| TRAINER_NOTE    | Feedback provided by trainers                      |

---

# Example Workflow

To understand how the system works, consider this example:

1. **Hitesh** joins the platform as a **trainer**.
2. Hitesh creates a coaching program called **"12 Week Fat Loss Program."**
3. **Sahil Pannu** signs up as a **client**.
4. Sahil purchases the program.
5. The system creates a **subscription** and records Sahil’s **₹5000 UPI payment**.
6. Hitesh schedules an **initial consultation session** with Sahil.
7. During the program, Sahil submits **weekly check-ins** with updates about weight and progress.
8. The system records Sahil’s progress, such as **weight dropping from 82 kg to 78 kg**.
9. Hitesh reviews the updates and adds **trainer feedback** to guide Sahil.

This workflow demonstrates how the database supports a real coaching platform.

---

# Relationships in the ER Diagram

Important relationships include:

* A **trainer can create multiple plans**
* A **client can purchase multiple plans over time**
* A **plan can have many clients**
* A **subscription can have multiple sessions and check-ins**
* A **trainer can manage many clients**

---

# Diagram

The repository includes an **ER diagram image** showing:

* entities
* attributes
* primary keys
* foreign keys
* relationships
* cardinality

---

# Design Goals

The database was designed with the following goals:

* clear separation of user, program, and progress data
* scalable structure for multiple clients and trainers
* support for subscriptions and payments
* structured progress tracking
* clean relational modeling

---

# Tools Used

The ER diagram can be created using tools such as:

* Excalidraw
* Draw.io
* Eraser
* FigJam

---

# Conclusion

This ER diagram models a **complete online fitness coaching ecosystem** where trainers can manage clients, programs, sessions, and progress in a structured and scalable way.

The design keeps the system **organized, practical, and ready for real-world implementation** in a fitness coaching platform.
