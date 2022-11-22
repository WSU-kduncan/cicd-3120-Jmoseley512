# cicd-3120-Jmoseley512

Documentation:

Overview: 

THe goal of this project is to containerize an application with docker, Automate the project pipeline with GitHubActions. 
And finally use webhooks to keep prouduction up to date.


# Run Project Locally
How docker was installed:

I am currently running on an arch linux based system. The installation was simply:
```sudo pacman -S docker```
To have docker-CLI installed on my system

How to build container from the docker file: 
```docker build -t [dockerfile]```

How to run the container:

```docker run -dit --name project-5-server -p 8080:80 Dockerfile-P5```

How to view project running:

Navigate to the ip address in a browser to see the running website

# Part 2: Github Actions and DockerHub

To create a public repo on dockerhub, first an account must be created. After that on the front page follow the link to create a public repo. 
When naming ensure only lowecase alphanumeric characters are used. Once it has been appropariatly named click ```create public repo``` and the repository is created. 

How to authenticate in Docker CLI: The credentials provided are the dockerhub username and the access token for the account

Github secrets: The secrets configured are the dockerhub username in one secret. And the dockerhub Access token in another, NOT the password.

Github workflow: THis executes an automated set of commands a user defines. These run when the repository is committed to, or if the user has set it to do so, on user command to avoid the pushing setp. 

The custom workflow variables which someone would need to change would be the names of the images 

