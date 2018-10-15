# demodockerwebapplication

This is a demo web application


# Remove images
docker rmi $(docker images -q) --force
docker images


cd DockerDemo/demodockerwebapplication/DemoDockerWebApplication/DemoDockerWebApplication

git clone https://github.com/bhoobal/demodockerwebapplication.git


git pull

docker build -t mydemowebapp:latest .

docker images
docker build -t mydemowebapp .

docker run -p 8080:80 9aa773253c3c

docker run -p 8080:80 --name myapp 9aa773253c3c

# Push image to docker repo
docker login

docker tag bc1b481b9f0c bhoobal/mydemowebapp:latest
docker push bhoobal/mydemowebapp


docker pull bhoobal/mydemowebapp


#Versioning
docker tag bc1b481b9f0c bhoobal/mydemowebapp:v1.0
docker tag bc1b481b9f0c bhoobal/mydemowebapp:v1.1
docker push bhoobal/mydemowebapp:v1.1








