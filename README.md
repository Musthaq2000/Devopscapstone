This repo contains the instructions and source code for the Capstone project, below steps have been executed to get the desired output.
Problem Statement:

ASI Insurance is facing challenges in improving the SLA to its customers 
due to its organizational growth and existing monolithic application 
architecture. It requires transformation of the existing architecture to a 
microservice application architecture, while also implementing DevOps 
pipeline and automations. 
The successful completion of the project will enable ASI Insurance to 
improve its overall application deployment process, enhance system 
scalability, and deliver better products and services to its customers.

Task to be performed:

1. Create the Dockerfile, Jenkinsfile, Ansible playbook, and the source file of 
the static website
2. Upload all the created files to GitHub
3. Go to the terminal and install NodeJS 16
4. Open the browser and access the Jenkins application
5. Create Jenkins pipeline to perform CI/CD for a Docker container
6. Create Docker Hub Credentials and other necessary pre-requisites before 
running build
7. Set up Docker remote host on AWS and configure deploy stage in pipeline
8. Execute Jenkins Build
9. Access deployed application on Docker container


Procedure:

---> launch the LMS lab for capstone project 
---> NOTE: this lab has the below app installed 
1. jenkins 
2. git
3. docker 
----> clone the below git repo using git clone command 
cmd: git clone https://github.com/GithubResources1/InsuranceManagement.git
---> make changes to the jenkinsfile and ansible-playbook.yml as per the below screenshot
---> create a new repo in github with your account and upload the files to the new created repo and verfiy as per the below screenshot 
CMD: git clone https://github.com/Musthaq2000/Devopscapstone.git
---> install nodejs 16 using below commands and validate:
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash 
source ~/.bashrc
nvm list-remote
nvm install v16.14.0
nvm list
node --version
---> access jenkins from the browser in console localhost:8080
---> credentials for the jenkins Username: admin password: admin
---> install maven plugin via Mangae jenkins --> plugin option
---> congfigure maven for jenkins via Manage jenkins --> tools--> maven installations --> add the Maven path as per the configuration in the LMS lab
---> Add docker credentials to the jenkins via --> manage jenkins --> credentials --> Global credentials --> add new Credentials 
---> Verify the specific credential docker account ID is updated in Jenkins file 
---> Before providie specific permissions to maven and docker sock file  using below command 
   1. chmod 777 /usr/share/maven 
   2. chmod 777 /var/run/docker.sock
---> Create a pipeline using selecting New item in dashboard and name the project and click on pipeline and proceed further 
---> Add the specific repo to the pipeline and branch accordingly 
----> click save and proceed for the build by clicking Build now option
----> Note: Build may take more than a minute to complete, once done confirm the build status via console output.
---> verify whether the docker file is available in your docker hub account 
---> Once Docker container is deployed using server IP address and port 8081 to access application

