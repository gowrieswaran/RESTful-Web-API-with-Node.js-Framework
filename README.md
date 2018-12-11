# RESTful-Web-API-with-Node.js-Framework

## Why this project?

This project introduces you to the fundamentals of web APIs with Node.js frameworks. Using your own private blockchain to create a web API is a huge first step toward developing your own web applications that are consumable by a variety of web clients.

## Build your Project

## Select a Node.js framework 

Before building the project, one has to choose their preferred Node.js framework from the following:

- Hapi.js
- Express.js
- Sails.js

I have choosen Express.js for the implementation.

## How to Run

The framework choosen will interface with the private blockchain(https://github.com/gowrieswaran/private-blockchain.git). To run, clone/download the private blockchain repo.

### Configure API service to the appropriate port

Added the server.js to configure the API service to the appropriate port.

### Configure two endpoints - GET & POST

Added the BlockController.js to create two endpoints, which allow the application to accept user requests.

### Install Dependencies

`npm install express`      - Installs the Fast, unopinionated, minimalist web framework for node.

`npm install body-parser`  - Node.js body parsing middleware, which parses incoming request bodies in a middleware before                                            your handlers, available under the req.body property.

### To run the project type `npm start` in the command prompt and on successful launch, it displays the message below:

![Listening for port](https://github.com/gowrieswaran/RESTful-Web-API-with-Node.js-Framework/blob/master/images/start-img.png)

## Testing the endpoints

Several tools are available on the internet to assist with API development and testing.

-Postman is a powerful tool used to test web services.

-CURL is a command-line tool used to deliver requests.

I have used Postman for testing.

## GET Block Endpoint - Tested using Postman

Configure a GET request using URL path with a block height parameter.

`http://localhost:8000/block/[blockheight]`

URL: http://localhost:8000/block/0

Response

![GET block 0](https://github.com/gowrieswaran/RESTful-Web-API-with-Node.js-Framework/blob/master/images/get-block-0.png)

URL: http://localhost:8000/block/100

Response

Block does not exist!

![GET block 100](https://github.com/gowrieswaran/RESTful-Web-API-with-Node.js-Framework/blob/master/images/get-block-100.png)

## POST Block Endpoint - Tested using Postman

Post a new block with data payload option to add data to the block body.

URL: http://localhost:8000/block

KEY:body VALUE:Data Added from Postman

Response

![POST block](https://github.com/gowrieswaran/RESTful-Web-API-with-Node.js-Framework/blob/master/images/post-with-data.png)

URL: http://localhost:8000/block

Response

Pass data to the block using data payload option!

![POST without data](https://github.com/gowrieswaran/RESTful-Web-API-with-Node.js-Framework/blob/master/images/post-without-data.png)

## GET block which is added using POST

URL: http://localhost:8000/block/11

![GET data after POST](https://github.com/gowrieswaran/RESTful-Web-API-with-Node.js-Framework/blob/master/images/get-block-after-post.png)
