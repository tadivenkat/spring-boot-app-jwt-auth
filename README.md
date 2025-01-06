```
$ git clone https://github.com/tadivenkat/spring-boot-app-jwt-auth.git
$ cd to project root directory
$ docker compose up -d
$ mvn clean install
$ java -jar target/runners-1.jar
To build a docker image and push to docker hub:
$ mvn spring-boot:build-image -DDOCKER_USERNAME=YOUR_DOCKER_USERNAME -DDOCKER_PASSWORD=YOUR_DOCKER_PASSWORD
Available unsecured endpoints:
1. POST http://localhost:8080/register
{
   "username": "venkat",
   "password": "password"
}
2. POST http://localhost:8080/login
{
   "username": "venkat",
   "password": "password"
}
Available secured endpoints:
Authentication required. You need to provide the bearer token in the Authorization requestheader.
3. POST http://localhost:8080/runs
{
  "title": "first run",
  "miles": 7,
  "startedOn": "2024-12-19T06:24:12",
  "completedOn": "2024-12-19T07:30:30",
  "location": "INDOOR"
}
4. GET http://localhost:8080/runs
5. GET http://localhost:8080/runs/{id}
6. PUT http://localhost:8080/runs/{id}
{
  "title": "first run",
  "miles": 7,
  "startedOn": "2024-12-19T06:24:12",
  "completedOn": "2024-12-19T07:30:30",
  "location": "INDOOR"
}
7. DELETE http://localhost:8080/runs/{id}
8. GET http://localhost:8080/users
9. GET http://localhost:8080/users/{id}
```
