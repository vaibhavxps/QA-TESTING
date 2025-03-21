# API Testing and Automation Using Python

### **Objective**:
This report outlines the process of using **Postman** for manual API testing and how I automated the testing process using **Python**. The goal is to ensure that the APIs are functioning correctly and to streamline the process through automated testing.

---

### **Step 1: Manual API Testing with Postman**

**Postman** is a tool that allows testing APIs manually. It helps ensure that the API is working correctly and can provide useful information like response codes and response bodies.

#### **1.1 Creating a Request in Postman**:
1. Open **Postman**.
2. Select the appropriate **HTTP method** (GET, POST, PUT, DELETE, etc.).
3. Enter the **API URL** (for example: `https://jsonplaceholder.typicode.com/posts`).
4. Click **Send** to initiate the request.

#### **1.2 Reviewing the Response**:
Once the request is made, I check the response:
- **Status code**: Ensure it is `200 OK` or the expected status code.
- **Response body**: Verify the content to check if it returns the expected data format (like JSON).
- **Response time**: Check if the response time is acceptable.

---

### **Step 2: Automating API Tests Using Python**

To automate the API testing process, I used **Python** with the `requests` library. This approach ensures that we can easily validate the API automatically in the future.

#### **2.1 Installing Required Libraries**:
To get started with Python, I installed the `requests` library. This is necessary to send HTTP requests and handle responses:



## 2.2 Writing the Test Script:

Below is a simple Python script I wrote that sends a GET request to an API and verifies if the response status code is 200 OK:

```python
import requests

# API URL to test
url = 'https://jsonplaceholder.typicode.com/posts'

# Send GET request to the API
response = requests.get(url)

# Check if the status code is 200 (OK)
if response.status_code == 200:
    print("Test Passed! Status code is 200.")
else:
    print("Test Failed! Status code:", response.status_code)

# Check if the response contains a list of posts
try:
    data = response.json()
    if isinstance(data, list):
        print("Test Passed! The response contains a list of posts.")
    else:
        print("Test Failed! The response is not a list.")
except Exception as e:
    print(f"Test Failed! Error parsing the response: {e}")
## 2.3 Running the Test:

To run the test:

1. Save the Python script (e.g., as `api_test.py`).
2. Open the terminal or command prompt.
3. Execute the script using Python:

    ```bash
    python api_test.py
    ```

The script checks if the status code is `200 OK` and whether the response body is a list (since the API returns a list of posts).

---

## Step 3: Automating the Testing in CI/CD Pipeline

In the future, I plan to integrate the Python test script into our **CI/CD pipeline** (such as Jenkins, GitLab CI, or GitHub Actions). This will allow the test to run automatically every time there is a change or update in the API, ensuring continuous validation.

### Steps to Automate Testing in CI/CD:

1. Add the **Python test script** to the project repository.
2. Set up a **CI/CD tool** (such as Jenkins or GitHub Actions) to run the Python script automatically as part of the build process.
3. If the test fails, the pipeline will stop, and notifications will be sent so issues can be addressed immediately.

---

## Conclusion

In this process, I:

- Used **Postman** for manual testing to quickly verify the API responses.
- Automated the tests using **Python** and the `requests` library for easy repeatability.
- Explored how to integrate the tests into a **CI/CD pipeline** for continuous testing and faster feedback.

This automation will help ensure that the APIs continue to work as expected and will help in identifying issues faster during development.

