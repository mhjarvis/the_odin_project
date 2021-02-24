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
# Objects as Design Patterns
    
