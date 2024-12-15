# Jenkins Pipeline for Java based application using Maven, SonarQube, Argo CD and Kubernetes

![Screenshot 2023-03-28 at 9 38 09 PM](https://user-images.githubusercontent.com/43399466/228301952-abc02ca2-9942-4a67-8293-f76647b6f9d8.png)


Here are the step-by-step details to set up an end-to-end Jenkins pipeline for a Java application using SonarQube, Argo CD and Kubernetes:

Prerequisites:

   -  Java application code hosted on a Git repository
   -  Jenkins server
   -  Kubernetes cluster
   -  Argo CD

Steps:

    1. Install the necessary Jenkins plugins:
       1.1 Git plugin
       1.2 Maven Integration plugin
       1.3 Docker Pipeline plugin
       1.4 SonarQube plugin

    2. Create a new Jenkins pipeline:
       2.1 In Jenkins, create a new pipeline job and configure it with the Git repository URL for the Java application.
       2.2 Add a Jenkinsfile to the Git repository to define the pipeline stages.

    3. Define the pipeline stages:
        Stage 1: Checkout the source code from Git.
        Stage 2: Build and test the Java application using Maven.
        Stage 3: Run SonarQube analysis to check the code quality.
        Stage 4: Build and Push the Docker Image to the DockerHub.
        Stage 5: Update the manifests repo.

    4. Configure Jenkins pipeline stages:
        Stage 1: Use the Git plugin to check out the source code from the Git repository.
        Stage 2: Use the Maven Integration plugin to build and test the Java application.
        Stage 3: Use the SonarQube plugin to analyze the code quality of the Java application.
        Stage 4: Use the Docker pipeline pulgin to build the and push the Docker Image to the DockerHub
        Stage 5: Update the Manifests repo using Shell Script

    5. Set up Argo CD:
        Install Argo CD on the Kubernetes cluster.
        Set up a Git repository for Argo CD to track the changes in the Kubernetes manifests.

    6. Run the Jenkins pipeline:
       7.1 Trigger the Jenkins pipeline to start the CI/CD process for the Java application.
       7.2 Monitor the pipeline stages and fix any issues that arise.

This end-to-end Jenkins pipeline automates the entire CI process for a Java application, from code checkout to deployment using Kubernetes manifests, while ArgoCD automates the CD process by managing deployments to the Kubernetes cluster.
