### Doubts and todo
+ can render method take full urls???  
+ learn rails refactoring
+ Callbacks in rails http://api.rubyonrails.org/v4.0.0/classes/ActiveRecord/Callbacks.html
& http://guides.rubyonrails.org/v3.2.13/active_record_validations_callbacks.html
+ How to deploy to production with ssl -7.4.4
+ Use of has_many through in joining tables.

### Ruby
+ All ruby objects are true, even 0. Only 'nil' and 'false' are false in ruby.
+ An array index of -1, ie, a[-1] represents the last array element.
+ self is used to denote that same object in a function, i.e. self == self.reverse

### General
+ HTTP is a stateless protocol. When a user makes a second request all the variables get set to their defults
 and instance variables to nil.

### Partials
+ name starts with a underscore
+ used as render 'location of partial file'

### controller
+ Controller receives specific requests for the application.  
+ this is where the info is collected.  
+ controller name while generating one should be plural, eg aritcles  
+ CRUD methods are defined in the controller  
+ Only public methods can be actions for controllers  
+ If a method is needed by more than 1 controller then we can move it to one of the helpers and then include it in application_controller.rb

### helpers
+ They are functions written to add more functionality to the view pages.
+ By default, methods defined in any helper file are automatically available in any view but not in any controller. To do so its helper controller must be included in the application_helper.rb

### Routing
+ decides which controller receives which requests.
+ a route is basically a web url.So for a route/web url to work it needs + to have a controller defined to serve the request.  

### Action
+ collects information to provide it to a view.    

### View
+ View/view templates/.html.erb_files displays this info in human readable format.    

### Resources
+ a method used to declare a standard rest resource.a new +resource needs to be added to routes.rb.
+ After declaring a resource rake routes defines routes for all the standard RESTful actions
+ Resource name to be plural.   

### Forms
+ <%= f.submit :Go%>/*this is how to change submit button's text now submit button will read Go*/
+ New form submissions is handled by the create method.
+ when a form is submitted its fields are sent to rails as parameters and can be used inside a controller's method.
ex- params[:username], params[:age],etc.
+ all form fields with errors are automatically wrapped with a div class called "field_with_errors"
+ text_field is used for single line input and text_area is used for multi-line inputs.     

### Models
+ Models while being generated use a singular name beginning with a capital letter
+ and the corresponding database table uses a plural name.
+ when a form is being submitted for editing rather than new submission must use PATCH HTTP method.
+ passing a symbol with the same name,say ':article' instead of an instance variable of same name say '@article' leads to the same behaviour.
+ scaffold and models can be roughly interchangable terms.The naming convention is same for both, i.e. singular.

### DB
+ Migrations need to be run to actually create tables in the database.
+ adding index to columns whose data you need to check if it exists makes the searches faster, because index notes all the occurrences of a particular entry.  
+ always create and run a new migration for any changes in DB structure.
+ create a production database by "$ bundle exec rake db:migrate RAILS_ENV=production"
+ Rails expects foreign key of the form <class_id> where class means the class name of the parent " database table" from which we are referencing the other table. This key has to be an attribute in the other table. Using this naming convention automatically creates foreign keys.

### Class
+ Class names in ruby must begin with a capital letter.    

### Standard CRUD action ordering:
+ index-show-new-edit-create-update-destroy:ALL PUBLIC METHODS

### SQLITE3
+ invoke terminal->sqlite3 db/development.sqlite3

### MIGRATIONS
+ when rake db:migrate is run only those tables that are not created are constructed.
+ ending a migration name with the tables' name helps rails to automatically infer the table we're interested in.

### Github posting

#### adding new repository
1. "git init" - add the git folder
2. "git add ."  -add all files in that folder recursively
3. git commit -m "Initial Commit"
4. "git remote add origin https://github.com/ravi8470/<repository_name>"
5. "git push -u origin master"  

#### For saving changes
+ git add .
+ "git commit -a -m "description"
+ "git push -u origin master"

### methods
+ Using ! after the name of a method causes it to raise an exception on failure.
