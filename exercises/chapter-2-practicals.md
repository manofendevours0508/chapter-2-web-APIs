# Chapter 2: How the Web and APIs Work

## Practical Exercises

### Practical 1: GET Requests

**Objective:** Retrieve information from an API using Python.

**Tools:** Python, Requests library, JSONPlaceholder API, JupyterLab.

Example:

```python
import requests

url = "https://jsonplaceholder.typicode.com/users/5"

response = requests.get(url)

print(response.status_code)

data = response.json()

print(data)
```

**Key concepts learned:**

- `requests.get()` sends a GET request to an API endpoint.
- `response` stores the HTTP Response object.
- `response.status_code` checks the HTTP status code.
- `200 OK` indicates a successful GET request.
- `response.json()` converts a JSON response body into Python objects.
- JSON objects become Python dictionaries, while JSON arrays become Python lists.
- Dictionary keys allow us to retrieve specific information.
- Nested dictionaries allow us to access information within other dictionaries.

Example of retrieving specific information:

```python
print(data["name"])
print(data["email"])
print(data["address"]["city"])
print(data["company"]["name"])
```

### Practical 2: POST Requests

**Objective:** Submit information to an API using Python.

Example:

```python
import requests

employee = {
    "name": "John",
    "email": "john@gmail.com",
    "department": "ICT"
}

url = "https://jsonplaceholder.typicode.com/users"

response = requests.post(url, json=employee)

print(response.status_code)
print(response.json())
```

**Key concepts learned:**

- `requests.post()` sends information to an API.
- `json=employee` sends the Python dictionary as JSON in the request body.
- The request body contains the information sent to the server.
- `Content-Type: application/json` identifies the request body's format.
- `201 Created` indicates successful resource creation.
- The response body contains information returned by the server.
- A server may assign a unique ID to a newly created resource.
- `400 Bad Request` indicates that the request contains invalid or improperly formatted information.

**Practical observation:**

JSONPlaceholder returned the submitted employee information together with an assigned ID. This is a simulated creation; JSONPlaceholder does not permanently store the new record.

### Learning Outcome

Successfully practised retrieving and submitting API data using Python's Requests library, inspecting HTTP status codes, interpreting JSON responses, and accessing specific information from Python dictionaries.
