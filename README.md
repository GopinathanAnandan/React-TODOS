# React Todo Task:

In this task, I created the simple Todo application using React. In this task, the todos created in the todo forms are displayed on cards. Each card contains a name, description, status (completed or not completed), a button to change the status, an edit button to edit the particular card, and a delete button to delete the card. This card is viewed by filtering the status, like (all, completed, and not completed).

# Components:

<ul>
  <li>TodoForm</li>
  <li>FilterTodos</li>
  <li>TodoList</li>
</ul>

# App.jsx:

<ul>
  <li>It uses useState hooks to manage three pieces of state:</li>
  <ul>
    <li>todos: An array containing all the todo items.</li>
    <li>filteredTodos: An array that holds the currently displayed todos based on the filter selected.</li>
    <li>nextId: An integer used to generate unique IDs for new todos.</li>
  </ul>
  <li>It defines several functions:</li>
  <ul>
    <li>addTodo: Adds a new todo item to the todos array.</li>
    <li>updateTodoStatus: Updates the status (completed/not completed) of a todo item.</li>
    <li>deleteTodo: Removes a todo item from the todos array.</li>
    <li>handleFilterChange: Updates the filteredTodos array based on the selected filter (all, completed, not completed).</li>
  </ul>
  <li>It renders the TodoForm component for adding new todos, the FilterTodos component for filtering the list, and the TodoList component to display and manage existing todos.</li>
</ul>

# TodoForm.jsx:

<ul>
  <li>This component defines the form for adding a new todo item.</li>
  <li>It uses useState hooks to manage the name, description, and any error messages for user input.</li>
  <li>The handleSubmit function validates the input and adds a new todo object to the todos array through the addTodo prop passed from App component.</li>
</ul>

# FilterTodos.jsx:

<ul>
  <li>This component provides a dropdown menu for filtering the displayed todos.</li>
  <li>It allows users to choose between seeing all todos, completed todos, or not-completed todos.</li>
  <li>When the selection changes, it triggers the handleFilterChange function in App component with the chosen filter value.</li>
</ul>

# TodoList.jsx:

<ul>
  <li>This component displays the list of todos and handles editing functionalities.</li>
  <li>It maintains its own state using useState hooks to track the currently edited todo's ID and its edited data (name and description).</li>
  <li>It renders each todo item with its name, description, status, and buttons for editing, marking as completed/not completed, and deleting.</li>
  <li>It defines functions for handling user interactions:</li>
  <ul>
    <li>handleStatusChange: Updates the status of a todo through the updateTodoStatus prop from App component.</li>
    <li>handleDelete: Deletes a todo using the deleteTodo prop from App component.</li>
    <li>handleEdit: Sets up the edit form with the selected todo's data.</li>
    <li>handleEditInputChange: Updates the edited data as the user types in the edit form.</li>
    <li>handleEditSubmit: Saves the edited todo data by updating the original todo object in the todos array.</li>
    <li>handleCancelEdit: Cancels the edit mode and resets the editing state.</li>
  </ul>
  <li>It conditionally renders the todo item details based on the editing state.</li>
</ul>

# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh
