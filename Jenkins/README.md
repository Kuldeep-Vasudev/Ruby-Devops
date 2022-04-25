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




![Jenkins UI for Ruby Pipeline](https://user-images.githubusercontent.com/68842056/165151107-9fddab77-74f7-4935-8b98-4f04babdbc41.png)
