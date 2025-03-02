# GraphQL Task Management API

A simple task management API built with GraphQL, Apollo Server, Node.js, and Express. This project demonstrates how to create and use a GraphQL API for managing tasks.

## Project Overview

This API allows you to:

- View all tasks or a specific task by ID
- Add new tasks with title, description, completion status, and duration
- Mark tasks as completed
- Update task descriptions
- Delete tasks

## Technologies Used

- **Node.js**: JavaScript runtime
- **Express**: Web application framework
- **GraphQL**: Query language for APIs
- **Apollo Server**: GraphQL server implementation
- **@graphql-tools/schema**: Tools for manipulating GraphQL schemas

## Project Structure

- `index.js`: Main server file that configures Apollo Server with Express
- `taskSchema.gql`: GraphQL schema definition file
- `taskSchema.js`: JavaScript module that loads the GraphQL schema
- `taskResolver.js`: Contains the resolver functions for GraphQL queries and mutations
- `sample-queries.md`: Example queries to test the GraphQL API

## Task Model

Each task in the system has the following properties:

- `id`: Unique identifier for the task
- `title`: Task title
- `description`: Detailed description of the task
- `completed`: Boolean indicating whether the task is completed
- `duration`: Time in days estimated to complete the task (integer)

## GraphQL Operations

### Queries

- `task(id: ID!)`: Get a specific task by ID
- `tasks`: Get all tasks

### Mutations

- `addTask`: Create a new task
- `completeTask`: Mark a task as completed
- `changeDescription`: Update a task's description
- `deleteTask`: Remove a task by ID

## Getting Started

1. Install dependencies:

   ```
   npm install
   ```

2. Start the server:

   ```
   npm start
   ```

3. Open your browser and navigate to:

   ```
   http://localhost:5000/graphql
   ```

4. Use the Apollo Studio interface to test the API with the provided sample queries.

## Sample Queries

Check the `sample-queries.md` file for example queries and mutations you can run in Apollo Studio.

## Educational Purpose

This project was created as a learning resource for understanding how to:

- Configure GraphQL with Node.js and Express
- Create GraphQL schemas and resolvers
- Handle queries and mutations in a GraphQL API
- Structure a simple task management application
