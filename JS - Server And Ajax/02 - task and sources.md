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
    - You see there the npm init command
- Install "express" according to the instructions
- Manually create an "index.js" file in the same folder
- Open the menu entry "Getting started" and copy the example from the top into your "index.js".
- Run the script (nodejs <filename> in terminal)
- Open the browser and check what is returned; Change the message and check if it has changed in the browser as well

## Returning JSON
- Copy the example route of expressjs and instead of listening to "/" listen to a path called "/products"
- In that method create an object called "shop" with a property "products"
- Add 3 product-objects into the array
- Serialize the object into a string (see: JSON.stringify) and return that string in the response (see: res.send).

```JSON
var shop = {
    "products": [ ]
}
```

## Serving static files
In expressjs you can either react on routes (e.g. "/") or you can serve static files from a folder.

- Before calling "app.listen" from the example above, add a line to serve the files from the public folder:

```JS
app.use(express.static('public'))
```

After this all files in the public folder can be called directly.
- Create the "public" folder parallel to your "index.js"
- Create an "index.html" file in the public folder
- Add a script to the index.html file that loads data from your "/products" path. (see: fetch)

```JS
fetch(<absolute/relative-url>)
    .then((response) => {
        return response.json();
    })
    .then((loadedProducts) => {
        // do something - e.g. console.log(loadedProducts)
    })
```

## Display HTML elements
For every product that you loaded from the service:

- Create a DIV
- Display the product name of the product inside the DIV 