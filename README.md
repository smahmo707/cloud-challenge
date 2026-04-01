# Cloud Engineer Intern Coding Challenge

## Instructions to run locally
1. Make sure Docker Desktop is installed and running.
2. Open a terminal in the project folder.
3. Run:

docker compose up --build

4. Open this in your browser: 
  https://localhost 

## Design choices
I wanted to keep things simple and clear:

- I used Flask because it’s lightweight and quick to set up
- I used Nginx to handle HTTPS and forward requests to the Flask app
- I used Docker Compose to run both services together 

## What I would improve with more time
If I had more time, I would:

- Use a real SSL certificate (like Let’s Encrypt)
- Add logging to track requests
- Use environment variables instead of hardcoding values
- Improve security for a production-ready setup

## AI tools used
I used ChatGPT to help guide the structure of the project and assist with Docker, Nginx, and HTTPS configuration.

## cloud Deployment
To deploy this in the cloud, I would use a service like AWS:

- Run the containers using ECS or EC2
- Use a load balancer to handle HTTPS with a trusted certificate
- Store sensitive data (like keys) using a secure service such as AWS Secrets Manager

## Why storing a private SSL key in a repository is bad
Private SSL keys should always be kept secret. If a private key is exposed in a repository:

- Someone could pretend to be your service
- Secure connections could be compromised
- User data could be at risk

