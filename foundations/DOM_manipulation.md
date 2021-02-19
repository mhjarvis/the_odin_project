# DOM or Document Object Model
A tree-like representation of a webpage. 

    <div id="container">                                                //parent
      <div class="display"></div>                                       //child of id="container"
      <div class="controls"></div>                                      //sibling of class="display"
    </div>

### Targeting Nodes with Selectors
These nodes can be targeted with CSS-style selector and/or relationship properties.

    <div class="display"></div>                 //can be targeted with div.display, .display,
                                                //#container>.display, div#container>div.display
    
    const container = document.querySelector('#container');     //select the #container div
    console.dir(container.firstElementChild);                   //select the first child of #contaainer (.display)
    const controls = document.querySelector('.controls');       //select the .controls div
    console.dir(controls.previousElementSibling);               //selects the prior sibling (.display)
    
### DOM Methods
##### Qeury Selectors
    element.querySelector(selector)             //returns reference to the first match of selector
    element.querySelectorAll(selectors)         //returns a 'nodelist' containing references to ll of thematches ofthe selectors
    Array.from()                                //convert nodelist to array
##### Element Creation
    document.createElement(tagName[, options])  //creates a new element of tag type tagName
                                                //[options] allows optional parameters
                                                
    const div = document.createElement('div');  //creates div in memory which allows you to add styles, classes, etc.

##### Append Elements (plaace element into the DOM)
    parentNode.appendChild(childNode)                   //appends childNode as the last child of parentNode
    parentNode.insertBefore(newNode, referenceNode)     //inserts newNode into parentNode before referenceNode
    
##### Remove Elements
    parentNode.removeChild(child)                       //removes child from parentNode on the DOM and returns reference to the child

##### Altering Elements
    const div = document.createElement('div');          //create a new div referenced in the variable 'div'
    
    div.style.color = 'blue';                                       //adds style rule
    div.style.cssText = 'color: blue; background: white';           //adds several style rules
    div.setAttribute('style', 'color: blue; background: white');    //adds several style rules
    
##### Editing Attributes
    div.setAttribute('id', 'theDiv');                               //if id exists, update it to 'theDiv', elsecreate an id
    div.getAttribut('id');                                          //return the value of specified attribute
    div.removeAttribute('id');                                      //remove specified attribute
    
##### Working with Classses
    div.classList.add('new');                                       //adds class 'new' to your new div
    div.classList.remove('new');                                    //remove 'new' class from div
    div.classList.toggle('active');                                 //if div doesn't hve class 'active, add it, or if it has it
                                                                    //remove it
##### Adding Text Content
    div.textContent = 'Hello World!'                                //create a text node containing text
    
##### Adding HTML Content
    div.innerHTML = '<span>Hello World!</span>';                    //render the html inside the div
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
