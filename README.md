# Comment Dockeriser une Architecture de Microservices avec Docker et Spring Cloud

Cela nous permet d'automatiser le processus de démarrage des microservices.

## Étapes à suivre :

1. **Générer un fichier exécutable .jar avec la commande :**
   ```bash
   mvn clean package -DskipTests

### Creer un fichier DockerFile Pour chaque Microservice : 
![Dockerfile](https://github.com/Bouchghel/Dockerize-Microservices/assets/93221225/f46ea69a-df55-428f-9544-b9b4470797ac)  

### Intégrer Docker Compose en créant un fichier DockerCompose.yml :
Pour éviter d'avoir à lancer les commandes : docker build, docker run à chaque fois.  
![DockerCompose yml](https://github.com/Bouchghel/Dockerize-Microservices/assets/93221225/4321d8f8-3643-4311-8720-990ca9707e2d)  
![DockerCompose yml2](https://github.com/Bouchghel/Dockerize-Microservices/assets/93221225/8393c476-5588-43f5-b2f0-5f4ca9fce770)

### Demmarer Docker : et lancer la commande : 
#### docker compose up -d --build
![microServices](https://github.com/Bouchghel/Dockerize-Microservices/assets/93221225/1c299dc1-2254-410d-8a32-6d5871ad15eb)  
![Cap](https://github.com/Bouchghel/Dockerize-Microservices/assets/93221225/7fdb4c2e-55a0-46cf-ad80-4e3080a71408)

### Passant maintenant a la partie FrontEnd
Premierement c'est de generer le build :  
On a integrer cette etape directement dans le Dockerfile :  
![Dockerfile FrontEnd](DockerfileAngular.PNG)  

#### Automatiser le process de docker build , docker run  :  
en modifiant DockerCompose.yml :  
![DockerComposeFront](<DockerCompose.yml FrontEnd.PNG>)  

### Pour lancer l'app :  
   ```bash
   docker compose up -d --build



