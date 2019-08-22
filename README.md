# Workshop 1

## Create a free Kubernetes cluster with one worker node and deploy your first app to IBM Cloud.

### To create a free Kubernetes cluster:

1. In the IBM Cloud Catalog, select Kubernetes Cluster and click Create. A cluster configuration page opens. By default, Free cluster is selected.

2. Give your cluster a unique name and select Geography --> North America && Metro --> Dallas.

3. Click Create Cluster. A worker pool is created that contains one worker node.

**The worker node can take a few minutes to provision, but you can see the progress in the Worker nodes tab. When the status reaches Ready, you can start working with your cluster!**

4. Click on DevOps and click on **Create a Toolchain** 

5. 






# Workshop 2

### Pre-requisites

1. Docker Installation- https://docs.docker.com/get-started/
2. Appsody Installation- https://appsody.dev/docs/getting-started/installation

Steps:

1. First, choose a development stack. To see all the available stacks, run:

``
      appsody list
``

2. Create a fully functional Appsody project using the nodejs-express stack:

``
  mkdir my-project
  cd my-project
  appsody init nodejs-express
``
3. Start the development container:

``
appsody run
``
Great! Now the project is running in a docker container, and the container is linked to the project source code on your local system. For nodejs-express, navigate to http://localhost:3000 to see the output.

Now let's try changing the code!

Edit the file app.js to output something other than "Hello from Appsody!".
``
vi app.js
``

**When you save the file, Appsody picks up the change and automatically updates the container.** Refresh http://localhost:3000 to see the new message!
