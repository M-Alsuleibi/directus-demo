# Instructions and bugs resolved references to view before runing the program: 
1. make a docker user in your local so you can run docker without **sudo**  
2. 
3. docker commands to interact with containers:

    * for every time you add or delete something in the docker-compose file .Its down and up together as i understood it: 
    ``` docker compose up --force-recreate ``` 
    * to log more information during creating the containers: 
    ``` docker compose --verbose up ```
    * to fix this bug [permission error when uploading file #8080](https://github.com/directus/directus/issues/8080) run this before compose up the images: 
    ``` sudo chown -R 1000:1000 ~/[Path to uploads folder] ```
    * to manipulate and see schema and tables inside pg container: 
    ```docker exec -it <pgDB container id> psql -U $DB_USER``` 
    [Ref 1 ](https://stackoverflow.com/questions/57130278/how-can-i-check-postgres-database-in-docker-volume) [Ref 2](https://www.postgresqltutorial.com/postgresql-administration/postgresql-describe-table/)
    * 
   
