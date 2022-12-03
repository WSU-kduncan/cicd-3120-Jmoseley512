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

# Part 3: Deployment

Description of the restart script:

The restart script works by taking a preset token from the user 

Setting up webhook and the server:

webhook install command ```sudo apt instal webhook```

To keep the webhook running I can use both ```systemctl enable webhook``` to make sure it starts at boot and running webhook in a GNU Screen session to have it running the entire time my system is up. 

webhook task definition file: 

The webhook task definiton file is the file which defines to the webhook program what to listen for and what action to take once the target "token" or packet has been received. 

Steps for Github notifier:

In the repository settings 
1. select email settings
2. enter the email desired to be notified for push events

# Part 4: Visualization 

![Workflow](https://github.com/WSU-kduncan/cicd-3120-Jmoseley512/blob/main/images/workflow.png)
