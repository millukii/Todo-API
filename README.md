# API TODOS Graphql, Mongo db and Golang
 
 # Generate & Run
- go generate ./...
  go run server.go
- go navitor at http://localhost:8080/ to play the queries
# Queries

mutation createTodo {
  createTodo(input: { text: "todo", userId: "1" }) {
    user {
      id
    }
    text
    done
  }
}

query Todos {
  todos {
    text
    done
    user {
      name
    }
  }
}


query Todo {
  todo(_id: "621ad78a9ddd75aabe73a10e") {
    text
    done
    user {
      name
    }
  }
}
