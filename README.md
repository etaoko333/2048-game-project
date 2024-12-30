Simple DevOps Project: Deployment of 2048 Game on AWS using Docker
Prerequisites
Project Structure
plaintext
Copy
2048-game/
├── Dockerfile
├── index.html
└── style.css
Step 1: Create index.html
Create a file named index.html and add the following code:

html

Step 2: Create style.css
Create a file named style.css and add the following styles:
css

Step 3: Create Dockerfile
Create a file named Dockerfile and add the following code: Dockerfile

dockerfile
Copy
FROM nginx:alpine
COPY . /usr/share/nginx/html
EXPOSE 80
Step 4: Build and Run the Docker Container Locally (Optional)
Open Terminal and navigate to the project directory:

cd path/to/2048-game
Build the Docker Image:
bash
Copy
docker build -t 2048-game .
Run the Docker Container:
bash
Copy
docker run -d -p 8080:80 2048-game
You can access the game in your browser at http://localhost:8080.
