# To-Do List Enhancement with React

This project is a simple To-Do List application built with **React**. It allows users to create a list of tasks, mark tasks as completed, toggle between a form view and the to-do list, and delete tasks. The application is built using **React's functional components** and **React hooks** like `useState`.

## Features

- **Add new tasks**: Enter a task name into the form and click the submit button to add it to your to-do list.
- **Mark tasks as complete/incomplete**: You can toggle a task's status by clicking on the checkbox next to each task.
- **Delete tasks**: Easily remove a task from the list by clicking the "Delete" button next to it.
- **Toggle between views**: Switch between the form view (to add tasks) and the list view (to see your tasks).

## Project Structure

### Components

1. **ToDoList Component**:

   - Manages the to-do list and form functionalities.
   - Includes functions to handle adding, toggling completion, deleting, and rendering the list of tasks.
   - Uses React's `useState` to manage form inputs and the to-do list state.

2. **App Component**:
   - The main application component that renders the `ToDoList`.

### CSS

- The application includes basic styling:
  - **Form Styling**: The form has a clean, centered layout.
  - **Completed Tasks**: Completed tasks have a strikethrough effect for visual feedback.
  - **Buttons**: Buttons are styled with a modern look and feel.

## How It Works

1. **State Management**:

   - The component manages the `todos` state, an array that stores the list of tasks.
   - The `newTodo` state stores the current input from the form field.
   - The `toggle` state controls whether the form or the task list is displayed.

2. **Form Submission**:

   - When a user types a new task and submits the form, the task is added to the `todos` array with a unique ID and default status of incomplete.

3. **Mark as Complete**:

   - Each task has a checkbox to mark it as complete or incomplete. When clicked, it toggles the `completed` property of that specific task.

4. **Delete Task**:

   - Each task has a "Delete" button that removes it from the `todos` array.

5. **Toggle View**:
   - A button toggles between the form to add new tasks and the display of the task list.

## Code Breakdown

### ToDoList Component

- `handleChange`: Updates the `newTodo` state with the current input value and assigns a random unique ID to each task.
- `handleSubmit`: Prevents page refresh on form submission, adds the new task to the `todos` array, and clears the input field.
- `handleStatus`: Toggles the `completed` status of a task.
- `handleDelete`: Removes the selected task from the list.
- `handleToggle`: Switches between the form view and the task list view.

### App Component

- The `App` component renders the `ToDoList` component as the primary UI.

## Getting Started

### Prerequisites

- **Node.js** installed on your system.

### Installation

1. Clone the repository or copy the provided code.
2. Create a basic React app using `create-react-app` or add the above code into an existing React project.
3. Open `index.html` in your browser to view the ToDo List, or if using a React app setup, run `npm start`.

### How to Run the App

- **In Browser**:
  - Open the `index.html` file directly in a web browser if using the provided standalone script with CDN links.
- **Using React CLI**:
  1. Install dependencies (if applicable):
     ```bash
     npm install
     ```
  2. Start the development server:
     ```bash
     npm start
     ```

## Built With

- **React**: JavaScript library for building user interfaces.
- **Babel**: JavaScript compiler for JSX transformation in the browser (if using standalone HTML + CDN).
