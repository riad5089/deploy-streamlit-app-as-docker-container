# deploy-streamlit-app-as-docker-container

1. Install required dependencies on local:

```commandline
$ pip install -r requirements.txt
pip install -r requirements.txt
```


2. Test the streamlit app on local:

```
$ streamlit run app.py
streamlit run app.py
```


@@ -27,14 +27,14 @@ $ streamlit run app.py
4. Start Docker:
- Linux (Home Directory):
  ```
  $ sudo systemctl start docker
  sudo systemctl start docker
  ```
- Windows: You can start Docker engine from Docker Desktop.

5. Build Docker image from the project directory:

```commandline
$ sudo docker build -t Image_name:tag .
sudo docker build -t Image_name:tag .
```

### (Note: Rerun the Docker build command if you want to make any changes to the code files and redeploy.)
@@ -44,7 +44,7 @@ $ sudo docker build -t Image_name:tag .
6. witch to Home Directory:

```
$ cd ~
cd ~
```
List the built Docker images
```
@@ -53,27 +53,27 @@ $ sudo docker images

7. Start a container:
```commandline
$ sudo docker run -p 80:80 Image_ID
sudo docker run -p 80:80 Image_ID
```

8. This will display the URL to access the Streamlit app (http://0.0.0.0:80). Note that this URL may not work on Windows. For Windows, go to http://localhost/.

9. In a different terminal window, you can check the running containers with:
```
$ sudo docker ps
sudo docker ps
```

10. Stop the container:
 - Use `ctrl + c` or stop it from Docker Desktop.

11. Check all containers:
 ```
 $ sudo docker ps -a
 sudo docker ps -a
 ```

12. Delete the container if you are not going to run this again:
 ```
 $ sudo docker container prune
 sudo docker container prune
 ```

### Pushing the docker image to Docker Hub
@@ -84,17 +84,17 @@ $ sudo docker ps

15. Log in to Docker Hub from the terminal. You can log in with your password or access token.
```
$ sudo docker login
sudo docker login
```

17. Tag your local Docker image to the Docker Hub repository:
 ```
 $ sudo docker tag Image_ID username/repo-name:tag
 sudo docker tag Image_ID username/repo-name:tag
 ```

17. Push the local Docker image to the Docker Hub repository:
 ```
 $ sudo docker push username/repo-name:tag
 sudo docker push username/repo-name:tag
 ```

(If you want to delete the image, you can delete the repository in Docker Hub and force delete it locally.)