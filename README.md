## Work in progress
Slides to accompany the basic demo: https://docs.google.com/presentation/d/1PlgcayXFV7-qaGWFoYw7uzbY8QpIjTPOcTwZ57s0NGc/edit#slide=id.g7864721daf_0_0

## Note: ***This only works on a public repo***

Clone the repo, remove the slides link and this section, push to a new repo and make the repo publc. 
1. Create a new public repo on github
2. git clone https://github.com/untitledteamuk/nodejs-cr-helloworld.git
3. cd nodejs-cr-helloworld/
4. git push https://new-repo.git
5. remove the old repo: cd .. && rm -rf nodejs-cr-helloworld/
6. git clone https://new-repo.git

## Pre Reqs

* If you are going to demo step 3 you will need a GKE cluster configured with cloud run for anthos.
* If you are going to demo step 4 you will need a GCE instance that you can RDP into, which also has access to the Cloud Run Service.//will add detail and image later.
* If you are going to demo step 5 you will need a IDE compatible with CloudCode (VSCode or IntelliJ) as well as a device capable of running MiniKube.
* If you are going to demo step 6 you will need to have pre-prepared the Wagtail imgae. //will add detail later.

# Cloud Run Hello World Sample

[![Run on Google Cloud](https://deploy.cloud.run/button.svg)](https://deploy.cloud.run)

This sample shows how to deploy a Hello World application to Cloud Run using the Deploy to Cloud Run Button - we then expand on this to set up Continuous deployment on cloud run.

You will need to configure GKE with Cloud Run for Anthos.

## Step 1

### Press the Button (hold ctrl and press to open a new tab or you leave the repo):

[![Run on Google Cloud](https://deploy.cloud.run/button.svg)](https://deploy.cloud.run)

![image](https://user-images.githubusercontent.com/11318604/128716343-05d6b9ba-0213-4e1c-a616-7e09da6f4d9b.png)

Once cloud shell opens talk through the process on Cloud Shell, building container using Cloud Build,pushing the deployment to GCR then deploying to CR.

![Screenshot from 2021-08-09 15-58-59](https://user-images.githubusercontent.com/11318604/128727893-586280db-8be5-46a8-acb4-35964147e594.png)

Once the deployment is completed press the URL to show it's worked.

![Screenshot from 2021-08-09 15-59-29](https://user-images.githubusercontent.com/11318604/128727925-34721336-302f-4e73-a274-bc70d5d18c0c.png)


## Step 2

### Set Up Continuous Deployment

![image](https://user-images.githubusercontent.com/11318604/128716460-253cee2e-07d6-4f0c-b6e9-60b6c35868c4.png)

* [go to the Google cloud console] (https://console.cloud.google.com/)
* Select Cloud Run under the Serverless options
* here you will see the deployment from step one, click into it
![Screenshot from 2021-08-10 15-12-46](https://user-images.githubusercontent.com/11318604/128883388-f35c70d0-c4fb-4a16-86ed-603e508d24ca.png)
* Select Set Up Continuous Deployment
![Screenshot from 2021-08-10 15-15-45](https://user-images.githubusercontent.com/11318604/128883456-fc41aaac-5300-48a6-8877-e7bc00e1a74c.png)
* Configure the source repositry (this uses Cloud Build)
![Screenshot from 2021-08-10 15-20-40](https://user-images.githubusercontent.com/11318604/128884158-89be5edc-3ffa-4f11-928b-967bf68d9553.png)
* Set the Branch to use and the buildtype (I use a Dockerfile here and Buildpacks for CRfA), press save.
![Screenshot from 2021-08-10 15-24-43](https://user-images.githubusercontent.com/11318604/128884729-5fbf2aa0-0878-4a97-850f-9d9b691460d0.png)
* The Cloud Build Trigger is now being created - I use this as an oppurunity to talk through the CR dashboards and logs as well as showing the YAML section. One completed you will see a build history at the top of the dashboard. Ctrl and Click into this for a new tab.
![Screenshot from 2021-08-10 15-28-34](https://user-images.githubusercontent.com/11318604/128885432-45f883cd-9a77-4682-8549-26e7ed18d9b6.png)
* Make a cahnge to in the index.js file, commit and push the change.
* In the Cloud Build Tab you will now see the build process start - highlight the commit ID on the build reference to help with debugging/auditing of a change if needed. 
![Screenshot from 2021-08-10 15-32-13](https://user-images.githubusercontent.com/11318604/128886106-93a8ebbb-b2fc-4dab-8019-f564cedb7490.png)
* Click into the build and talk through the steps.
![Screenshot from 2021-08-10 15-32-03](https://user-images.githubusercontent.com/11318604/128886376-943e89ea-aee3-40ea-b383-75c89fd65b36.png)
* once the build is showing as complete, highlight the time taken and go to the page opened at the end of step 1 and refresh the page to show the change.
![Screenshot from 2021-08-10 15-36-16](https://user-images.githubusercontent.com/11318604/128886701-04910749-6d74-47f1-9caf-b64510935612.png)
* reenforce all of this was done automatically form Cloud Run


## Step 3

### Deploy on CRfA setp continuous Deployment with buildpacks

![image](https://user-images.githubusecontent.com/11318604/128716559-2f85ec2f-37ef-4a4c-93d5-b75d76d56095.png)
* **A GKE Cluster with Cloud Run for Anthos is required to be pre configured.** I also recommend pre deploying the first service prior to the demo, to jump straight into the Continuous Deployment set up.
*  

## Step 4

### all private (Need a GCE instance with RDP access)

![image](https://user-images.githubusercontent.com/11318604/128716764-907d3955-a76b-408a-8c28-10a25f894794.png)

## Step 5

### CloudCode Goodness

![image](https://user-images.githubusercontent.com/11318604/128716882-dce13846-4c24-4b5d-a94e-02e1cfd5d03f.png)

## Step 6

### Using other cloud services.

![image](https://user-images.githubusercontent.com/11318604/128717042-3fb28a89-8e5d-4ddc-b641-096abc2ba769.png)


