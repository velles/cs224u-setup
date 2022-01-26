# CS224U Setup with Docker
Docker set up for Stanford Class CS224u. Based on the original non Docker setup [here](https://nbviewer.org/github/cgpotts/cs224u/blob/master/setup.ipynb#Jupyter-notebooks)

In this setup I am using `jupyter lab` not `jupiter notebook`.

# Customization
1. Inside `Docker-Jupiter-build.yml` change `author` to your name

# Set up
1.  Docker 
  - Install [Docker Client](https://docs.docker.com/get-started/overview/) 
  - Have `docker` and `docker-compose` installed (You can check this by doing `docker -v` and `docker-compose -v`)
  
2. Build Custom Image  
    > `docker-compose -f Docker-Jupiter-build.yml build`

3. Run Image    
    > `docker-compose -f Docker-Jupiter-compose.yml -p stanford-classes up -d`

# Access Jupiter Lab
1. Make sure the container is running 

2. Go to http://127.0.0.1:8882

3. Get Initial Token for Lab   
  3.1 Open Docker Dashboard   
  3.2 Go Under stanford-classes -> cs224u-notebook   
  3.3 In the Logs you can see `...?token=MY-TOKEN`

# Other Notes: 
- Notepads are saved under `/work` directory.
- Save Data files under `/work` directory which is mounted and accessible in the docker instance

# Helpful Commands
- SSH into the Docker Instance  
`docker exec -it cs224u-notebook bash`
