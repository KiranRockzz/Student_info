# Student_info

# Student Server Assignment

This project sets up a basic Node.js HTTP server that returns student data based on the provided student ID.

## How to Run

1. Ensure Node.js is installed on your machine.
2. Clone the repository:

    ```sh
    git clone https://github.com/kakumanupraveen/student-server-assignment.git
    cd student-server-assignment
    ```

3. Start the server:

    ```sh
    node server.js
    ```

4. Access the server with a web browser or a tool like `curl`. For example:

    ```sh
    curl http://localhost:8000/?student_id=11111
    ```

## Functionality Overview

1. **Module Imports:**
    - **http:** Utilized to create an HTTP server.
    - **url:** Used for parsing URLs and query parameters.

2. **Student Data Definition:**
    - Contains an object with predefined student information, including IDs, names, and scores.

3. **HTTP Server Creation:**
    - The server listens for incoming HTTP requests.
    - Extracts the `student_id` from the query parameters of the request URL.
    - Checks if the `student_id` is present in the predefined student data.
    - If the ID is found, responds with the relevant student information in JSON format.
    - If the ID is not found, responds with a 404 status code and a JSON error message.

4. **Server Initialization:**
    - The server starts listening on port 8000 and logs a message to the console upon starting.

## Integration with Project

1. **Retrieving Student Information:**
    - This script allows fetching student details through an HTTP GET request by providing a `student_id` query parameter.
    - Example: Accessing `http://localhost:8000/?student_id=11111` will return the information for Bruce Lee.

2. **Handling Errors:**
    - Ensures that if a student ID does not exist, the server responds appropriately with a 404 status and a JSON error message.
