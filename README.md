# Workshop 1- Create a free Kubernetes cluster with one worker node and deploy your first app to IBM Cloud.

### To create a free Kubernetes cluster:

1. In the IBM Cloud Catalog, Create a **Continuous Delivery** service

1. In the IBM Cloud Catalog, select Kubernetes Cluster and click Create. A cluster configuration page opens. By default, Free cluster is selected.

2. Give your cluster a unique name and select Geography --> North America && Metro --> Dallas.

3. Click Create Cluster. A worker pool is created that contains one worker node.

**The worker node can take a few minutes to provision, but you can see the progress in the Worker nodes tab. When the status reaches Ready, you can start working with your cluster!**

4. Click on **DevOps** and click on **Create a Toolchain** 

![DevOps](/images/9.png)

5. Click on **Develop a Kubernetes app** 

![DevOps](/images/1.png)

6. In the redirected page, select Dallas as the region for Toolchain and in Delivery pipeline, click CREATE next to **IBM Cloud API Key** and click on **CREATE** the toolchain.

![DevOps](/images/8.png)

![DevOps](/images/7.png)

7. Click Delivery Pipeline and you can see the BUILD, CONTAINERIZE and DEPLOY stage.

![DevOps](/images/6.png)

![DevOps](/images/delivery_pipeline.png)

8. Click on Deploy to Kubernetes within DEPLOY stage.

![DevOps](/images/2.png)

![DevOps](/images/5.png)

9. VIEW the application in the URL mentioned near **VIEW THE APPLICATION AT**


NEXT STEPS:

Let's change the code in app.js by opening ECLIPSE ORION WEB IDE and then push the changes through DELIVERY PIPELINE.

# Workshop 2- Build cloud-native apps faster for Kubernetes with Kabanero

### Pre-requisites

1. Docker Installation- https://docs.docker.com/get-started/
2. Appsody Installation- https://appsody.dev/docs/getting-started/installation

### Steps:

1. First, choose a development stack. To see all the available stacks, run:

``
      $ appsody list
            ``

2. Create a fully functional Appsody project using the nodejs-express stack:

     ```
      $ mkdir my-project
      $ cd my-project
      $ appsody init nodejs-express
      ```

3. Start the development container:

``
      $ appsody run
``

Great! Now the project is running in a docker container, and the container is linked to the project source code on your local system. For nodejs-express, navigate to http://localhost:3000 to see the output.


### Now let's try changing the code!


Edit the file app.js to output something other than "Hello from Appsody!".

``
vi app.js
``

**When you save the file, Appsody picks up the change and automatically updates the container.** Refresh http://localhost:3000 to see the new message!


You now have a containerized application that's ready to deploy to a suitable runtime infrastructure such as a cloud platform that hosts a Kubernetes cluster.


Refer to [deploying your app directly to a Kubernetes cluster](https://appsody.dev/docs/using-appsody/building-and-deploying) for more information on deploying to IBM Cloud Kubernetes cluster.
