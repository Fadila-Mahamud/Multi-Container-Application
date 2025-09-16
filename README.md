# Multi-Container-Application With Docker
![dockerimage](https://github.com/user-attachments/assets/0a95cc76-7b13-4703-a005-57157683a445)

---

# Overview
Docker enables developers to package applications and their
 dependencies into lightweight, portable containers using a
 Dockerfile. These containers can be linked together using Docker
 Compose, which uses YAML files to configure and manage multi
service setups like a web server and Redis. YAML provides a clear,
 human-readable format for defining services, networks, and
 volumes. Cloud computing, the delivery of computing resources
 over the internet, supports scalable, cost-effective infrastructure
 through models like IaaS, PaaS, and SaaS.
 
 ---
# Create a Project Directory
<img width="636" height="149" alt="image" src="https://github.com/user-attachments/assets/1d363d2a-1d4d-4f4b-8254-b8397845122b" />

Create a project directory to house all necessary files for the 
multi-container application.

---
#  Create a Web Service
<img width="683" height="319" alt="image" src="https://github.com/user-attachments/assets/ca6f1eaa-818d-450a-983b-3827d75167b4" />

<img width="664" height="341" alt="image" src="https://github.com/user-attachments/assets/4e21f89f-b1e4-449c-8284-6a2a5a704845" />

 
 After a project directory is created, proceed to create individual files 
starting with a Dockerfile then the app.py file.

<img width="636" height="123" alt="image" src="https://github.com/user-attachments/assets/c1556738-a66e-457e-9b8c-e658dd39d622" />

- A basic web service is replicated using Python and a dockerfile is written to 
containerize the web service specifying the base image, necessary 
dependencies, and how to run the service.
- To achieve this, a app.py(main app code), Dockerfile and the
 requirements.txt(contains dependencies needed to run the app)  is created with the 
content as shown in the images above


---

# Set Up Redis as a Database
<img width="577" height="263" alt="image" src="https://github.com/user-attachments/assets/f1488368-e6fb-45af-8a06-2b84aac373bb" />

Set up a Redis Database using the official Redis Image from the 
Docker Hub with the script above in the docker-compose.yml file.

---

#  Link Services in Docker Compose
<img width="610" height="267" alt="image" src="https://github.com/user-attachments/assets/cdaaf451-fe37-4847-b506-6c3ca2eec935" />

Edit the docker-compose.yml file to link the web app to the redis database 
using the depends_on key.

---

#  Run and Test
<img width="588" height="324" alt="image" src="https://github.com/user-attachments/assets/06c4049a-eef0-48f3-b5bb-db6c7af84754" />

- To build the container, run the docker-compose up –build command to start the services.
- Confirmed this is successful by checking from the docker desktop app on your local machine.

<img width="750" height="208" alt="image" src="https://github.com/user-attachments/assets/c4892d95-2d3a-464d-b4b4-1a6a1b533aa8" />

 - Again, ensure that the container is running in the background. Then, enter the terminal inside the 
container using the docker-compose exec app shcommand to test connectivity between the web service and 
the Redis database.
 • Here, run the ping redis command. Observe packets being pulled, indicating a successful connection 
between the application and the Redis database.


In further testing of the running container 
services, the various endpoints 
for different checks were employed by testing the GET/POST 
methods in the following slides using the web 
browser.
- Begin by accessing the health of 
the services using 
http://localhost:5000
- The display below shows a message
 welcoming users to the app, 
redis_status as connected indicating a 
successfully linked database and a 
timestamp to log when this request 
was made.

<img width="497" height="358" alt="image" src="https://github.com/user-attachments/assets/1b9f7ed8-8ed5-458a-b733-3d1070ec1d04" />

---



<img width="358" height="291" alt="image" src="https://github.com/user-attachments/assets/a22bf699-8566-4bd4-aba4-aad0eb812756" />


For health checks of the services 
http://localhost:5000/health

<img width="400" height="291" alt="image" src="https://github.com/user-attachments/assets/dc936a5f-fcb9-42e1-ac54-e61a6c56d504" />

 To set Redis values, the name was set to Juliet using 
the path- http://localhost:5000/set/name/Juliet

<img width="392" height="295" alt="image" src="https://github.com/user-attachments/assets/96b43497-3ff5-456a-b5bb-038da48d81be" />

 To test the increment route, the path below was used return
the number of times the page had been visited 
http://localhost:5000/counter

<img width="391" height="300" alt="image" src="https://github.com/user-attachments/assets/e8382ac2-d4dd-4f19-8658-73205dd0c894" />

To get data from the Redis data, the path below was used to 
get the name passed into the db earlier which 
displayed the value 'Juliet' - http://localhost:5000/get/name


---

# Conclusion

 In this project, Docker Compose was used to successfully run 
a multi-container application consisting of a web service and 
a Redis service. 
Defining services using a docker
compose.ymlfile, run containers in the background, and 
verify communication between them using internal 
networking were learnt. 
This project helped to better understand how to manage and link 
multiple services in a containerized environment effectively.










 
