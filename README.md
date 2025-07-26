#☀️ **ECS_Deployments**
- Deploy three Nginx microservices in ECS Cluster.
#

#☀️ **Requirements**

####  **1: Create ECR Repositories**
`Build & Push Docker Images`
  
<details>
<summary><strong>2: Create ECS Task Definitions</strong></summary>
<p><strong>Step 1:</strong> Create a JSON Task Definition File</p>
<p><strong>Step 2:</strong>Register the Task Definition</p>
  Create the IAM Role
<p><strong>Step 3:</strong> Check the Task Definition was created</p>
  aws ecs describe-task-definition --task-definition service1-task
</details>  


####  **3: Create ECS Cluster & Services**
####  **4: Configure ALB & Path-Based Routing**
####  **5: Implement Monitoring and Healtchecks**
####  **6: Logging**


##- **Execution**

munish@munish-ThinkPad-T480:/$ aws ecr get-login-password --region us-west-2 | docker login --username AWS --password-stdin 975050024946.dkr.ecr.us-west-2.amazonaws.com
Login Succeeded


## Create Cluster
<details>
  <summary><strong>Step1: Create ECS Cluster</strong></summary>

  Run the following command to create an ECS cluster:
 #### - `aws ecs create-cluster --cluster-name muni-microservices-cluster --region us-west-2`
  
  ```bash
  {
  "cluster": {
    "clusterArn": "arn:aws:ecs:us-west-2:975050024946:cluster/muni-microservices-cluster",
    "clusterName": "muni-microservices-cluster",
    "status": "ACTIVE",
    "registeredContainerInstancesCount": 0,
    "runningTasksCount": 0,
    "pendingTasksCount": 0,
    "activeServicesCount": 0,
    "statistics": [],
    "tags": [],
    "settings": [
      {
        "name": "containerInsights",
        "value": "disabled"
      }
    ],
    "capacityProviders": [],
    "defaultCapacityProviderStrategy": []
  }
}
</details> ```


Step 2: Register the Task Definition
Step 2: Check the Task Definition was created
 - `aws ecs describe-task-definition --task-definition service1-task --region us-west-2`




