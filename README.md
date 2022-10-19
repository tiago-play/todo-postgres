<h1 align="center">
  🐘 Api Todo with ElephantSQL - PostgreSQL as a Service
</h1>

<p align="center">
  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/tiago-play/todo-postgres">

  <img alt="Repository size" src="https://img.shields.io/github/repo-size/tiago-play/todo-postgres">

  <a href="https://github.com/https://github.com/tiago-play/todo-postgres">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/tiago-play/todo-postgres">
  </a>

  <a href="https://github.com/tiago-play/todo-postgres">
    <img alt="Repository issues" src="https://img.shields.io/github/issues/tiago-play/todo-postgres">
  </a>

  <img alt="License" src="https://img.shields.io/badge/license-GNU-brightgreen">
</p>


<p align="center">
	<a href="#-technologies">Technologies</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
	<a href="#-project">Project</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
	<a href="#-instructions">Instructions</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp; 
	<a href="#-routes">Routes</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
	<a href="#-license">License</a>
</p>

## 🚀 Technologies

This project was development with the following technologies
- Javascript 
- Nodejs

**Dependencies**
- Express.js
- PG > Module for connection with the Database
- Dotenv > Environment Variables Configuration
- Nodemon > Installed in the development environment, restart the server automatically at any changes


## 💻 Project
This project was developed for acquiring skills with the video tutorial *__API REST NodeJS em menos de 1h: Todo app com Express e Postgres (SQL) - deploy no Heroku__* of the youtube channel [Dev & Design](https://www.youtube.com/watch?v=8T8YmSHZ3fg). The API is a CRUD system, with an route for each operation, and database in the cloud. 


## ✍🏻 Instructions
1. The project was deployed in Heroku, URL for test online: <br>
https://tiago-play-api-node-postgres.herokuapp.com/
2. If you prefer you can download the project in your computer, in both cases it's necessary use an API client like [Insomnia](https://insomnia.rest/download) or [Postman](https://www.postman.com/).
3. Instructions for download
4. Clone this repository <br>
https://github.com/tiago-play/todo-postgres
5. Open the paste of the project in the terminal/cmd
6. Install the dependencies <br>
*__npm install__*
7. Run the server in production mode <br>
*__npm start__*
8. The server will start on port 3333, or in another available if you run in the Heroku. 
9. URL for local test: http://localhost:3333

## 🥷🏻 Routes
All routes that have body is type json

**Create and login User**
- Route: /session <br>
- Checks if the user exists, if doens't, the user is created <br>
- Method: Post <br>
- Body:
```
{
	"username": "user@gmail.com"
}
```	
<br>

**Now for the next routes is simulated that the user are logged in, so will be necessary the user_id** <br>
Only the user_id who created the **todo** can execute the crud methods.<br>

**Create todo**
- /todo/:user_id
- Method: Post
- Body
```
{
	"description": "test",
	"done": (boolean)
}
```

**List todo**
- Route: /todo/:user_id
- Method: Get
- Hans't body

**Update todo**
- Route: /todo/:user_id/:todo_id
- Method: Patch
- Body: 
```
{ 
	"description": "write the readme file", 
	"done": false 
}
```

**Delete todo**
- Route: /todo/:user_id/:todo_id
- Method: Delete
- Hans't body

## 📝 License

This project it is under the license GNU. Se the de file [LICENSE](LICENSE.md) for more details.
