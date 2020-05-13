# Task2DevOps
Working with Dockerfile and Jenkins

[![Testing.jpg](https://i.postimg.cc/NMByqr08/Taliger.jpg)](https://postimg.cc/cKk1fCw6)

### Problem Statement
1.	Create container image that’s has Jenkins installed  using dockerfile 

2.	When we launch this image, it should automatically starts Jenkins service in the container.

3.	Create a job chain of job1, job2, job3 and  job4 using build pipeline plugin in Jenkins 

4.	 Job1 : Pull  the Github repo automatically when some developers push repo to Github.

5.	 Job2 : By looking at the code or program file, Jenkins should automatically start the respective language interpreter install image container to deploy code ( eg. If code is of  PHP, then Jenkins should start the container that has PHP already installed ).

6.	Job3 : Test your app if it  is working or not.

7.	Job4 : if app is not working , then send email to developer with error messages.

8.	Create One extra job job5 for monitor : If container where app is running. fails due to any reson then this job should automatically  start the container again.

### Solution

To get started ,we start docker service in hosrt vm.
create a new folder for dockerfile.
the dockerfile i created looks like -
[![dockerfile.png](https://i.postimg.cc/QMPkdZY5/Screenshot-2.png)](https://postimg.cc/PLW8S9jr)

Then save it and we need to build the image
   ```
   docker build -t myjenkins:v1 /pathtodockerfile

   ```
But, there was an error,!
[![Screenshot-3.png](https://i.postimg.cc/WzcG06v1/Screenshot-3.png)](https://postimg.cc/1nMVQFXk)

Tried adding a line to the dockerfile, to run commands after loading-
   ```
   SHELL ["/bin/sh","-lc"}

   ```


I was unable to solve this , so i couldnt continue with the jenkins jobs:( I will keep looking to solve it and update my readme.
