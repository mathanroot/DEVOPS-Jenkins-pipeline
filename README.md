# jenkins-pipeline

#In this pipeline project I have Create a app.js,package.json and docker file.

#app.js contains javascript file.

#package.json contains packages for the javascript file.

#Dockerfile contains commands execute the Javascript file.

#Jenkinsfile contains pipeline for the project.

#Uploaded to github repo and config the jenkins pipeline 


#In jenkins goto triggers --> GitHub hook trigger for GITScm polling

#Pipeline --> pipeline script from scm, Enter github repo link.

#Add DockerHub Credentials -->

#Go to: Manage Jenkins → Credentials → (global)

#Add Username + Password

#ID: dockerhub-creds (must match Jenkinsfile)


#Then,set Github hook===> GitHub repo → Settings → Webhooks → Add Webhook

#After successfully upload or update the code , it will be pushed to jenkins ..

#Then, Jenkins pust to the images to dockerhub 

#Build the images to local machine and run the images with assigning port , run the local host server......


<img width="1464" height="1092" alt="image" src="https://github.com/user-attachments/assets/1a6eaaf7-f7b7-4f6b-84ba-cd975e7c03ff" />


#With html and js,
<img width="1906" height="1124" alt="image" src="https://github.com/user-attachments/assets/d37b2c38-e17c-4291-9ce1-b48a2a8c8bc9" />





