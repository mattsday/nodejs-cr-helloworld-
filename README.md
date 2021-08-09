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

## Step 3

### Deploy on CRfA setp continuous Deployment with build packs

![image](https://user-images.githubusercontent.com/11318604/128716559-2f85ec2f-37ef-4a4c-93d5-b75d76d56095.png)

## Step 4

### all private (Need a GCE instance with RDP access)

![image](https://user-images.githubusercontent.com/11318604/128716764-907d3955-a76b-408a-8c28-10a25f894794.png)

## Step 5

### CloudCode Goodness

![image](https://user-images.githubusercontent.com/11318604/128716882-dce13846-4c24-4b5d-a94e-02e1cfd5d03f.png)

## Step 6

### Using other cloud services.

![image](https://user-images.githubusercontent.com/11318604/128717042-3fb28a89-8e5d-4ddc-b641-096abc2ba769.png)


