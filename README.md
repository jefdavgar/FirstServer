# Creating Your First Node.js Server
Node.js is a powerful and popular server-side platform for web development. In this tutorial, we'll be showing you how to create a simple Node.js server from scratch.
 
## Prerequisites
Before we start, make sure you have the following tools installed:

Node.js (you can download it from the official website)
A code editor of your choice (such as Visual Studio Code)
Step 1: Creating a New Project
Open your code editor and create a new folder for your project. In this example, we'll call it "FirstServer".

## Step 2: Installing Required Packages
We will use the popular express package to create our Node.js server. To install it, open a terminal in your project folder and run the following command:

npm install express

## Step 3: Creating the Server
Create a new file in your project folder and name it index.js. This will be the entry point for our server.

Start by including the express package and creating an instance of the express application:
const express = require("express");
const app = express();
Next, we'll define the port that our server will listen to. In this example, we'll use port 3000:

const port = 3000;
Now, let's create our first endpoint. An endpoint is simply a URL that our server will respond to. In this example, we'll create an endpoint for the root URL (/):

app.get("/", (req, res) => {
  res.send("Hello Jeff");
});
Finally, we'll start our server by calling the listen method on our app instance and passing it the port we defined earlier:

app.listen(port, () => {
  console.log("My port is: " + port);
});

## Step 4: Running the Server
Open a terminal in your project folder and run the following command to start the server:

node index.js
You should see the following output in your terminal:

My port is: 3000
To test your server, open a web browser and go to http://localhost:3000. You should see the message "Hello Jeff" displayed in the browser.
