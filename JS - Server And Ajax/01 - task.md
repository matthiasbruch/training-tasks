## Preparation
- Install a recent nodejs version.
- Validate that you have installed nodejs:
    - Open a terminal
        - Hit R key while holding Windows key
        - Enter "cmd" and hit the enter key
    - In the terminal enter "node --version"
    - It should return a version number

## Running express
- Create a folder on your harddrive
- Open the terminal and enter "npm init"
- Keep hitting enter till it creates a packages.json
- Open the website "https://expressjs.com/en/starter/installing.html"
- Install "express" according to the instructions
- Manually create an "index.js" file in the same folder
- Open the menu entry "Getting started" and copy the example from the top into your "index.js".
- Run the index.js script
- Open the browser and check what is returned; Change the message and check if it has changed in the browser as well

## Returning JSON
- Copy the example route of expressjs and instead of listening to "/" listen to a path called "/products"
- In that method create an object called "shop" with a property "products"
- Add 3 product-objects into the array
- Serialize the object into a string and return that string in the response.

## Serving static files
In expressjs you can either react on routes (e.g. "/") or you can serve static files from a folder.

- Add a configuration for expressjs to serve static files from the public folder
- Create the "public" folder parallel to your "index.js"
- Create an "index.html" file in the public folder
- Add a script to the index.html file that loads data from your "/products" path. (see: fetch)

## Display HTML elements
For every product that you loaded from the service:

- Create a DIV
- Display the product name of the product inside the DIV 