# Angular Resource

> Adapted from [Sitepoint](http://www.sitepoint.com/creating-crud-app-minutes-angulars-resource/)

Built on the top of the `$http` service, Angular’s `$resource` is a service that lets you interact with RESTful backends easily. `$resource` is very similar to models in Rails. In this tutorial, we're going to make use of a book API that can be found here: `http://daretodiscover.herokuapp.com/books`

## Installation
1. The `$resource` service doesn’t come bundled with the main Angular script. Add it to your `index.html` file.
```html
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.3.14/angular-resource.min.js"></script>
```

1. Now you need to load the `$resource` module into your application.
```js
angular.module('app', ['ngResource']);
```

## Interacting with the API
1. To use `$resource` inside your controller/service you need to declare a dependency on `$resource`. The next step is calling the `$resource()` function with your REST endpoint, as shown in the following example. This function call returns a `$resource` class representation which can be used to interact with the REST backend. Create a `services.js` file and put your new `$resource` service in it.

  ```js
  angular.module('myApp').factory('Book', function($resource) {
    return $resource('http://daretodiscover.herokuapp.com/books/:id');
  });
  ```

1. The result of the function call is a resource class object which has the following five methods by default: `get()`, `query()`, `save()`, `remove()`, `delete()` (delete is an alias for remove)

1. Let’s see how we can use the `get()`, `query()`, `save()`, and `delete()` methods in a controller:
```js
angular.module('myApp').controller('ResourceController',function($scope, Book) {
    $scope.book = Book.get({ id: $scope.id }, function(data) {
      console.log(data);
    }); // get() returns a single book

    $scope.allBooks = Book.query(function(data) {
      console.log(data);
    }); //query() returns all the books

    // add a new book
    $scope.newBook = {"title":"JavaScript: The Good Parts","author":"Douglas Crockford","image":"","release_date":"May 11, 2008"};

    Book.save($scope.newBook, function(data) {
      console.log(data);
    });

    // delete a book
    Book.delete({id:200});
});
```

  The `get()` function in the above snippet issues a GET request to `/books/:id`.

  The function `query()` issues a GET request to /api/entries (notice there is no `:id`).

  The `save()` function issues a POST request to `/api/entries` with the first argument as the post body. The second argument is a callback which is called when the data is saved.

1. We have explored the create, read and delete parts of CRUD. The only thing left is update. To support an update operation we need to modify our custom factory `Book` as shown below.
  ```js
  angular.module('myApp').factory('Book', function($resource) {
    return $resource('http://daretodiscover.herokuapp.com/books/:id', { id: '@_id' }, {
      update: {
        method: 'PUT' // this method issues a PUT request
      }
    });
  });
  ```

1. Now we can use the `update` function like this:
  ```js
  var book = Book.get({ id: $scope.id }, function() {
      book.title = "Updated Title";
      Book.update({id: $scope.id}, book)
  });
  ```

## Base Challenges

1. Display all the books in an aesthetically pleasing layout.
1. Create a form to add a new book. Make it work!
1. Add a delete book button next to each book. Make it work!
1. Add edit functionality.
