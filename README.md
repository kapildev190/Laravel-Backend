# Laravel REST API with Sanctum

This is an example of a REST API using auth tokens with Laravel Sanctum

## Usage

Change the *.env.example* to *.env* and add your database info

Change database setting and follow below mentined step 

# Update composer
composer update

# Run migration
php artisan migrate

# Run the webserver on port 8000
php artisan serve


## Routes

```
# Public

GET   /api/products
GET   /api/products/:id

POST   /api/login
@body: email, password

POST   /api/register
@body: name, email, password, password_confirmation


# Protected

POST   /api/products
@body: name, slug, description, price

PUT   /api/products/:id
@body: ?name, ?slug, ?description, ?price

DELETE  /api/products/:id

POST    /api/logout
```
