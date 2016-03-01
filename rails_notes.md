controller receives specific requests for the application.
---this is where the info is collected.
---controller name while generating one should be plural. eg. aritcles
---CRUD methods are defined in the controller
---Only public methods can be actions for controllers.

routing decides which controller receives which requests.
--- a route is basically a web url.So for a route/web url to work it needs to have a controller defined to serve the request.

Action collects information to provide it to a view.

View/view templates/.html.erb_files displays this info in human readable format.

resources - a method used to declare a standard rest resource.a new resource needs to be added to routes.rb.
---After declaring a resource rake routes defines routes for all the standard RESTful actions
---**Resource name to be plural.

Forms
---<%= f.submit :Go%>/*this is how to change submit button's text now submit button will read Go*/
---New form submissions is handled by the create method.
---when a form is submitted its fields are sent to rails as parameters and can be used inside a controller's method. 
ex- params[:username], params[:age],etc.
---all form fields with errors are automatically wrapped with a div class called "field_with_errors"
--- text_field is used for single line input and text_area is used for multi-line inputs.

Models
--- Models while being generated use a singular name beginning with a capital letter
    and the corresponding database table uses a plural name.
--- when a form is being submitted for editing rather than new submission must use PATCH HTTP method.
---passing a symbol with the same name,say ':article' instead of an instance variable of same name say '@article' 
   leads to the same behaviour.
---scaffold and models can be roughly interchangable terms.

DB
---maybe need to run migration file to create tables in the database. or to create the database structure.

Class
---Class names in ruby must begin with a capital letter.

#Standard CRUD action ordering: index-show-new-edit-create-update-destroy:ALL PUBLIC METHODS


SQLITE3
---invoke terminal->sqlite3 db/development.sqlite3

Doubts
---can render method take full urls???
---learn rails refactoring

MIGRATIONS
--when rake db:migrate is run only those tables that are not created are constructed.



