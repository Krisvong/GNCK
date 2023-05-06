# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)


1. GNCK PERN To Do App

This is the Milestone two project of all stars Casey, Kristen, Nick and Gregg for the NCSU Software Development Bootcamp. The goal ofthis project was to demonstrate our knowledge and understanding of a fuulstack application from conception to deployment. It is a culmination of all of our work in the software development course with a specific focus on building from scratch a React front end, an Express back end, connecting to a PostgreSQL database, and running in a Node environment. Our overarching goal was to build an API that relied on RESTful pricipals, keeping our code as DRY as possible, and to make an app that was functional and useful, and that looked good too. This project differed from our last in that it involved a group that allowed us begin to better understand what a real working environment in this field could be like. We at once had to put aside any apprehension and learn very quickly to cooperate and help each other navigate the ins and outs of collaborative coding.
2. Outline

In order to organize our original thoughts, we started our planning with an outline. It was not 100% complete, and it had some things that would change in the end, but it helped us to get going.
Here is what our outline looked like:
Pern to do List outline

Build server
Create folder to hold client and server
In server NPM init
NPM install express, PG, cors
Touch index.js
In index.js require express
Cont app = express()
app.listen(5000, () => {console.log(“server has started on port 5000)});
Start nodemon
Const cors = require(“cors”);
Create middleware (app.use(cors())
app.use(express.json());
Create postgres database and table
Create file called database.sql
Inside database.sql at the top CREATE DATABASE perntodo;
CREATE TABLE todo
Got to postgres shell type psql -U postgres
Type your password
/l to view all Databases
Move inside the database for todo
Copy CREATE DATABASE command from database.sql and run in shell
/dt to view the table
Connect our Postgres database and server
Create a file called db.js
Inside db.js const Pool = require(“pg”),Pool;
Below that const pool = new Poolmodule.exports = pool;
Go back to index.js const pool = require(“./db”);
Routes create a todo -Get all todo -Get a todo -Update a todo -Delete a todo
Build routes with postgres queries
Start creating client side
New terminal npx create-react-app define as client
Go into client
Get rid of test
Get rid of service worker
Get rid of logo
Go into index.js
Get rid of service worker stuff and comments
Go into app.js get rid of logo
In import react statement add { Fragment }
Under function App clean out and add return
Make new folder called components
New file Input todo.js
New file Listtodos.js
New file Edittodo.js
Open bootstrap website
copy bootstrap css link
Add bootstrap link to public .html file
Get js model from bootstrap website
Place near the bottom body of public.html
Build input component
Npm start in client folder
Go into input component folder
Import React from “react”
Const InputTodo = () => { -Return ( -h1 Input todo h1 -) - }
Export default InputTodo;
Go to app.js
Import InputTodo from “./components/InputTodo”
Inside fragment in function app put
Add
Go back into InputTodo component folder
Add {Fragment} to React import statement
Put in InputTodo function
Add h1 To do List h1 inside fragment in function
Add className of “text-center and mt5
Under that create a form className=”d-flex mt 5”>
input type=”text” className=”form-control”
<button className=”btn btn-success”>Add
Add React hooks { Fragment, useStste }
In the top of the function before return add const[description, setDescription] = useState (“”)
After input type=text className=formControl add value={description}
After that onChange={e => setDescription(e.taget.value)}
After the UseState of # 70 const onSubmitForm =async(e) => { -e.preventDefault(); -Try{ -const body = { description }; -Const response = await fetch(“http://localhost:5000/todos”, { -method: “POST”, -headers: {“Content-Type”: “application/json” }, -body: JSON.stringify(body) -}); -} catch (err) { -console.error(err.message) -}
Add onSubmit={onSubmitform} to form at d-flex
Build the ListTodo
Import React
Const ListTodos function
Export default
Go into index.js and import ListTodos from components
Add it to the index function
Add fragment to ListTodo
Get table tag from bootstrap and add it to ListTodos function
Add table class “table mt-5 text-center”
Make the displays for the table description, edit, delete
Add useEffect and useState to ListTodos
Write use effect function to hit get Todos
Map the data to the bootstrap table
Build the delete button (button classname ‘btn btn-danger’>Delete</button)
Inside todos map add key={todo.todo_id} to get todo id
In delete button add onClick ={() => deleteTodo(todo.todo_id)}
Back at the top of ListTodos create delete function
Build the edit todo component
Inside EditTodo import React from React
Make edit function
Get modal button from bootstrap
Build button just like the the delete
3. Usage:

We undertook to build an intuitive app that harkens back to the days of a paper to do list. Add your todos and a due date and watch them populate to the integrated calander. Check off done items and they will be moved to a new list so you can reference your progress.
4. About the Team

Casey:
Hey I'm Casey. I have been a stay at home mom for a few years and now looking for a change of scenery! I enjoy technology and learning new skills as well as creating and fixing projects. I would love to pursue something with the car industry and software. Here's to a new journey!

Nick:

Nick has been working in IT for over 10 years. He is looking forward to making a career transition into software development, focusing on frontend specialties. When he's not learning new code, Nick enjoys playing guitar and chess, as well as working on projects outside.

Kristen:

Hi there! I am Kristen, a software developer. I am passionate about fitness, reading, and I love to learn about new technologies.

Gregg:

Gregg has spent the last many years opening and developing a venerable local eatery/institution, but has now decided to try his hand at a different kind of development. He likes to debate matters of great import with his adult sons, and is obsessed with electrified stringed instruments.

5. Tech

The team made use of an Express App running React and a PostgreSQL database to keep track of everything, all of which is running in a Node environment. Upon deployment a user should see a seamless app.