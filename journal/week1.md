# Week 1 — App Containerization
## Week Summary
1. I commited my code after each lecture
2. I followed the tutorial to implement the Notifcation feature both for frontend and backend, also for the postgres and dynamoDB

## Homework Challenges
1. I pushed and tagged an image to dockerhub called nodejs-4-aws-cloud-bootcamp. I also learnt how to multistage in docker. It is very clear to me now but i believe it will be as we progress. Below is the docker repository which contains a normal image tagged "latest" and a multistage image tagged "2.0"
[Docker image](https://hub.docker.com/repository/docker/gerald22/nodejs-repo-4-aws-cloud-bootcamp/general)

2. Learnt how to succesfully install docker on my localmachine through repository through the official link [docker install tutorial](https://docs.docker.com/desktop/install/ubuntu/)

3. I lauched an EC2 instance of ubuntu, installed docker on it and pulled the same image I pushed from my localmachine, then ran the image as a container.
```
docker pull nodejs-repo-4-aws-cloud-bootcamp
```

then to run the image as a container

```
docker run nodejs-repo-4-aws-cloud-bootcamp
```

4. I researched about docker best practices and some included:
- Using the official and verfied reposiory image from dockerhub
- It is better to using an image containing a runtime environment or a language as your base image rather than using an OS image as base image and installing languages as packages
- It is better to use a fixated number tag or version number instead of "latest" as that could change and break code

5. I researched about health check on docker but could not implement it as i didnt full understand it. 
      interval: 60s

```
   healthcheck:
      test: curl --fail http://localhost:8000 || exit 1
      interval: 60s
      retries: 5
      start_period: 20s
      timeout: 10s
```