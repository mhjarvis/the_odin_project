### Variables
Variables can only contain letters, digits, or the symbols $ and _ . The first digit cannot be a number. Case does matter. Non-latin letters are allowed but not recommended.

    let message                                         //declaration
    let user = "j", age = 2;                            //declare multiple variables at once
    
    let user = "j",                                     //declare multiple variables variant
        age = 24,
        message = "H";  
        
### Constants
Constant variables cannot be reassigned. Use uppercase for constants. 

    const PI = 3.14;

### Numbers
Adding a string and number will result in a string. JavaScript will try to convert strings to numbers in all numeric operations (ex: "100" / "10" = 10 (except for addition). "10" + "20" = 1020. 'NaN means not a legal number (as in 100 / "number"). 

    console.log(0.2 + 0.1)                              //precision is an issue as this will return 0.30000000000000004
    console.log(0.2 * 10 + 0.1 * 10)                    //will return 0.3
    isNaN(10);                                          //true
    
    var x = NaN;
    var y = "5";
    var z = x + y;                                      //z will be NaN5
    
    typeof NaN                                          //return number
    Infinity                                            //is returned when number is outside the largest possible number
    -Infinity                                           //division by zero will also result in Infinity
    
    var x = 0xFF;                                       //hexideimal; will return 255
    
    var n = 32;
    n.toString(10);                                     //returns 32
    n.toString(16);                                     //returns 20
    
    var y - new Number(123);                            //y defined as an object
    ==                                                  //checks for equality
    ===                                                 //equal numbers are not equal; === expects equality in type and value
    
    var x = new Number(500);
    var y = new Number(500);
    x == y;                                             //false, becuase comparing two objects always is false
    
### Strings
    str.length;                                         //return length of string;
    str.indexOf("World");                               //returns index of first occurance, -1 if not found
    str.lastIndexOf("World");                           //returns index of last occurance
    str.search("locate");                               //search cannot take a second start position argument
                                                        //indexOf cannot take powerful search values (reg expressions)
##### Extracting String Parts
    str.slice(start, end);                              //end is not included; if negative, it is counted from the end of str
                                                        //omiting the 2nd parameter will cut off the rest of the string
    str.substring(start, end);                          //substring cannot accept negative values
    str.substr(start, length);                          //second parameter specifies the length of the extracted part
    
##### Replace String Content
    str = "Please visit me";                            //replaces first match; is case sensitive
    let n = str.replace("me", "us");                    //returns Please visit us; returns new string
    let n = str.replace(/MICROSOFT/i, "Something");     ///replace case insensitive with /i
    str.replace(/Microsoft/g, "Something");             //replace all matches with /g
    let n = str.toUpperCase();                          //convert str to upper case
    let n = str.toLowerCase();                          //convert str to lower case
    text1.concat(" ", text2);                           //concat two strings
    
    str.trim();                                         //removes whitespace from both sides of a string
##### str.padStart(x, y), str.padEnd(x, y)
    let str = "5";
    str = str.padStart(4, 0);                           //returns 0005
    str = str.padEnd(4, 0);                             //returns 0006
##### charAt()
    str.charAt(0);                                      //returns character at that position (0)
    str.charCodeAt();                                   //returns unicode of the char at position (x)
    str[0];                                             //allows property access
##### Converting a String to an Array
    str.split();                                        //input what to split on
    
### Conditionals
##### String comparisons
    alert('Z' > 'A');                                   //true
    alert("glow" > "glee");                             //true
    alert('2' > 1);                                     //true as '2' becomes a number
    alert(true == 1);                                   //true
    
    0 == false                                          //true
    0 === false                                         //false (=== checks the equality without type conversion)

    



    
