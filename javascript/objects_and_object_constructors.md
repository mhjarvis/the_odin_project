# Refresher
##### Defining an Object
    const myObject = {
      property: 'Value',
      otherProp: 77,
      "another property": function() {},
    }
##### Get Information Out of an Object
    myObject.property;              //'Value'   //dot notation will not work for sentence strings
    myObject["another property"];   //function(){}
    
    const variable = 'property';
    myObject.variable;              //will not work, as it will look for 'variable' key in object
    myObject[variable];             //will work
### Objects as Design Patterns
    const playerOneName = "tim"
    const playerTwoName = "jenn"
    const playerOneMarker = "X"
    const playerTwoMarker = "O"

    const playerOne = {
      name: "tim",
      marker: "X"
    }

    const playerTwo = {
    name: "jenn",
    marker: "O"
    }
### Object Constructors
    function Player(name, marker) {         //object with constuctor
      this.name = name;
      this.marker = marker;
    }
    
    constant player = new Player('steve', 'X');
    console.log(player.name);                       //returns name
    
##### Adding Function to Object
    function Player(name, marker) {
      this.name = name;
      this.marker = marker;
      this.sayName = function() {
        console.log(name);
      }
    }
    
    const player1 = new Player('steve', 'X');
    player1.sayName();                              //steve
    
# Factory Functions and the Module Pattern
### Factory Function Introduction
The factory function pattern is similar to constructors, but instead of using ```new``` to create an object, factory functions simply set up and return the new object when you call the function. 
    
    const personFactory = (name, age) => {
      const sayHello = () => console.log('hello');
      return {name, age, sayHello};
      };
      
    const jeff = personFactory('jeff', 27);                 //create object
    console.log(jeff.name);                                 //jeff
    jeff.sayHello();                                        //calls the sayHello() function
    
This is the same as:

    ---------------------------------------------------------------------------------------
    const Person = function(name, age) {
      this.sayHello  = () => console.log('hello');
      this.name = name;
      this.age = age;
    };
    
    const jeff = new Person('jeff', 27);
    ---------------------------------------------------------------------------------------
##### Object Shorthand
If creating an object where you are referring to a variable that has the exact same name as the object property you are creating, you can condense like so:

    return {name, age, sayHello};
### Scope and Closure
Scope refers to where things like variables and functions can be used. 

### Private Variables and Functions
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
