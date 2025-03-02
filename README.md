# Task Management GraphQL API


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


