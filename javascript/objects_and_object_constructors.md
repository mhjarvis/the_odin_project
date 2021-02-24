### Refresher
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
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
