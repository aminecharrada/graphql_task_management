# Task Management GraphQL API

This project is a **Task Management API** built using **Node.js**, **Express**, and **Apollo Server** with **GraphQL**. The API allows users to manage tasks, including adding, retrieving, updating, completing, and deleting tasks.

---

## 📂 Project Structure

```
/project-root
│
├── taskSchema.gql            # GraphQL Schema Definition
├── taskSchema.js              # Loads and builds schema from taskSchema.gql
├── taskResolver.js            # Resolvers defining business logic for GraphQL operations
├── server.js                   # Main Express server integrating Apollo GraphQL
├── README.md                   # Documentation (this file)
└── package.json                # Node dependencies
```

---

## 📋 Features

- Retrieve all tasks
- Retrieve a single task by ID
- Add new tasks
- Update task descriptions
- Mark tasks as completed
- Delete tasks

---

## 🚀 Installation

1. Clone this repository:
    ```bash
    git clone <repository-url>
    cd <project-folder>
    ```

2. Install dependencies:
    ```bash
    npm install
    ```

3. Start the server:
    ```bash
    npm start
    ```

4. The GraphQL Playground will be available at:
    ```
    http://localhost:4000/graphql
    ```

---

## 📚 GraphQL Schema

### Task Type

```graphql
type Task {
  id: ID!
  title: String!
  description: String!
  completed: Boolean!
  duration: Int
}
```

### Queries

```graphql
type Query {
  task(id: ID!): Task
  tasks: [Task]
}
```

### Mutations

```graphql
type Mutation {
  addTask(title: String!, description: String!, completed: Boolean!, duration: Int): Task
  completeTask(id: ID!): Task
  changeDescription(id: ID!, description: String!): Task
  deleteTask(id: ID!): Boolean
}
```

---

## 📌 Sample GraphQL Queries & Mutations

### 1. Get All Tasks
```graphql
query {
  tasks {
    id
    title
    description
    completed
    duration
  }
}
```

### 2. Get a Single Task
```graphql
query {
  task(id: "1") {
    id
    title
    description
    completed
    duration
  }
}
```

### 3. Add New Task
```graphql
mutation {
  addTask(
    title: "Build a GraphQL API"
    description: "Create a basic API using Node.js, Express, and Apollo Server"
    completed: false
    duration: 5
  ) {
    id
    title
    description
    completed
    duration
  }
}
```

### 4. Mark Task as Completed
```graphql
mutation {
  completeTask(id: "1") {
    id
    title
    completed
  }
}
```

### 5. Update Task Description
```graphql
mutation {
  changeDescription(id: "2", description: "Updated description for task 2") {
    id
    title
    description
  }
}
```

### 6. Delete a Task
```graphql
mutation {
  deleteTask(id: "3")
}
```

---

## ⚙️ Technologies Used

- **Node.js** - Backend runtime
- **Express** - Web framework
- **Apollo Server** - GraphQL server
- **GraphQL Tools** - Schema and resolvers management
- **body-parser** - Parse incoming request bodies
- **graphql** - GraphQL query language

---

## 📄 How the Project Works

1. **Schema Definition (`taskSchema.gql`)**  
   Defines types, queries, and mutations for the task management system.
2. **Resolvers (`taskResolver.js`)**  
   Implements the logic for each query and mutation using an in-memory array (`tasks`).
3. **Schema Loader (`taskSchema.js`)**  
   Loads the schema from `taskSchema.gql` and builds it into a GraphQL executable schema.
4. **Server (`server.js`)**  
   Combines Express with Apollo Server to expose the `/graphql` endpoint.

---

## 📝 Example Task Data

```json
[
  {
    "id": "1",
    "title": "Développement Front-end pour Site E-commerce",
    "description": "Créer une interface utilisateur réactive en utilisant React et Redux pour un site e-commerce.",
    "completed": false,
    "duration": 14
  },
  {
    "id": "2",
    "title": "Développement Back-end pour Authentification Utilisateur",
    "description": "Implémenter un système d'authentification et d'autorisation pour une application web en utilisant Node.js, Express, et Passport.js.",
    "completed": false,
    "duration": 7
  },
  {
    "id": "3",
    "title": "Tests et Assurance Qualité pour Application Web",
    "description": "Développer et exécuter des plans de test et des cas de test complets.",
    "completed": false,
    "duration": 5
  }
]
```

---

## 🔧 Environment Variables (Optional)

You can set the server port using:
```
PORT=4000
```

---

## 🧰 Running the Project with Nodemon (Optional)

To enable auto-restart during development, install nodemon:
```bash
npm install -g nodemon
```
Then run:
```bash
nodemon server.js
```

---

## 🏁 Future Enhancements

- Persist tasks to a database (MongoDB, PostgreSQL, etc.)
- Add user authentication and authorization
- Add more advanced filtering and sorting capabilities
- Implement unit and integration tests


