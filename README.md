# mongodb-docker using docker-compose
1. Run 'docker-compose up -d'
2. Access mongo container bash: 'docker exec -it <container name or id> mongo'
3. Access mongo shell: 'mongosh'
4. Stop 'docker-compose down'

If you want to create your own image and use that to run MongoDB:
1. Create Dockerfile (use base image like node, set directories, install dependencies, expose ports, define command to run when start) 
2. Build image using that Dockerfile, e.g. 'docker build -t my-mongo-db-image .'
3. Run it by name, in background and port: 'docker run --name my-mongo-db-app -d -p 27017:27017 my-mongo-db-image'
