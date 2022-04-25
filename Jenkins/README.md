## CI/CD

We have run a simple Jenkins container for this purpose

- `docker run -d -p 8999:8080 jenkins:latest`

- Then we need to place all the files needed for deployment in Jenkins container 
  (Ex: Deployment files etc)

- Configure credentails to use AWS commands (EKS etc needs aws credentials)

- Install relevant plugins.

- Configure the Jenkins Pipeline 

*Hit build to check the pipeline*

----------------------------------------------------------------------------------------------------------------------------



![Jenkins-UI](https://user-images.githubusercontent.com/68842056/165119816-566947db-95b6-4c6f-87a2-2e4a7c84be29.png)
