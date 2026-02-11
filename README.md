## 📦 S2T3 — MongoDB Structures

## 🎯 Project Goal & Overview

The goal of this project is to practice **NoSQL data modeling with MongoDB** through a set of exercises based on real-world scenarios.

This repository defines the MongoDB data model for the optical store **“Cul d’Ampolla”**, focused on managing:
- customers and recommendations
- suppliers
- employees
- glasses
- sales with date and time

The project emphasizes:
- designing database structures according to different application perspectives
- choosing between embedded documents and references
- justifying modeling decisions in a NoSQL context

---

## 📦 Deliverables

For each exercise, the repository includes:

- s.json → MongoDB script that creates the collections and inserts sample data according to the designed NoSQL model.
- data model diagram → preliminary schema design used to define entities, relationships, and embedding vs referencing decisions before implementing the JSON structure.

---

## 🤔 Reflections on NoSQL Design

While designing the MongoDB models for this project, I realized that there are multiple valid ways to structure a NoSQL database.

Two main approaches became clear:

- reference-based modeling → separate collections per entity, using ObjectId references instead of foreign keys. This approach keeps data more normalized and reduces duplication.
- embedded document modeling → storing related data inside arrays or nested objects within the same document. This may introduce duplication, but improves read performance and simplifies queries.

The main takeaway is that MongoDB schema design is driven by access patterns rather than strict normalization rules.  
The optimal structure depends on how the application consumes and updates data.

---

## 🧩 LEVEL 1 — Optical Store

### 📌 Exercise 1 — Customer-Centric View

Design the database model assuming the interface is oriented to the customer.

The system must store:
- customer personal data and registration date
- recommended-by relationship between customers
- sales history per customer
- employee responsible for each sale
- date and time of each sale
- glasses sold (brand, frame type, colors, lens graduation, price)
- supplier information for the glasses

---

### 📌 Exercise 2 — Glasses-Centric View

Redesign the database model assuming the interface is oriented to the glasses.

The model must allow:
- viewing glasses as the main entity
- identifying their supplier
- tracking related sales
- linking sales with customers, employees, and timestamps

---

## 🧩 LEVEL 2 — Food Delivery System

### 📌 Exercise 1 — Online Food Ordering Platform

Design a MongoDB database for an online food delivery system with the following requirements:

- customers can place multiple orders
- each order belongs to one customer and one store
- orders can include multiple products (pizzas, burgers, drinks)
- orders store date/time, delivery or pickup type, quantities, total price, and notes
- stores manage multiple orders
- employees work in a single store
- delivery orders store the delivery employee and delivery date/time
- pizzas belong to categories that may change over time

---

## 🛠 Technologies

- MongoDB
- MongoDB Compass
- Docker
- JSON
- Git & GitHub
