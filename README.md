
## Dockerize a .NET Core App

### Getting started
These instructions will get you a copy of the project up and running on your local machine.
* Prerequisites
* Installation and Run
* Dockerizing the API
* Running The API on Docker


### Prerequisites
The things you need before installing the software.
* .NET Core SDK
* Docker Desktop


### Installation and Run

A step by step guide that will tell you how to get the development environment up and running.

```bash
# Clone this repository
$ git clone https://github.com/EzharAnsari/dockerize-dotnet-app.git

# Go into the repository
$ cd dockerize-dotnet-app

# Install dependencies
$ dotnet restore

# publish
$ dotnet publish -c Release -o out

# Run
$ dotnet run
# or
$ dotnet out/moviesapi.dll
```
### Dockerizing the API
Let’s build the image with the following command.
```bash
# build the image
$ docker build -t moviesapi .

# check the images
$ docker images
```

### Running the Api on Docker
Once the Docker image is built. You can run the image with the following command.
```bash
# run the image
$ docker run -d -p 8080:5000 --name webapp moviesapi

# list of running containers
$ docker ps
```