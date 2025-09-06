nextwork-cicd-web-project

This is a simple Java web application created primarily for deployment on an AWS EC2 instance. The project is part of a complete CI/CD pipeline that automates the build, test, and deployment processes using AWS services. Any changes pushed to the GitHub repository are automatically built and deployed to a production environment on EC2.
📘 View Project Documentation Repository
Click here to view documentaion
🎯 Project Objectives

    Set up a Java web application hosted on an EC2 instance.
    Integrate the application with a full CI/CD pipeline using AWS services.
    Automate code deployment to production via GitHub commits.
    Gain hands-on experience with AWS DevOps tools and infrastructure as code.

🧰 Technologies & AWS Services Used

    Java (Amazon Corretto 8)
    Apache Maven (build and dependency management)
    Apache Tomcat (for deployment)
    Git & GitHub (version control)
    AWS CodePipeline – Orchestrates the CI/CD workflow.
    AWS CodeBuild – Builds the project from source.
    AWS CodeDeploy – Deploys the built artifact to EC2.
    AWS CodeArtifact – Manages dependencies (e.g., Maven).
    AWS S3 – Stores build artifacts.
    AWS EC2 – Hosts the Java web application.
    AWS CloudFormation – Provisions infrastructure resources.
    IAM & VPC – Secure and manage resources and access.

📁 Project Structure

nextwork-cicd-web-project/
├── appspec.yml
├── buildspec.yml
├── pom.xml
├── README.md
├── scripts/
│   ├── install_dependencies.sh
│   ├── start_server.sh
│   └── stop_server.sh
├── settings.xml
└── src/
    └── main/
        └── webapp/
            ├── index.jsp
            └── WEB-INF/
                └── web.xml

index.jsp: The main entry point of the web app.

web.xml: Configuration file for the web application.

pom.xml: Maven build file specifying project dependencies.

appspec.yml: Defines how CodeDeploy manages the deployment on EC2.

buildspec.yml: Contains build commands and artifact instructions for CodeBuild.

scripts/install_dependencies.sh: Installs necessary packages and dependencies on the EC2 instance.

scripts/start_server.sh: Starts the application server after deployment.

scripts/stop_server.sh: Stops the application server before a new deployment.

settings.xml: Maven settings file, used for configuring repositories like AWS CodeArtifact.
🚀 CI/CD Pipeline Overview

    Code Commit
        Push changes to the GitHub repository.
    CodePipeline Trigger
        AWS CodePipeline detects the change and triggers the pipeline.
    Build Phase
        CodeBuild compiles the Java project using pom.xml.
        Artifacts are uploaded to an S3 bucket.
    Deployment Phase
        CodeDeploy deploys the build to the target EC2 instance.
        EC2 instance is provisioned via CloudFormation and configured to serve the application.
    Production
        Changes are reflected live on the website hosted on EC2.

📌 Notes

This project is for learning and demonstration purposes only.

No business logic or database layer is included.

Primary focus is on cloud infrastructure, CI/CD automation, and DevOps practice.