LAB README Objectives
Deploy Stack: docker stack deploy -c docker-compose.yaml  myapp-stack
Scale Out: docker service scale myapp-stack_myfirstwebsite=7
Scale In: docker service scale myapp-stack_mysecondwebsite=2
Remove and Delete Stack and Containers:
- docker stacker rm myapp-stack 
- docker rm 55ef595282a5 (that's just one instance of a container)

-------------------------------------------------------------------------------------------

Docker Build: docker build -t dockercompose:latest .
Docker Run: docker run -d --name composelab -p 4040:4040 dockercompose:latest
URL: http://localhost:4040/

Sample Code:
---
StudentId: 11223344
FirstName: Preveen
LastName:  James
PhoneNumbers:
  - 254-555-1212
  - 789-123-4567
  - 222-333-9876
Addresses:
  - Street: 123 Main Street
     City: Lehi
     State: Utah
  - Street: 456 Maple Road
     City: Draper
     State: Utah
...

services:
	 	mywebsite:
			image: myapp:latest
			ports: 
				- 3000:8080
			deploy:
				replicas: 3


Sample Command: 
- docker stack deploy -c docker-compose.yaml  mywebstack
- docker system info
- docker swarm init


