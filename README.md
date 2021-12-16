# VPC and CICD Task

## Diagram
![diagram](images/jenkinsvpc.png)

## SetUp Jenkins EC2
- Install Java and JDK, [click here for Java installation guide](https://www.digitalocean.com/community/tutorials/how-to-install-java-with-apt-on-ubuntu-18-04#installing-specific-versions-of-openjdk)
- Install Jenkins and dependencies, [click here for Jenkins installation guide](https://www.digitalocean.com/community/tutorials/how-to-install-jenkins-on-ubuntu-18-04) 
- Set up Jenkins within EC2 instance and then enter Jenkins using EC2 Instance, `http://publicIP:8080`
- After installing nodejs, configure global tools and give nodajs a name and select said node within the build. 

## Jenkins NPM Test
- Start the pipeline with a test build to ensure any changes made to the repo passes the built in tests for the application. 
- Once this build passes, move on to the next build. 

## App SetUp
![app code](images/app_code.PNG)
- App instance up and running and jenkins build can initialise app to be viewed on web browser using the app EC2 instance IP, reverse proxy removes the need to enter `IP:3000`. 

## DB SetUp
![DB Code](images/db_code.PNG)
- After running pm2 start app.js on console, the /posts web page loads the database. 
