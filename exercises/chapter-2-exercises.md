# Chapter 2: How the Web and APIs Work
## Theory Exercises

These exercises demonstrate my understanding of HTTP methods, HTTP status codes, API requests, responses, authentication, authorization, and HTTP headers.

---

## Exercise 1: Employee Registration and Retrieval
**Level:** Guided

### Scenario
A government institution uses an API to register and retrieve employee information.

### Tasks and Learning Outcomes

1. **POST:** Used to submit employee information and create a new resource.
2. **Request body:** Contains the employee information in JSON format.
3. **201 Created:** Confirms that a new resource was successfully created.
4. **Content-Type:** Identifies the format of the response body, such as application/json.
5. **Location:** Identifies the newly created resource, for example `/api/employees/105`.
6. **GET:** Retrieves an existing employee resource.
7. **200 OK:** Confirms that the retrieval request succeeded.

---

## Exercise 2: Employee Update and Access Control
**Level:** Semi-guided

### Scenario
An administrator updates an employee's department using PATCH.

### Tasks and Learning Outcomes

1. **PATCH:** Updates part of an existing resource.
2. **401 Unauthorized:** Occurs when authentication credentials are missing or invalid.
3. **403 Forbidden:** Occurs when the server has authenticated the user, but the user lacks the required permission.
4. **Authorization header:** Carries credentials, such as a bearer token, used to authenticate the request and evaluate access rights.
5. **200 OK:** Confirms that the update succeeded and a response body was returned.
6. **201 Created:** Is not normally used when updating an existing resource without creating another resource.

---

## Exercise 3: Employee Deletion and HTTP Headers
**Level:** Independent

### Scenario
An administrator requests deletion of an employee record.

### Tasks and Learning Outcomes

1. **DELETE:** Requests removal of a resource.
2. **204 No Content:** Confirms that the request succeeded without returning response content.
3. **Response body:** A 204 response does not contain a response body.
4. **Date header:** Indicates when the response was generated.
5. **Cache-Control: no-store:** Instructs caches not to store the response.
6. **Cache-Control: max-age=600:** Allows a cached response to be reused while fresh for 600 seconds (10 minutes).

---

## Key Concepts Strengthened

- Difference between HTTP request and HTTP response.
- Difference between Content-Type and Accept headers.
- Difference between 401 Unauthorized and 403 Forbidden.
- Difference between 200 OK, 201 Created, and 204 No Content.
- Purpose of the Location header.
- Purpose of Authorization and Cache-Control headers.
- Difference between cache freshness duration and server response time.

---

## Learning Reflection

These exercises helped strengthen my understanding of how clients communicate with servers through HTTP and APIs.

I practised reasoning through realistic employee-management scenarios relevant to government ICT systems.

**Next:** Three Python practical exercises involving API requests, JSON data, HTTP responses, and error handling.
