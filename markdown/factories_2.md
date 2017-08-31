```js
function todoService() {
    var todos = [];

    var service = {
        getTodos: getTodos,
        addTodo: addTodo
    };

    return service;

    function getTodos() {
        return todos;
    }

    function addTodo(todo) {
        todos.push(todo);
        return todos;
    }
}
```
