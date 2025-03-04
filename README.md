# api-tester
The API Tester web app will serve as a tool to test and debug various API endpoints. You’ll build a user interface where you can input API endpoints, set HTTP methods, headers, and body parameters, and then view the responses in a formatted manner.

## Project Breakdown
### Define Scope & Set Up Project

Goals:

    Define the features and user flows for the API Tester.
    Set up the project structure and install required dependencies.

Tasks:

    Outline the core features:
        User interface to input API endpoint, HTTP method, headers, and body.
        Display API response status, headers, and body in a readable format.
        Optionally, support saving and organizing past tests.
    Sketch a UI wireframe showing:
        A form for API request input.
        A display area for API responses.
    Set up the project folder structure:

    /api-tester
      ├── /templates        // HTML templates
      ├── /static           // CSS/JS files
      ├── main.go
      ├── routes.go
      ├── handlers.go
      └── db.go

    Initialize with go mod init api-tester and install dependencies (Gin, Resty, Testify, godotenv).

📌 Deliverable: Project is initialized with a clear scope, wireframe, and folder structure.

### Build the Core API Testing Interface

Goals:

    Develop the frontend form for API request inputs.
    Create the basic backend endpoint to receive and process these requests.

Tasks:

    Create HTML templates using html/template:
        A form to input API endpoint, select HTTP method, and add headers/body.
    In routes.go, set up an endpoint (e.g., POST /test) to accept form submissions.
    In the handler, capture the input data and prepare to make an API request.
    Use simple CSS to style the form for clarity and ease-of-use.

📌 Deliverable: A basic, functional form for inputting API request parameters.

### Implement API Request Functionality

Goals:

    Use Resty to make API calls based on user input.
    Process and format the response.

Tasks:

    Write a function that takes the API endpoint, method, headers, and body, and then makes an HTTP request using Resty.
    Capture the response status, headers, and body.
    Handle errors and timeouts gracefully.
    Return the processed response to the frontend.

📌 Deliverable: A function that successfully makes API calls and returns a formatted response.

### Integrate Frontend & Display API Responses

Goals:

    Connect the backend API request function to the frontend.
    Dynamically display the API response on the web page.

Tasks:

    Update the HTML template to include a section for displaying the API response.
    Modify the backend handler to pass the API response data to the template.
    Use Go’s template syntax to render the response status, headers, and body.
    Ensure the UI is clean and easy to read.

📌 Deliverable: Users can submit API requests through the form and see formatted responses on the page.

### Add Advanced Features & User Feedback

Goals:

    Enhance the API Tester with additional functionalities and improve usability.

Tasks:

    Add support for:
        Saving past API requests and responses.
        Optionally, a history panel to quickly re-run previous tests.
    Implement input validation and user-friendly error messages.
    Optimize the UI to ensure responsiveness and clarity.
    Collect feedback on what additional features might be useful (e.g., via a simple poll on your social channels).

📌 Deliverable: An enhanced UI with additional interactive features that improve user experience.

### Testing, Debugging & Unit Testing

Goals:

    Thoroughly test the API Tester application.
    Write unit tests for your API request function using Testify.

Tasks:

    Manually test various API calls (successful, failing, timeout scenarios).
    Use Postman or similar tools for additional testing.
    Write unit tests to verify the correctness of your API request handling and error processing.
    Debug and resolve any issues that arise.

📌 Deliverable: A robust, well-tested application with unit tests demonstrating API call reliability.

### Final Testing, Documentation & Deployment

Goals:

    Finalize the application, polish documentation, and deploy the project online.

Tasks:

    Perform end-to-end testing of the entire workflow.
    Update the README and documentation with setup, usage, and troubleshooting guides.
    Use godotenv to manage environment variables (API keys, etc.).
    Deploy the app on a platform such as Railway, Heroku, or Fly.io.

📌 Deliverable: The API Tester is live, fully documented, and ready to be showcased in your portfolio.
