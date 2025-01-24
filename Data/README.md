# 📊 **Dataset Description**
📌 **Note**:  
This datasets are uploaded using git LFS and its just the attributes of the files that is seen here, to have access to this dataset you need to clone this repository and install git LFS then pull to access the datasets. 

git lfs install  (if you are using a Mac you need brew to install this from terminal then initialise the install on the working directory or the local host)
git clone https://github.com/Tolorunleke/InstaCart.git
git lfs pull

Ensure you are on the working directory before running the provided code.

## 🛒 **Orders Dataset** (3.4M rows, 206K users)

### **Columns**
- **`order_id`**: 🆔 Order identifier  
- **`user_id`**: 👤 Customer identifier  
- **`eval_set`**: 📂 Evaluation set this order belongs to (see **Evaluation Sets** below)  
- **`order_number`**: 🔢 Order sequence number for this user (1 = first, n = nth)  
- **`order_dow`**: 📅 Day of the week the order was placed  
- **`order_hour_of_day`**: ⏰ Hour of the day the order was placed  
- **`days_since_prior`**: 🔄 Days since the last order, capped at 30 (NA for first order)  

---

## 🛍️ **Products Dataset** (50K rows)

### **Columns**
- **`product_id`**: 🆔 Product identifier  
- **`product_name`**: 🏷️ Name of the product  
- **`aisle_id`**: 🔗 Foreign key linking to the **Aisles Dataset**  
- **`department_id`**: 🔗 Foreign key linking to the **Departments Dataset**  

---

## 🛒 **Aisles Dataset** (134 rows)

### **Columns**
- **`aisle_id`**: 🆔 Aisle identifier  
- **`aisle`**: 🏬 Name of the aisle  

---

## 🏢 **Departments Dataset** (21 rows)

### **Columns**
- **`department_id`**: 🆔 Department identifier  
- **`department`**: 🏷️ Name of the department  

---

## 📦 **Order Products Dataset (30M+ rows)**

### **Columns**
- **`order_id`**: 🔗 Foreign key linking to the **Orders Dataset**  
- **`product_id`**: 🔗 Foreign key linking to the **Products Dataset**  
- **`add_to_cart_order`**: 🛒 Order in which each product was added to the cart  
- **`reordered`**: 🔄 Indicates if the product was ordered before by the user (1 = Yes, 0 = No)  

---

## 🗂️ **Evaluation Sets** (Column: `eval_set` in **Orders Dataset**)

1. **`prior`**: 📦 Orders prior to the user's most recent order (~3.2M orders)  
2. **`train`**: 📘 Training data for participants (~131K orders)   

---
