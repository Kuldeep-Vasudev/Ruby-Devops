# K8s Deployment

---------------------------------------------------------------------------------------------------------------------------------------------------

We use the following files in order to make the Deployment reilable and Fault tolerant.

- _*deployment.yaml*_ : This is used to deploy the application in a reliable manner and the state that is declared in this file is maintained as a desired state.

- *_service.yaml_* : This file is used to make the deployment accessible to other in a form of service.

- *_cm.yaml_* : This file is used to store the configurations required for the Deployment.


----------------------------------------------------------------------------------------------------------------------------------------------------

In order to deploy all the objects to K8s we can either use Jenkins CI/CD or do manually as below:

- `kubectl apply -f cm.yaml`
- `kubectl apply -f deployment.yaml`
- `kubectl apply -f service.yaml`

In order to check the status we can run : 

- `kubectl get all` 



