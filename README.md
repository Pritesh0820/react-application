# React-application deployment procedure

step 1 - docker installation ( to create image and container)
         git installation ( to clone the repository)
         kubeadm installation ( to run k8s)

step 2 - git clone https://github.com/MaheshRautrao/React-Todo-list?ref=reactjsexample.com

step 3 - write Dockerfile to create an image of react application (create multi-build file to reduce image size)

step 4 - create image from Dockerfile .
        command - docker build -t reactapplication .

step 5 - create docker container and expose it to the port 80:80 (# to check weather application runs properly)
         command - docker run -d -p 80:80 --name reactapplication reactapplication:latest

step 6 - give tag to docker image to push image in dockerhub repository.
         docker tag reactapplication jhapritesh/reactapplication

step 7 - push the image in GitHub repository.
         docker push jhapritesh/reactapplication

step 8 - write yml file for deployment .

step 9 - write yml file for service . (#to access through internet in our case we used loadBalancer)

step 10 - kubectl apply -f deployment.yml (#execute command for deployment)

step 11 - kubectl apply -f service.yml (#execute command for service)

step 12 - kubectl get deployments (# to check if the deployment is successful)

step 13 - kubectl get pods (# to check if the pods is running state)

step 14 - kubectl get svc (# to check the status of service)

step 15 - kubectl get svc react-application-service (#to get the details of svc and url)

step 16 - 44.210.93.21:31110 (hit this url on web)


This is a React To do list app developed by me to learn and enhance my react skills.

 

  ## Screen-shots
![react-application](https://github.com/user-attachments/assets/4f9d00f3-11f9-4101-bea2-a356b7de0a9f)
![kubernetesdata](https://github.com/user-attachments/assets/c8f3b6e7-f887-4174-9a5c-46f1495651e4)

