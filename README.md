# phase-3-week-2-coffee-shop-challenge

      Coffee Ordering System

A simple Python-based object-oriented system that models the relationship between Customers, Coffees, and Orders. The project demonstrates clean OOP design, data validation, and associations among classes.

      Project Structure

pgsql
Copy code
coffee-ordering-system/
├── customer.py
├── coffee.py
├── order.py
└── README.md
Features
Customer

Can place orders for different coffee types.

Tracks all their own orders.

Can view a list of all unique coffees they've ordered.

Can create new orders via a method.

Class method most_aficionado determines which customer has spent the most on a specific coffee.

Coffee

Tracks all orders associated with that coffee.

Can list all unique customers who ordered it.

Calculates:

Total number of orders.

Average price of all orders for that coffee.

Order

Connects a customer to a coffee with a specific price.

Enforces validations:

customer must be a valid Customer instance.

coffee must be a valid Coffee instance.

price must be a float between 1.0 and 10.0.

            * How It Works

This project models real-world relationships:

A Customer can place many Orders.

Each Order is for one Coffee.

A Coffee can be ordered by many Customers through Orders.

Example usage:

python
Copy code
from customer import Customer
from coffee import Coffee

# Create instances

alice = Customer("Alice")
espresso = Coffee("Espresso")

# Customer places an order

alice.create_order(espresso, 4.5)

# Check orders

print(alice.orders) # All Alice's orders
print(espresso.orders) # All orders for Espresso
print(espresso.customers) # Unique customers who ordered Espresso

-      Validations
  Customer name must be a string of 1 to 15 characters.

Coffee name must be a string with at least 3 characters.

Order price must be a float between 1.0 and 10.0 inclusive.

-     Concepts Demonstrated
  Object-Oriented Programming (OOP)

Encapsulation and property decorators

Class and instance methods

Data validation

Relationships: One-to-Many, Many-to-One

Aggregation and association of objects
