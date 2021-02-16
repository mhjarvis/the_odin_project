# Basic Data Types
### Numbers
##### Convert between int and float
    12.to_f                                     //12.0
    12.34.to_i
##### Number Methods
    6.even?                                     //true
    8.odd?                                      //false
### Strings
##### Ways to Concatenation
    "Hello" + "there!"                          //Hello there!
    "Hello" << "there!"                         //Hello there!
    "Hello ".concat("there").concat("!")        //Hello there!
##### Substrings
    "hello"[0]                                  //'h'
    "hello"[0..1]                               //'he'
    "hello"[0, 4]                               //'hell'
    "hello"[-1]                                 //'o'
    "hello"[0..-1]                              //'hello'
##### Escape Characters
    \\                                          //backslash
    \b                                          //backspace
    \r                                          //carriage return
    \n                                          //newline
    \s                                          //space
    \t                                          //tab
    \"                                          //double quote
    \'                                          //single quote
##### Interpolation
    name = "Markus"
    puts "Hello, #{name}"                       //Hello, Markus
    puts 'Hello, #{name}'                       //Hello, #{name}
##### String Methods    https://ruby-doc.org/core-2.7.1/String.html
    "hello".capitalize                          //Hello
    "hello".include?("el")                      //true
    "hello".include?("f")                       //false
    "hello".upcase                              //HELLO
    "HEllO".downcase                            //hello
    "hello".empty?                              //false
    "".empty?                                   //true
    "hello".length                              //5
    "hello".reverse                             //olleh
    "hello there".split                         //["hello", "world"]
    "hello".split("")                           //["h", "e", "l", "l", "o"]
    "hello there  ".strip                       //hello there
    "he33o".sub("3", "l")                       //hel3o
    "he33o".gsub("3", "l")                      //hello
    "hello".insert(-1, " there")                //hello there
    "hello world".delete("l")                   //heo there
    "!".prepend("hello, ", "world")             //hello, world!
##### Convert to String
    5.to_s                                      //"5"
    nil.to_s                                    //""
    :symbol.to_s                                //"symbol"
### Symbols
#####
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
