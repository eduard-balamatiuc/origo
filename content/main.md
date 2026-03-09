1. Who are we? Why are we doing this?
### Course overview 
1. Explaining the outline of the course, and making some introductions on who is this course for. What is the structure of the course (videos + theoretical materials + homeworks + quizzes)
2. Finding your solution.
3. Problems at a hackaton (Isolating your project parts, don't make a login page)
### [[Working on the same code]]
1. Familiarizing with git and github (main git commands). 
2. Creating separate github repos for frontend and backend and adding collaborators, working with `.gitignore`.
3. Branches. Pull requests. Conflicts and resolving conflicts. 
4. Documenting your projects (minimal README.md for front and back)
### Creating the back-end (==Marin==)
1. Initializing the Python project (creating a virtual env, adding requirements, installing necessary libraries).
2. What is Fast API? Launch your first server (create a `main.py` file, where we instantiate `fastapi` and `uvicorn` and launching it).
2. Create first mock endpoint (to return `{message:"Return something"}`). Work with fast api documentation and swagger (`localhost:8000/docs`)
3. Showcase a basic architecture (folder structure) for a project. Why is this important?
4. Decide the theme of the project. Create necessary models and schemas (explain difference between models and schemas).
5. Create your first database connection (using `sqlite` and `sqlalchemy` as ORM). Use Bind, to automatically map the models to the database.
6. Create the CRUD (explain what is CRUD for sanity check) operations while using the creating the schemas and models created (will be divided in two lessons -> authorization CRUD (add explanations about how auth works) and the theme CRUD). 
7. Make the necessary endpoints according to the CRUD operations (if necessary) (can be divided in two lessons -> authorization endpoints and the theme endpoints).
8. Create the middleware for the authorization part. (Additional)
9. Work with exceptions, endpoint responses and response codes (`400`,`401`,`200`). Testing (via postman or `/docs` swagger).
10. Work with external API's (OpenAI, Claude, MongoDB) (can be divided in multiple lessons)
### Databases and containers (==Max==)
1. Concept of containers. Familiarize yourself with `docker`, `docker-compose.yaml` .Write your first `docker-compose.yaml` file. 
2. Main docker commands (`docker compose up`, `docker ps`, `docker volume ls`) (ADDITIONAL)
3. Manage you current Postgres db with dBeaver (since it's the simplest and easiest). Basic SQL commands for testing and internal db manipulations.
4. Connect your Postgres container to the actual backend. Introduce `config.yaml` and `.env`(tho they can be introduced earlier).

### Front-end creation (==Max==)
1. Initialize your front-end. Install node js, npm and rest. Using main front-end commands (`npm`,`create-react-app`, `npm start` or `npm run dev`). Install necessary dependencies (vite, node modules). Use secondary libraries to avoid unnecessary styling (ANT UI or chakra).
2. Divide your front-end folder management in `components`,`pages` and `api` and make your first page and component.
3. NavBar and Footer. Layering.
4. {Here we should include everything that is needed for the website depending on the theme of the project (lists, dropbar, chats) and divide them in lessons}.
5. Using mock data for testing.
6. `api` folder. Start connecting front-end with the back-end (CORS, hosts, and `headers`).
7. Connect all the made components and pages to the back-end (big lesson).
8. Test the front-end for errors, mistakes and dangers (`npm build`).
### Deploying your app (ADDITIONAL) (==Ed==)
1. Deploy the front-end in a few simple steps with Vercel.
2. Start deploying the backend with AWS or use your computer as a host machine (tunneling with `ngrok`).
3. Create your free tier AWS account. 
4. Create your EC2 instance.
5. Clone the back-end repository, install dependencies and with `tmux` launch the db and back-end.
6. Use `ngrok` to create a secure `https` connection and connect it to the front-end.
7. Test the final app.
### Additional points (==ALL==)
1. Open discussion regarding further development. Our personal advices and recommendations. Podcasting (our experience regarding hackatons and shit).