# Whipped 쇼필몰 제작

- Made a shopping mall by copying the 'Whipped' site, whice sells eco-friendly products.
  
### 1. Built with

- Java
- Node.js
- React
- Postgresql


### 2. Getting started

- Init package.json
- Coding Nodejs for API Server
- Install Express
- Create MySQL Database
- Install MySQL Connector and Sequelize ORM
- Define Sequelize Object Model
- Create Table Scheme
- Syncronize Object Model with Database



### N. Trouble Shutting

- Issue No.1: When refreshing the page, a 404 error occurs even though the screen loads correctly initially.
- Issue No.2: React-Uncaught SyntaxError : Unexpected Token <.
- Issue No.3: 
- Issue No.4: 

### N. Solving Problems

- Issue No.1: Create a file called nginx.conf and configure the Nginx web server to first check the index.html file when the page is refreshed, in order to verify if the requested route exists.
- Issue No.2: Added <base href='/' /> to the index.html file.


### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
