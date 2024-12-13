This JavaScript code creates three Person objects, each with name and age properties. It then uses the name of a person to retrieve and print their age.

```javascript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
}

var people = {};

function addPerson(name, age) {
  people[name] = new Person(name, age);
}

function getAge(name) {
  if (people[name]) {
    console.log(name + " is " + people[name].age + " years old.");
  } else {
    console.log("Person not found.");
  }
}

addPerson("Ana", 30);
addPerson("Mario", 25);
addPerson("Louise", 40);

getAge("Mario");
```

Example prompt 1
What design patterns could improve this code? Don't show me code examples.

Example prompt 2
You can now ask Copilot to implement the pattern that you feel is most appropriate.

Refactor this code using the suggested pattern
