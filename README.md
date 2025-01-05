```
$ git clone https://github.com/tadivenkat/spring-boot-app-with-postgresqldb.git
$ cd to project root directory
$ mvn clean install
$ java -jar target/runners-1.jar    
Available endpoints:
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
3. GET http://localhost:8080/runs
Authentication required. You need to provide the token in the Authorization header.
This will get the list of runners registered in the database
Check other endpoint in Controllers
```
