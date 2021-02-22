# JavaScript Objects    
Objects are used to store keyed collections of various data and more complex entities. They are created with ```{...}``` and have the option to add properties. Properties are key:value pairs, where the key is a string and the value can be antyhing. https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics

##### Create an Empty Object
    let user = new Object();        //object constructor syntax
    let user = {};                  //object literal syntax
    
### Literals and Properties
##### Adding Properties
Properties can be added to objects when they are created. 

    let user = {                    //object
      name: "John",                 //key => name, value => 'John'
      age: 30,                      //key => age, value => 30
      "likes birds": true,          //use multiple words as key; has to use ""; last comma optional but makes it easier to add to
    };    
##### Accessing Properties
    alert( user.name );
    alert( user.age );
##### Adding key:value
    user.isAdmin = true;            //adds isAdmin:true to user object
##### Deleting key:value
    delete user.age;                //deletes age:30 from user object
### Square Brackets
Multiword properties such as ```"user name": "Joe"``` cannot be accessed with dot access. Dot access will not work with variables that have spaces, start with a digit, or starts with special characters (with the exception of ```$``` and ```_```. Instead you will need to use square bracket notation.

    let user = {};
    user["likes birds"] = true;     //set key:value
    alert(user["likes birds"]);     //get key:value (multi-word)
    delete user["likes birds"];     //delete key:value
    
##### Use Variables to Access Multiline Keys
    let key = "likes birds";
    user[key] = true;
##### Use Prompt/Variable
    let user = {name: "john", age: 30};
    let key = prompt("Enter object value: ");
    alert( user[key] );             //returns john if 'name' is entered
##### Computed Properties
    let fruit = prompt("Which fruit to buy?", "apple");
    let bag = { [fruit]: 5, };      //the name of the property is taken from the variable fruit
    alert( bag.apple );             //5 if fruit="apple"
Can also be written:
    
    let fruit = 'apple';
    let bag = {};
    bag[fruit] = 5;
Or more complex:

    let fruit = 'apple';
    let bag = {
      [fruit + 'Computers']: 5      //bag.appleComputers = 5
    };
### Property Value Shorthand
    function makeUser(name, age) {
      return {
        name: name,
        age: age,
      };
    };
    
    let user = makeUser("John", 30);
    alert(user.name);               //John
Can be written shorthand by:
    
    function makeUser(name, age) {
      return {
        name,                       //same as name: name
        age,                        //same as age: age
      };
    };
### Property Names Limitations
No restrictions as for variables.
    
    for: 1,                         //valid
    let: 2,                         //valid
    return: 3,                      //valid
    0: "test",                      //valid, 0 converted to string "0"
    
    alert (obj["0"];                //valid
    alert (obj[0]);                 //valid
### Property Existence Test, "in" Operator
Reading a non-existent property returns ```undefined```. Note that the purpose of the 'in' property is to test whether a key stores ```undefined``` To test whether a property exists: 
    
    let user = {};
    alert( user.noSuchProperty === undefined );         //true means the property does not exist
Or:
    
    let user = { name: "John", age: 30 };               //the left side of 'in' must be a property name
    alert( "age" in user );                             //true
    alert( "blaaa" in user );                           //false
    
##### Accessing with Variables
    let user = { age: 30 };
    let key = "age";
    alert( key in user );                               //true
### The "for...in" Loop
To go through each key of an object there is a special form of the for...in loop.

    for (key in object) {
      ...;
    }
An example:
    
    let user = { name: "John", age: 30, isAdmin: true, };
    for (let key in user) {
      alert(key);                                       //name, age, isAdmin
      alert(user[key]);                                 //John, 30, true
                                                        //can also use ```for (let prop in obj)```
##### Ordered Like an Object
Integers are sorted in order. In this case, '+49' and '1.2' are not integers.

    let codes = {
      "49": "Germany",
      "41": "Switzerland",
      "44": "Great Britain",
      "1": "USA",
    };
    
    for (let code in codes) {
      alert(code);                                      //1, 41, 44, 49
    }
If the keys are non-integer, then they are listed in creation order.

    let user = { name: "John", surname: "Smith" };
    user.age = 25;
    for (let prop in user) {
      alert( prop );                                    //name, surname, age
    }
To get integer keys to show in order, we can make them non-integer by:
    
    for (let code in codes) {
      alert( +code );                                   //49, 41, 44, 1
    }
    
    
    
    
    
    
