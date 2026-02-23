# cs2-creating-elements

# Learning Target
I am learning how to create elements with the DOM and JavaScript

# Success Criteria
- I can create an element using ```document.createElement(tagname)``` and store it in a variable
- I can use ```document.body.appendChild(newElement)``` to add a new element to the end of the body
- I can use ```existingElement.appendChild(newElement)``` to add a new element to an existing element

# Project Setup
1. Install *Live Server*
2. Create ```script.js```
3. Add ```console.log("Script started")``` to begining of ```script.js```
4. Add ```<script src="script.js"></script>``` before ```</body>``` tag in ```index.html``` to link the script
5. Go live and use the inspection tool to check that you see ***Script started*** in the console to verify your script is linked correctly to your html 

# Essential Notes
There are three basic steps to creating a new element on your webpage.
1. Create the element from a tag name (e.g. ```"p"```, ```"h1"```, ```"img"```, etc.) using ```createElement(tagname)``` and store it in a variable
    ```javascript
    let newElement = document.createElement("p");
    ```
2. Configure the new element by setting its text, attributes, and styles (right now, we only know how to set its text)
    ```javascript
    newElement.innerText = "some text";
    ```
3. Add it to an existing container element using ```appendChild(newElement)```
    - **Option 1** Add it to the end of the ```body```
    ```javascript
    document.body.appendChild(newElement);
    ```
    - **Option 2** Add it to the end of another element (usually a ```div```) in which case you need to first get the existing element stored in a variable
    ```javascript
    let existingElement = document.getElementById("my-div");
    existingElement.appendChild(newElement);
    ```

# Example 1
1. Define a new function named ```addElementToBody()```
    ```javascript
    function addElementToBody() {

    }
    ```
2. Add the ```onclick``` attribute to the **Add element to body** button in ```index.html``` to call the function
    ```html
    <button onclick="addElementToBody()">Add element to body</button>
    ```
3. In your function, create a new ```p``` tag and set its text to **Hello world!**
    ```javascript
    let p = document.createElement("p");
    p.innerText = "Hello world!";
    ```
4. Append the new paragraph element to the body
    ```javascript
    document.body.appendChild(p);
    ```
5. Test and check the console for error messages

# Example 2
1. Define a new function named ```addElementToContainer()```
    ```javascript
    function addElementToContainer() {

    }
    ```
2. Add the ```onclick``` attribute to the **Add element to container** button in ```index.html``` to call the function
    ```html
    <button onclick="addElementToContainer()">Add element to container</button>
    ```
3. In your function, create a new ```h1``` tag and set its text to **whatever**
    ```javascript
    let h1 = document.createElement("h1");
    h1.innerText = "whatever";
    ```
4. Store the container element in a variable
    ```javascript
    let container = document.getElementById("container");
    ```
5. Append the new ```h1``` element to the body
    ```javascript
    container.appendChild(h1);
    ```
6. Test and check the console for error messages