Open the monorepo folder you will be presented with 
- "backend" folder 
- "frontend" folder
- compose-spec.json file
- docker-compose.yml file

Run the following services in the monorepo folder in the order below:
1. docker-compose up --build mysql
2. docker-compose up --build backend
3. docker-compose up --build frontend

Run the App: http://localhost:3000/login

username: admin@admin.com
password: password

