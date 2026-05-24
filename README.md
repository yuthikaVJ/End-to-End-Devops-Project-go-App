# Go Web Application

This is a simple website written in Golang. It uses the `net/http` package to serve HTTP requests.

## Running the server

To run the server, execute the following command:

```bash
go run main.go
```

The server will start on port 8080. You can access it by navigating to `http://localhost:8080/courses` in your web browser.

## Looks like this

![Website](static/images/golang-website.png)


## Deployement

### Run Container Locally 

#### Build Docker image
```bash
 docker build -t go-app . 
```

#### Run Docker Container
```bash
docker run -d -p 8080:8080 --name go   go-app
```

#### Rename Docker image

```bash 
docker tag go-app:latest <your Docker hub repository>
```

#### upload to Docker Hub

```bash
docker  login
```

##### Push to the Docker hub

```bash
docker push <repo>:tagname
```

