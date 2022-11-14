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
