# Docker-Jenkins-Kubernetes
This TP aims to guide you through the process of creating, containerizing, and deploying an Express.js application with SQLite using Docker and Docker Compose. Additionally, you will learn to automate the CI/CD pipeline using Jenkins to build the Docker image.
## Step 1: Configure the GitLab Project
1. Create a project on GitLab (or GitHub) titled "express-sqlite."
2. Clone the project to your local machine.
3. Configure a GitFlow workflow for the project using your preferred tool.
   
## Step 2: Create Express.js Application with SQLite
1. Navigate to the project directory: `cd express-sqlite`
2. Initialize a Node.js project: `npm init`
3. Install dependencies (Express.js and SQLite): `npm install express sqlite3`
4. Create `app.js` and add the provided Express.js application code. Test it with Postman.

![postman](https://github.com/hadil-kortas/express-sqlite/assets/97675597/d71b616e-a082-4abb-a8a9-032a9f5817e7)

## Step 3: Create Docker Image
1. Create a `Dockerfile` in the project root with the provided content.
2. Build the Docker image: `docker build -t <username>/express-sqlite-app .`
3. Test the Docker image locally: `docker run -p 3000:3000 <username>/express-sqlite-app`
4. Connect to DockerHub and publish the Docker image: `docker push <username>/express-sqlite-app`
   
## Step 4: Docker Compose
1. Create a `docker-compose.yml` file in the project root using the provided example.
2. Run the application with Docker Compose: `docker-compose up`

![docker](https://github.com/hadil-kortas/express-sqlite/assets/97675597/8a36a7a9-50cb-4648-be36-bdf6ee82ab8f)
## Step 5: Jenkins CI/CD
1. Add your DockerHub login to Jenkins. Use the ID `dh_cred`.
2. Create a `Jenkinsfile` in the project root with the provided content.
3. Commit and push the changes to trigger the Jenkins pipeline.
4. Monitor the pipeline execution on the Jenkins dashboard.
   
![pipeline](https://github.com/hadil-kortas/express-sqlite/assets/97675597/8cc7a4e6-39b4-44d3-80c2-08ef05c1d39a)

## Simple Pod

![cap12](https://github.com/hadil-kortas/Docker-Jenkins/assets/97675597/60ae7f8b-89bb-4415-bdca-ad3c52fa28a7)

## Creating a Kubernetes Deployment

![cap13](https://github.com/hadil-kortas/Docker-Jenkins/assets/97675597/777c1e8a-ac1f-4f5e-b01a-452472174a7e)

Exposure via a LoadBalancer after Exposure via a NodePort

![cap14](https://github.com/hadil-kortas/Docker-Jenkins/assets/97675597/736ebf0c-1571-4495-9a50-fbb420eb51b5)



