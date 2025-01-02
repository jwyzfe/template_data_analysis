## co_data_analysis
#### Main package
- python:3.11
- mongo:7

#### CLI with Dockerfile and compose.xml : duration 150.4s
```
# --project-name is docker container name
~$ docker-compose --project-name data_analysis up -d --build
```
#### connect remote Docker container
```
@ http://localhost:8888/
@ mongodb://localhost:27017/ or mongodb://mongodb:27017/
```
#### samples
- [samples\sample_mongodb_connection.ipynb](./samples/sample_mongodb_connection.ipynb)
