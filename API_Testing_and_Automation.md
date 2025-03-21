# API Testing and Automation Using Python

### **Objective**:
In this report, I’m outlining how I’ve used **Postman** for manual API testing and how I’ve automated the testing process using **Python**. The goal was to ensure that the APIs are working correctly and that we can easily run automated tests as part of our continuous integration process.

---

### **Step 1: Manual API Testing with Postman**

**Postman** is a tool I used to manually test the API endpoints. 

#### **1.1 Creating a Request in Postman**:
1. I opened **Postman** and selected the appropriate **HTTP method** (GET, POST, etc.).
2. I entered the **API URL** (for example: `https://jsonplaceholder.typicode.com/posts`).
3. I clicked **Send** to make the request to the API.

#### **1.2 Reviewing the Response**:
After sending the request, I checked the **response status code** (like `200 OK`) and the **response body** to ensure the API was working as expected. If the status code was not `200`, I investigated the issue further.

---

### **Step 2: Automating API Tests Using Python**

I wanted to automate the API testing process, so I used **Python** along with the `requests` library to send API requests and validate responses.

#### **2.1 Installing Required Libraries**:
To get started with Python, I installed the `requests` library by running:

```bash
pip install requests
