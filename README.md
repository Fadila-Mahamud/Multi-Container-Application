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






 
