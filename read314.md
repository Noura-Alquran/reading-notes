# Readings: Django REST Framework & Docker Summary 
## Docker
* Docker is a containerization tool used for spinning up isolated, reproducible application environments.
* Docker is really just Linux containers which are a type of virtualization.
* **How could multiple programmers use the same single machine?** The answer was virtualization and specifically virtual machines which are complete copies of a computer system from the operating system on up.**But** *What’s the downside to a virtual machine?* Size and speed. A typical guest operating system can easily take up 700MB of size. So if one physical server supports three virtual machines, that’s at least 2.1GB of disk space taken up along with separate needs for CPU and memory resources.
* **How do the virtual environments differ from containers?** 
    - Virtual environments are used to isolate Python software packages locally. We can create an isolated box for individual projects so one can use Python 2.7 and Django 1.5 while another can use Python 3.5 and Django 2.1 on the same computer. Virtual environments are great.

    - But…virtual environments can only isolate Python packages. They still rely on a global, system-level installation of Python albeit they can refer to the proper version. So when we use Python 2.7 in a project, we’re pointing to an installation of Python 2.7 on the computer itself, not actually within the virtual environment.
* **Why Docker ?**
    * With Docker it doesn’t matter if you are using a Mac, Windows, or Linux computer anymore. The entire development environment is isolated: programming language, software packages, databases, and more. 
    * With Docker we now longer have to mess around with virtual environments. We can faithfully reproduce a production environment locally.
    * And Docker can be shared among team members so everyone is working on the same setup. Wins all around.
* **Install Docker**
    * download the desktop add and create account 
    * sudo pip install docker-compose
    * check versions >> **docker --version** / **docker-compose --version**
    * To confirm Docker installed correctly we can run our first command **docker run hello-world**. This will download an official image and then run the container.
    *  to inspect Docker run **docker info**

* Images and containers are the two fundamental concepts to grasp when you start with Docker. An image is a snapshot in time of what a project contains. A container is a running instance of the image.
* **Dockerfile** is a list of instructions for creating an image
* Images are made up of one or more layers
* Containers are a running instance of an image
* docker-compose.yml controls how to run the container
* Containers are stateless and ephemeral in nature. We can link the local filesystem

## Django REST Framework 
* Django REST Framework works alongside the Django web framework to create web APIs. We cannot build a web API with only Django Rest Framework; it always must be added to a project after Django itself has been installed and configured.
* **The differences between traditional Django and Django REST Framework** >> The most important takeaway is that Django creates websites containing webpages, while Django REST Framework creates web APIs which are a collection of URL endpoints containing available HTTP verbs that return JSON.
