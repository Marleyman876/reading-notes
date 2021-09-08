# Django REST Framework & Docker

* Docker is really just Linux containers which are a type of virtualization.

* Docker is a containerization tool used for spinning up isolated, reproducible application environments. It is a popular development tool for Python developers.

* A good command to inspect Docker is ```docker info```.

* Dockerfiles are read from top-to-bottom. The first instruction must be the ```FROM``` command which lets us import a base image to use for our image. This base image could be another Docker image or one we create entirely from scratch.

* Image layering exists for two main reasons. First, each image layer is immutable–unchanged–like a git commit. This helps ensure consistency when two developers build the same image. The second reason is performance. Docker caches the steps in a ```Dockerfile``` to speed up subsequent builds. When a change is made to a step, all steps following it will be executed from scratch.

For more reading on how to create your own images using docker click [here.](https://realpython.com/python-versions-docker/#using-docker).
