# 🗃️ Inventory Management System (IMS)

A full-featured **Inventory Management System** implemented using **PostgreSQL**. This project models the complete backend schema and operations for an inventory-driven business. It handles **products, suppliers, purchases, storage, sales, returns, damages, promotions**, and more, with advanced SQL queries and triggers for dynamic stock management.

---

## 📁 Project Structure

- `DDL.txt`: Contains the complete database schema with all `CREATE TABLE` and `CONSTRAINT` definitions.
- `INSERT_statements.txt`: Provides data population scripts, schema alterations, and some dynamic constraints.
- `SQL Queries.txt`: Advanced SQL queries, views, triggers, and stored procedures for analytics and operations.

---

## 🧱 Database Schema Overview

The system is structured into multiple interconnected tables:

### ✅ Core Tables
- **Supplier**: Manages supplier information.
- **Product**: Catalogs all inventory products with stock and pricing.
- **Purchase_Order & Ordered**: Track orders from suppliers and their fulfillment status.
- **ProductInstance**: Represents individual items with unique identifiers and locations.
- **Storage_Location**: Maps physical warehouse locations.
- **Employee**: Information about staff involved in transactions.
- **Sales_Transaction**: Records product sales with payment details.
- **ReturnedProducts & Damaged_Products**: Capture return and damage cases for audit and analysis.
- **Promotions & Has_Promo**: Support discount campaigns across products.

---

## ⚙️ Functional Features

### 📌 Triggers & Functions

1. **Auto stock decrement** when a sale is made.
2. **Auto stock increment** when a return is processed.
3. **Auto stock increment on successful purchase delivery**.
4. **Mark returned items as "NowSold"** upon resale.
5. **Mark slow-moving items inactive** based on sales patterns.
6. **Delete discontinued products** after inactivity and stock depletion.

### 📊 Views

- `Inventory_Value`: Overall inventory valuation.
- `products_needing_reorder`: Highlights understocked products and suppliers.
- `orders_pending_past_expected_del_date`: Lists delayed incoming orders.

---

## 🔍 Example SQL Queries

- **Retrieve all products by a specific supplier**
- **Sales summary for a given date**
- **Top 3 best-selling products in the last 3 months**
- **Check reorder needs and recent order history**
- **Identify most returned or damaged suppliers**

---

## 🛠️ How to Use

1. **Set up PostgreSQL** and run the schema in `DDL.txt`.
2. **Load data** using `INSERT_statements.txt`.
3. **Run analytical queries** and **triggers** from `SQL Queries.txt`.
4. Use `pgAdmin` or `psql` CLI to explore and test queries.

---

## 📈 Business Logic Highlights

- **Cascade & Restrict constraints** for data integrity.
- **Real-time stock tracking** via triggers.
- **Dynamic discount management** with promotional associations.
- **Employee-linked transactions** with fallback on employee exit.
- **Fine-grained return/refund tracking**.

---

## 🚀 Future Enhancements

- Add UI frontend (React/Django).
- Add stored procedures for user-level actions.
- Implement role-based access control.
- Integrate barcode scanning and inventory alerts.

---

## 🧑‍💻 Author

**Panchal Dhruv**  
📬 [dhruv-panchal.medium.com](https://dhruv-panchal.medium.com/)  
🔗 GitHub: [panchaldhruv27223](https://github.com/panchaldhruv27223)

---

## 📜 License

This project is open-source and free to use under the MIT License.