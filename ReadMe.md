# Server Side

## Installation 
https://www.npmjs.com/package/json-server

 ### Server command
    npm install json-server

### DataBase Creation
Create a file named __db.json__
and copy paste for basic json database (you can use GPT for better bigger data in the same format)


    {
    "products": [
        {
        "id": "c095",
        "name": "milk",
        "categoryId": "2",
        "price": 5.5,
        "stock": 100
        },
        {
        "id": "206c",
        "name": "Apple",
        "categoryId": "1",
        "price": 0.5,
        "stock": 100
        }
    ],
    "categories": [
        {
        "id": "1",
        "name": "Fruits"
        },
        {
        "id": "2",
        "name": "Dairy"
        },
        {
        "id": "3",
        "name": "Bakery"
        }
    ],
    "cart": [
        {
        "id": "206c",
        "name": "Apple",
        "categoryId": "1",
        "price": 0.5,
        "stock": 100
        }
    ]
    }


 ### Server command to run server
    $ npx json-server db.json

### result
    JSON Server started on PORT :3000
    Press CTRL-C to stop
    Watching db.json...

    ♡⸜(˶˃ ᵕ ˂˶)⸝♡

    Index:
    http://localhost:3000/

    Static files:
    Serving ./public directory if it exists

    Endpoints:
    http://localhost:3000/products
    http://localhost:3000/categories
    http://localhost:3000/cart

## Axios 
https://www.npmjs.com/package/axios

<script src="https://cdn.jsdelivr.net/npm/axios@1.6.7/dist/axios.min.js"></script>


better fech method
### Installltion Terminal Command
    npm install axios

# CRUD
    GET - READ
    PUT - UPDATE
    POST - WRITE 
    DELETE - DELETE

## GET
    <body>
        <script>
        const SERVER = "http://127.0.0.1:3000/products"
        axios(SERVER).then(res => console.log(res.data));
    </script>
    </body>

###
        const SERVER = "http://127.0.0.1:3000/products/"
        axios(SERVER).then(res => display.innerHTML = res.data.map(products => `
        <div>
                    <button onclick="deleteItem('${products.id}')">Delete from cart</button>
                    <button onclick="add('${products.name}')">Add to cart</button>
            name:${products.name},
            category:${products.categoryId}
            </div>
        `).join(""));
## POST
    // add a new item
                const add = () => {
            axios.post(SERVER, {
                name: itemName.value,
                categoryId: categoryId.value,
                price: price.value,
                stock: stock.value
            }).then(res => console.log(res));
        };

        const addCart = (id, name, categoryId, price) => {
            axios.post(CARTSERVER, {
                id: id,
                name: name,
                categoryId: categoryId,
                price: price
            }).then(res => console.log(res));
        };



# Front Side

### BootStrap 
a tool for nice css

    <!DOCTYPE html>
    <html lang="en">

    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">

    </head>




# TO DO LIST

Unordered List
 * add searchbar
 * better UI
 * make ASYNC


