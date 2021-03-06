# CI-Using-Jenkins
Integrating the repository with different environments of software production to synchronize the workflow.
![](https://github.com/Aman9026/CI-Using-Jenkins/blob/master/data/images/1_jFpGk7qNLh9kbw_o-WOW1g.gif)

---

**Continuous integration** is a coding philosophy and set of practices that drive development teams to implement small changes and check in code to version control repositories frequently. Because most modern applications require developing code in different platforms and tools, the team needs a mechanism to integrate and validate its changes.
![](https://github.com/Aman9026/CI-Using-Jenkins/blob/master/data/images/1_iKuaNfxgZSTe_J2x3PYRUg.png)

---

Here we will use **Docker, Git-hooks and Jenkins** to showcase a sample DevOps pipeline.
![](https://github.com/Aman9026/CI-Using-Jenkins/blob/master/data/images/1_sHuwGqrg3cNlKkOX9ONUWQ.gif)

## Sample Job-1
If Developer push to **dev** branch then Jenkins will fetch from dev and deploy on **dev-docker** environment.
![](https://github.com/Aman9026/CI-Using-Jenkins/blob/master/DEMO/Job1.gif)

## Sample Job-2
If Developer push to **master** branch then Jenkins will fetch from master and deploy on **master-docker** environment.

*PS: both **dev-docker** and **master-docker** environment are on different docker containers.*
![](https://github.com/Aman9026/CI-Using-Jenkins/blob/master/DEMO/Job2.gif)

## Sample Job-3
Jenkins will check (test) for the website running in **dev-docker** environment. If it is running fine then Jenkins will merge the dev branch to master branch and trigger **#job 2**
For this we need to add two things:
* First ```if sudo curl IP-Of-Dev-Env``` is true we can proceed with merging.
* Add a post build trigger in **Jenkins** for building **#Job2**
![](https://github.com/Aman9026/CI-Using-Jenkins/blob/master/DEMO/Job3.gif)

***You are always welcome to add more or improve any resource in this repository by following [these](https://github.com/Aman9026/CI-Using-Jenkins/blob/master/CONTRIBUTING.md) instructions.***
