# ever-learner
Developer Learning

*Architecture*
*Domain Driven Design (DDD)*

Bounded Context Map
https://vimeo.com/125769142 - Video By Eric Evans


*.Net Core 2*

Introducing .NET Core 2.1 Flagship Types: Span T and Memory T
https://www.codemag.com/Article/1807051/Introducing-.NET-Core-2.1-Flagship-Types-Span-T-and-Memory-T


*Microservices*
https://martinfowler.com/articles/microservices.html

C#

https://www.codemag.com/Article/1807051/Introducing-.NET-Core-2.1-Flagship-Types-Span-T-and-Memory-T


*Docker chect sheet*
* docker build -t friendlyhello .             # Create image using this directory's Dockerfile
docker run -p 4000:80 friendlyhello         # Run "friendlyname" mapping port 4000 to 80
docker run -d -p 4000:80 friendlyhello      # Same thing, but in detached mode
docker container ls                         # List all running containers
docker container ls -a                      # List all containers, even those not running
docker container stop <hash>                # Gracefully stop the specified container
docker container kill <hash>                # Force shutdown of the specified container
docker container rm <hash>                  # Remove specified container from this machine
docker container rm $(docker container ls -a -q)         # Remove all containers
docker image ls -a                          # List all images on this machine
docker image rm <image id>                  # Remove specified image from this machine
docker image rm $(docker image ls -a -q)    # Remove all images from this machine
docker login                                # Log in this CLI session using your Docker credentials
docker tag <image> username/repository:tag  # Tag <image> for upload to registry
docker push username/repository:tag         # Upload tagged image to registry
docker run username/repository:tag          # Run image from a registry
  
https://github.com/docker/machine/issues/4424



Entity Framework Core:
AsNoTracking()
* AsNoTracking() allows the "unique key per record" requirement in EF to be bypassed (not mentioned explicitly by other answers).
* In a nutshell you should use .AsNoTracking() in any Entity Framework query which you intend to use only for reading data. This will ensure minimal memory usage and optimal performance in these cases.
