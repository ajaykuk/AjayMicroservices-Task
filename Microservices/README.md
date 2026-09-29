# Microservices-Task

## Overview

This document provides details on testing various services after running the `docker-compose` file. These services include User, Product, Order, and Gateway Services. Each service has its own endpoints for testing purposes.

---

## Services and Endpoints

### **User Service**

- **Base URL:** `http://localhost:3000`
- **Endpoints:**
  - **List Users:**  
     `    curl http://localhost:3000/users`
    Or open in your browser: [http://localhost:3000/users](http://localhost:3000/users)

        curl http://localhost:3000/users

    [{"id":1,"name":"John Doe"},{"id":2,"name":"Jane Smith"}]%

![alt text](<Screenshot 2026-09-29 at 5.36.00 PM.png>)

---

### **Product Service**

- **Base URL:** `http://localhost:3001`
- **Endpoints:**
  - **List Products:**

    ```
    curl http://localhost:3001/products
    ```

    Or open in your browser: [http://localhost:3001/products](http://localhost:3001/products)

    [{"id":1,"name":"Laptop","price":999},{"id":2,"name":"Phone","price":699}]%

    ![alt text](<Screenshot 2026-09-29 at 5.37.45 PM.png>)

---

### **Order Service**

- **Base URL:** `http://localhost:3002`
- **Endpoints:**
  - **List Orders:**

    ```
    curl http://localhost:3002/orders
    ```

    Or open in your browser: [http://localhost:3002/orders](http://localhost:3002/orders)
    EMPTY RESPONSE FOR ..3002/orders--> []%

    ![alt text](<Screenshot 2026-09-29 at 5.39.07 PM.png>)

---

### **Gateway Service**

- **Base URL:** `http://localhost:3003/api`
- **Endpoints:**
  - **Users:**

    ```
    curl http://localhost:3003/api/users

       ajaymalik@Ajays-MacBook-Pro Microservices % curl http://localhost:3003/api/users

    [{"id":1,"name":"John Doe"},{"id":2,"name":"Jane Smith"}]%
    ```

  - **Products:**

    ````
    curl http://localhost:3003/api/products
    curl http://localhost:3003/api/products
    [{"id":1,"name":"Laptop","price":999},{"id":2,"name":"Phone","price":699}]%

       ```
    ````

ajaymalik@Ajays-MacBook-Pro Microservices %

- **Orders:**

  ````
  curl http://localhost:3003/api/orders
  curl http://localhost:3003/api/orders
  []%

     ```
  ````

---

## Instructions

1. Start all services using the `docker-compose` file:
   ```
   docker-compose up -d --build
   ```
2. Once the services are running, use the above endpoints to verify the functionality.

Happy testing!
