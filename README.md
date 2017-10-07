# graphql-go-demo
A demo show for graphql in go ， supported graphiql tools to debug api and got any documents help！Very cool ，right？

# Go GraphQL ToDo example

An example that consists of basic core GraphQL queries and mutations.

Run the example, it will spawn a GraphQL HTTP endpoint

```
glide install
go run main.go
```

Execute queries via shell.

```
//This url will be show graphiQL tool and docs 
http://localhost:8080/graphql

// To get single ToDo item by ID
curl -g 'http://localhost:8080/graphql?query={todo(id:"b"){id,text,done}}'

// To create a ToDo item
curl -g 'http://localhost:8080/graphql?query=mutation+_{createTodo(text:"My+new+todo"){id,text,done}}'

// To get a list of ToDo items
curl -g 'http://localhost:8080/graphql?query={todoList{id,text,done}}'

// To update a ToDo
curl -g 'http://localhost:8080/graphql?query=mutation+_{updateTodo(id:"b",text:"My+new+todo+updated",done:true){id,text,done}}'

```

## Web App

Access the web app at `http://localhost:8080/`. It is work in progress and currently is simply loading todos by using jQuery ajax call.
