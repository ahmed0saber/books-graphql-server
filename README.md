# Books GraphQL Server

A GraphQL server to handle CRUD operations for books and authors. The server has been developed with Express.js and GraphQL.js!

## Add New Book

```
mutation {
  addBook(name: "extends ahmed0saber", authorId: 4) {
    id,
    name,
    authorId
  }
}
```

## Add New Author

```
mutation {
  addAuthor(name: "ahmed0saber") {
    id,
    name,
  }
}
```

## Get All Books

```
{
  books {
    id
    name
    authorId
    author {
      id
      name
    }
  }
}
```

## Get All Authors

```
{
  authors {
    id
    name
    books {
      id
      name
    }
  }
}
```

## Get Book By Id

```
{
  book(id: 1) {
    name
    author {
      id
      name
    }
  }
}
```

## Get Author By Id

```
{
  author(id: 1) {
    name
    books {
      id
      name
    }
  }
}
```

### Example Request

```
http://localhost:3000/graphql?query=%7B%0A%20%20author(id%3A%201)%20%7B%0A%20%20%20%20name%0A%20%20%20%20books%20%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%20%20name%0A%20%20%20%20%7D%0A%20%20%7D%0A%7D
```

## Keep Learning

The following resources can be helpful if you want to learn how to set up your own GraphQL server.

- https://www.youtube.com/watch?v=ZQL7tL2S0oQ
- https://graphql.org/graphql-js/running-an-express-graphql-server/
- https://dev.to/codesphere/how-to-build-a-graphql-server-with-nodejs-and-express-2g8j
- https://snipcart.com/blog/graphql-nodejs-express-tutorial
