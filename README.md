# FashionEasy SQL, RAG, LLM and Fine Tuning Project

## Project Name: FashionEasy

###  Description  
FashionEasy is a database system designed to manage users, products, orders, vendors, and styling suggestions. It facilitates efficient tracking of fashion-related data, including user preferences, product inventory, order details, and vendor relationships.

---

##  Project Files and Purpose  

### 1️`FashionEasy_Creation_of_Database.ipynb`  
   - Notebook for creating the database schema.  
   - Defines tables and their relationships based on the entity-relationship diagram.  
   - Initializes constraints like primary keys (PK) and foreign keys (FK).  

### 2️ `FashionEasyFakeDataGen.ipynb`  
   - Generates synthetic data for testing the FashionEasy database.  
   - Populates tables with mock user details, products, vendors, and orders.  

### 3 `Fashioneasy Generated database.db`  
   - The SQLite database file containing the FashionEasy data.  
   - Can be queried using SQL for analysis.  

### 4️ `RAG_FashionEasy.ipynb`  
   - Notebook implementing a **Retrieval-Augmented Generation (RAG)** system.  
   - Enhances user interaction with the database using AI-driven insights.  

### 5️ `Privacy_Enhanced_RAG_System_.ipynb`  
   - Builds on the RAG system with additional privacy enhancements.  
   - Ensures sensitive user information is protected in responses.  

### 6️ `FashionEasyERD.drawio.png`  
   - Entity-Relationship Diagram (ERD) showing database structure.  
   - Provides a visual reference for table relationships.  

---

## Database Schema Overview  
The FashionEasy database consists of the following tables:

### **Users Table**  
Stores customer details.  
- **Attributes:** `user_id`, `user_name`, `email`, `user_country`, `user_zipcode`, `phone_number`.

### **Products Table**  
Maintains product details available in the store.  
- **Attributes:** `product_id`, `vendor_id (FK)`, `price`, `inventory`.

### **Vendors Table**  
Contains details about fashion product suppliers.  
- **Attributes:** `vendor_id`, `vendor_name`, `location`.

### **Orders Table**  
Keeps records of user purchases.  
- **Attributes:** `order_id`, `order_date`, `order_status`, `user_id (FK)`.

### **OrderDetails Table**  
Tracks the products purchased in each order.  
- **Attributes:** `quantity`, `product_id (FK)`, `order_id (FK)`, `delivery_address`.

### **StylingPreferences Table**  
Stores user fashion preferences.  
- **Attributes:** `styling_id`, `preference_details`.

###  **StylingSuggestions Table**  
Links users, products, and styling preferences to generate fashion recommendations.  
- **Attributes:** `styling_suggestion_id`, `user_id (FK)`, `product_id (FK)`, `styling_id (FK)`, `event_details`.

---

##  How to Use This System  

### **1. Setting Up the Database**  
- Run the `FashionEasy_Creation_of_Database.ipynb` notebook to initialize the schema.  
- Execute the SQL scripts in the notebook to create tables.  

### **2. Generating Sample Data**  
- Run `FashionEasyFakeDataGen.ipynb` to populate the tables with test data.  

### **3. Querying the Database**  
- Use SQL queries to extract user preferences, top-selling products, or vendor performance.  

### **4. AI-Enhanced Search with RAG**  
- Utilize `RAG_FashionEasy.ipynb` to retrieve fashion insights using AI.  

###  **5. Enhancing Privacy**  
- Execute `Privacy_Enhanced_RAG_System_.ipynb` to ensure secure user interactions.  

---

## Next Steps  
- Implement a **web-based interface** for customer interaction.  
- Integrate **real-time inventory updates** for vendors.  
- Enhance the RAG system with **personalized AI fashion recommendations**.  

---

## Technologies Used  
- **Database:** SQLite  
- **Backend:** Python (SQLAlchemy, Pandas)  
- **AI Components:** RAG System (Retrieval-Augmented Generation)  
- **Privacy Features:** Data masking and secure retrieval  

#SQL #Python #RAG #LLM #privacy


