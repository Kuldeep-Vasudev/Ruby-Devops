# Application 

In order to make the Application Cloud Agnostic we have dockerized the Application 
(Ref in sample_rails_application/Dockerfile)

------------------------------------------------------------------------------------------------------------------------

In order to build the application run below commands 

- `docker build . -t <image-name>:<tag-name>`

_At this point we will have an image built which we can refer in the K8s/deployment.yaml or run manual commands to deploy_

- `docker run -d -p 3800:3800 <image>:<tag>`

To confirm run the below command:

- `docker ps`

Also to check if the application was properly deployed or no run below command:

- `curl -v localhost:3800`


------------------------------------------------------------------------------------------------------------------------

## Log Rotate 

We have installed and configured _logRotate_ 

It configures the schedule or time that we need to keep rotating our logs in **/etc/logrotate.conf**
