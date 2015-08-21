# Angular Directives Challenges

| Objectives |
| :--- |
| Show and hide data with `ng-hide` |
| Filter data in an `ng-repeat` with a custom filter |
| Pluralize words with `ng-pluralize` |
| Insert partial templates with `ng-include` |
| Use `ng-submit` to do validation |

# Challenges

## Base Challenges

For these challenges use your todo app from this morning

1. Pluralize the label of the count of your todos. e.g. "4 Todos"
1. Add an attribute `created_at` to your todos and use the `date` filter to display this time as "posted on Monday April 24, 2015". Hint: use `new Date()`
1. Update your todo form to use an actual `<form>` and `ng-submit`.
1. Require the `todo.title` and disable the button if `todo.title.$invalid`
1. Use a partial and the `ng-include` directive to iterate over your todos.
1. Add an attribute "completed" to each todo.
1. Make a button that when you click it sets the "completed" to true.
1. Use the directive `ng-class` to conditionally set a class that strikes through the todo title and turns the text grey if "completed" is true. Look up the ng-class docs to complete.

## Stretch Challenges

1. Add an attribute to your todos that gives each todo a `kind` (create 2-3 kinds).
  * Add a radio button to your new todo form that allows the user to pick a `kind` of todo.
  * Use `filter` to filter to see only one kind of todos.
  * Add a new form that lets the user add new kinds. Make this new kind available as a radio button on the todo form. 
