Ici, on vous guide à travers le processus de construction d'une image Docker pour exécuter une application Spring Boot.

Prérequis: 
		1. JDK 1.8 ou plus récent
		2. Dernière version de Maven
		3. Dernière version de Docker

Suivez les étapes ci-dessous dans l'ordre.

- Exécutez la commande ci-dessous pour créer et démarrer l'application Spring Boot.

        $ ./mvnw package && java -jar target/hello.jar

- Connectez-vous à http://localhost:8080 pour voir votre message "Hello Docker World".


- Pour conteneuriser l'application Hello World (référez-vous au Dockerfile pour plus de détails), exécutez les commandes ci-dessous qui construiront une image Docker sous le nom docker-spring-boot:1.0

		$ ./mvnw spring-boot:build-image

- Run the docker image with the below cmd
	
		$ docker run -p 8081:8080 -t docker-spring-boot:1.0

- Connectez-vous à http://localhost:8081 pour voir votre message "Hello Docker World".

- Ici, 8081 est le port Docker et 8080 est le port Tomcat où s'exécute l'application Spring Boot. 


contactez ricken.bazolo@gmail.com pour plus de détails et pour toute question. 


			
