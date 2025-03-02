# Sample GraphQL Queries

## 1. Get All Tasks

```graphql
query GetAllTasks {
  tasks {
    id
    title
    description
    completed
    duration
  }
}
```

## 2. Get a Single Task

```graphql
query GetTask {
  task(id: "1") {
    id
    title
    description
    completed
    duration
  }
}
```

## 3. Add a New Task

```graphql
mutation AddNewTask {
  addTask(
    title: "Implementation of GraphQL API"
    description: "Create a GraphQL API with Node.js, Express, and Apollo Server"
    completed: false
    duration: 3
  ) {
    id
    title
    description
    completed
    duration
  }
}
```

## 4. Complete a Task

```graphql
mutation MarkTaskAsComplete {
  completeTask(id: "1") {
    id
    title
    completed
  }
}
```

## 5. Change Task Description

```graphql
mutation UpdateTaskDescription {
  changeDescription(
    id: "2"
    description: "Updated description for the authentication system"
  ) {
    id
    title
    description
  }
}
```

## 6. Delete a Task

```graphql
mutation RemoveTask {
  deleteTask(id: "3")
}
```
