---

## **PROGRAM 6 – Servlet-Based Controller for Shopping Cart**

---

### **AIM**

To design a **Java Servlet controller** that connects the front-end shopping cart application with a **MySQL database**, using the **MVC architecture** pattern.

---

### **DESCRIPTION**

This experiment integrates a web-based shopping cart interface with a backend **MySQL database** using a **Java Servlet**. The servlet (controller) handles **HTTP requests**, connects to the database, retrieves product data, and sends it back to the client as a **dynamic HTML response**.

The application showcases a basic **MVC structure** using:

* **HTML** (View)
* **Servlet** (Controller)
* **MySQL** (Model)

The project is developed and run using **VS Code**, compiled with the **Servlet API**, and deployed on **Apache Tomcat**.

---

### **PROJECT STRUCTURE**

```
shopping-cart/
│
├── src/
│   └── servlets/
│       └── ProductServlet.java         # Servlet controller to handle /products
│
├── WebContent/
│   ├── index.html                      # Home page with canvas UI
│   ├── catalog.html                    # Catalog page with canvas + product loading link
│   └── WEB-INF/
│       ├── web.xml                     # Servlet configuration and routing
│       └── lib/
│           └── mysql-connector-j-9.3.0.jar
│
├── bin/                                # Compiled .class files
├── lib/
│   └── javax.servlet-api-4.0.1.jar
├── README.md                           # Project documentation
```

---

### **INSTALLATION & SETUP**

#### **PREREQUISITES**

• Java JDK

• Apache Tomcat

• MySQL

• VS Code with Java Extension Pack

• Servlet API (`javax.servlet-api-4.0.1.jar`)

---

### **STEPS TO RUN THE PROJECT**

1. **Place Required JARs**
   Copy the following files to your `lib/` folder:

   * `mysql-connector-j-9.3.0.jar`
   * `javax.servlet-api-4.0.1.jar`

2. **Compile Servlet**

   ```bash
   javac -cp "lib/*" -d bin src/servlets/ProductServlet.java
   ```

3. **Deploy to Apache Tomcat**

   * Copy `WebContent/` to `tomcat/webapps/shopping-cart/`
   * Copy compiled `bin/` classes to `WEB-INF/classes/`

4. **Start Tomcat Server**

5. **Visit in Browser**

   ```
   http://localhost:8080/shopping-cart/index.html
   ```

---

### **DATABASE SETUP**

**Database:** `shopping_cart`
**Table:** `products`

```sql
CREATE TABLE products (
  id INT PRIMARY KEY AUTO_INCREMENT,
  name VARCHAR(100),
  price DECIMAL(10,2)
);

```

---

### **LICENSE**

This project is **open-source** and free to use.

---

### **Author**

• **Mohammad Nowfa**

• GitHub: [https://github.com/nowfamohammad04](https://github.com/nowfamohammad04)

---
