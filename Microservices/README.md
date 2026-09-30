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

![alt text](<Screenshot 2026-09-29 at 5.39.54 PM.png>)

- **Products:**

```
  curl http://localhost:3003/api/products
  curl http://localhost:3003/api/products
  [{"id":1,"name":"Laptop","price":999},{"id":2,"name":"Phone","price":699}]%
```

![alt text](<Screenshot 2026-09-29 at 5.40.26 PM.png>)

- **Orders:**

  ```
  curl http://localhost:3003/api/orders
  curl http://localhost:3003/api/orders
  []%
  ```

  ![alt text](<Screenshot 2026-09-29 at 5.41.00 PM.png>)

---

## Instructions

1. Start all services using the `docker-compose` file:

```
docker-compose up -d --build
```

![alt text](<Screenshot 2026-09-29 at 4.50.12 PM.png>)

2. Once the services are running, use the above endpoints to verify the functionality.

![alt text](<docker compose ps at 6.04.38 PM-1.png>)

![alt text](<docker compose logs order-service 6.04.46 PM.png>)

![alt text](<docker compose logs user service 6.05.03 PM.png>)

![alt text](<docker comose logs product-service 6.05.28 PM.png>)

Run docker compose exec gateway-service sh and then run
wget -qO- http://product-service:3001/products
wget -qO- http://user-service:3000/users
wget -qO- http://order-service:3002/orders

![alt text](<Product Service 10.29.31 AM-1.png>)
![alt text](<user service 10.29.03 AM.png>)
![alt text](<Order Service 10.30.11 AM.png>)

```

```
