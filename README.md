# Ruby-Devops

Here we see how we Deploy a sample Ruby application using the major Devops principles.  

------------------------------------------------------------------------------------

## Principles

- I have used certain tools for this purpose, details of which is mentioned in their respective Folder 

  - For example to understand how I have containerised the application on Docker go in _devops/sample_rails_app_ , simlilarly for Infra, Jenkins etc

 ## Outcome

- I have set-up the Ruby-on-Rails application on Docker container and have configured _LogRotate_ too in order to rotate the logs.

- In order to make sure that the Application starts up on failure, Kubernetes is being used to make sure that the state of Application is always Highly available and    Fault tolerant.

- In order to make sure that the Application get deployed Automatically, Jenkins has been used for CI/CD. 

- For the above mentioned Kubernetes Cluster, EKS has been used and in order to provision it I have used Terraform.

- The routing to the application is done by a DNS record which is managed by _Nginx_.

- I have enabled TLS (which also redirects http to https) using the cert and private keys generated by _Lets Encrypt_ 

- The SSL-Labs test gives a Grade A to the Application URL.

----------------------------------------------------------------------------------------------------------------------------------------------------------------

## Results 

1. [The application url](Removed now)


