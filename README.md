# 🛒 E-commerce Database Design – Peer Group Assignment (Group 540)

## 📘 Project Overview

This project involves designing and documenting a relational database schema for an e-commerce platform. The objective is to model key entities such as products, brands, variations, categories, sizes, and custom attributes in a scalable and normalised format.

## ✅ Work Done

### 1. **Schema Development**
We created a normalised SQL schema using Mysql with the following core tables:

| Table | Description |
|-------|-------------|
| `brand` | Stores brand-related information |
| `product_category` | Classifies products (e.g., electronics, clothing) |
| `product` | Stores general product details like name and price |
| `color` | Manages color options |
| `size_category` | Groups sizes into types (e.g., shoe size, clothing size) |
| `size_option` | Specific size values (e.g., M, L, 42) |
| `product_variation` | Combines product, size, and colour into unique variations |
| `product_item` | Represents SKU-level stock and pricing details |
| `product_image` | Stores image URLs and thumbnails |
| `attribute_type` | Defines attribute data types (text, number, etc.) |
| `attribute_category` | Organizes custom attributes into groups |
| `product_attribute` | Connects attributes to products for flexibility |

### 2. **ERD Design**
We designed a clear and professional **Entity-Relationship Diagram (ERD)** showing:
- Table relationships (1:1, 1:N, N:M)
- Primary keys (PK) and foreign keys (FK)
- All major attributes and connections


### 3. **SQL Script**
We developed a full SQL schema file:
- Auto-creates the database
- Defines all 12 main tables with keys and constraints
- Ensures data normalisation and referential integrity


---

## 🔄 Data Flow Between Entities

1. A **brand** is linked to many **products**
2. A **product** belongs to one **category** and one **brand**
3. A **product** can have multiple **images**
4. A **product** is connected to **product_variations** by color and size
5. Each **variation** (e.g., Red, Size M) links to one or more **product_items** (individual SKUS)
6. **product_items** hold stock, pricing, and are what customers buy
7. **attribute_type** and **attribute_category** define reusable fields like material or weight
8. **product_attribute** allows adding flexible, custom characteristics to any product
9. **size_option** is categorized under a **size_category** (e.g., Shoe sizes)

This data model ensures that every product can be richly described, flexibly customised, and precisely tracked through variations and inventory.

---

## 🧠 Learning Outcomes
- Hands-on experience with SQL DDL
- Understanding of e-commerce data modelling
- Practical use of Mysql Workbench for ERD design
- Collaboration and task sharing in a group setting

## 👥 Group Members (Group 540)
1. Denzel Odhiambo
Other group members are not participating 

---

## 🛠️ Tools Used
- **MySQL Workbench** – for schema modeling and ERD
- **VS Code / Notepad++** – for editing SQL

## 📌 Notes
- The schema is extendable (e.g., for cart, orders, users)
- Follows best practices for naming and constraints
