Descriptive variable names and parameter names make it easier to understand their purpose.This JavaScript code logs a message about a person's age to the console. The abstract parameter names make it difficult to understand the purpose of the code.

```python
function logPersonsAge(a, b, c) {
  if (c) {
    console.log(a + " is " + b + " years old.");
  } else {
    console.log(a + " does not want to reveal their age.");
  }
}
```

Example prompt:
Improve the variable names in this function

Avoiding sequential conditional checks
if...else chains can be difficult to read, especially when they are long.

Example scenario
This Python code prints the sound that various animals make, if defined, or "Unknown animal" if the animal type is not recognized. However, the chain of if...else statements makes the code inefficient and cumbersome.

```python
class Animal:
    def speak(self):
        pass

class Dog(Animal):
    def speak(self):
        return "Woof!"

class Cat(Animal):
    def speak(self):
        return "Meow!"

class Bird(Animal):
    def speak(self):
        return "Tweet!"

def animal_sound(animal_type):
    if animal_type == "dog":
        return Dog().speak()
    elif animal_type == "cat":
        return Cat().speak()
    elif animal_type == "bird":
        return Bird().speak()
    else:
        return "Unknown animal"

print(animal_sound("dog"))
print(animal_sound("cat"))
print(animal_sound("bird"))
print(animal_sound("fish"))
```
Example prompt:
Simplify this code. Avoid using if/else chains but retain all function return values.

Splitting up large methods
It can be difficult to grasp exactly what a method or function does if it is too long, making it difficult to maintain. Methods or functions that perform multiple tasks may not be reusable in other contexts. It may also be difficult to test each task in isolation.

Example scenario
This Java method processes a customer order and prints a message. It performs multiple tasks in a single method.
```java
public void processOrder(Order order) {
  if (order == null || order.getItems().isEmpty()) {
    throw new IllegalArgumentException("Order is invalid.");
  }

  double totalPrice = 0.0;
  for (Item item : order.getItems()) {
    totalPrice += item.getPrice() * item.getQuantity();
  }
  order.setTotalPrice(totalPrice);

  if (totalPrice > 0) {
    order.setStatus("Processed");
  } else {
    order.setStatus("Pending");
  }

  System.out.println("Order for customer " + order.getCustomerName() + " has been processed. Total price: " + totalPrice);
}
```
Example prompt:
How could the processOrder method be refactored to be more useful and easier to maintain

