# JavaScript Objects
Objects are used to store keyed collections of various data and more complex entities. They are created with ```{...}``` and have the option to add properties. Properties are key:value pairs, where the key is a string and the value can be antyhing. 

##### Create an Empty Object
    let user = new Object();        //object constructor syntax
    let user = {};                  //object literal syntax
    
### Literals and Properties
##### Adding Properties
Properties can be added to objects when they are created. 

    let user = {                    //object
      name: "John",                 //key => name, value => 'John'
      age: 30,                      //key => age, value => 30
      "likes birds": true           //use multiple words as key; has to use ""
    };    
##### Accessing Properties
    alert( user.name );
    alert( user.age );
##### Adding key:value
    user.isAdmin = true;            //adds isAdmin:true to user object
##### Deleting key:value
    delete user.age;                //deletes age:30 from user object
    
