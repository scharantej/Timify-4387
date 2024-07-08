## Flask Application Design for Smart Time

### HTML Files

- **index.html**:
    - Main page of the application.
    - Contains the user interface for creating and managing tasks.
    - Includes fields for task name, description, due date, time slot, and priority.
- **schedule.html**:
    - Displays the user's personalized schedule.
    - Shows all tasks and their assigned time slots.
    - Allows for dragging and dropping tasks to adjust the schedule.

### Routes

**GET Routes:**

- **"/index"**: Renders the index.html page.
- **"/schedule"**: Renders the schedule.html page.

**POST Routes:**

- **"/add_task"**: Receives data from the index.html page when a new task is created.
    - Parses the data and adds the task to a database.
    - Generates a time slot for the task using the Smart Time algorithm.
    - Redirects to the index.html page.

- **"/update_schedule"**: Receives data from the schedule.html page when a task is moved or rescheduled.
    - Parses the data and updates the task's time slot in the database.
    - Returns a JSON response with the updated schedule.

**Other Route:**

- **"/logout"**: Logs out the user and redirects to the login page (not specified in the problem). Can be included for user authentication if necessary.