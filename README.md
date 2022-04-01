# Py-ML-Playground
Objective : 
1. Learn ML using Python for personal learning 
2. Share the learning :smile: 
3. Fork this project to your personal Git repo for personalized PlayGround experience!

# Lab Setup
## Pre-requisite 
- docker for desktop is installed
- Pull Py-ML-Playground code to local machine

## Preliminary Setup
1. Go to the root folder of Py-ML-Playground in command line
2. Build and Run Jupyter Server within container 
- Please note building from parent folder and pointing docker file from subfolder.
- This will copy all the folder and notbooks into the container which later visible in jupyter server
```
docker build -t jupyter-server -f ./jupyter-in-docker/Dockerfile .
```
3. Run the Server 
```
docker run -p 8888:8888 jupyter-server 
```
4. Copy and paste the Jupyter server url to your preferred browser

Enjoy the Python ML Playground :smiley:

## Maintenance  :
- Files added or modified in the container may get lost once the container destroyed!

Option 1:
1. Pull the files to local folder
```
docker cp <docker-container-id>:/home/sm/practice-ML-lib-tools/ practice-ML-lib-tools/
```
2. Manual backup the files

Option 2:
1. Create Your GitHub repo and fork the intial docker, jupyter setup.
2. Modify Docker build script to setup Git within continer so that manage changes within container!


