# Step 1:

- http://nisanthsojan.com/django-mysql-with-docker%e2%80%8a-a-step-by-step-guide-for-local-development-part-1/

# Step2 :

- http://nisanthsojan.com/django-mysql-with-docker%e2%80%8a-a-step-by-step-guide-for-local-development-part-2/

```Please follow the step and understand the reason why we are using mysql_native_password
Mysql Version 8 stopped using this and the tutorial tries to fallback to the previous authentication mechanism. It is to be noted that not all servers stops the caching
References
https://dev.mysql.com/doc/refman/8.0/en/caching-sha2-pluggable-authentication.html
https://mysqlserverteam.com/mysql-8-0-4-new-default-authentication-plugin-caching_sha2_password/

To remove a container
docker container rm <containerid>

## Incase you have issues with the mysql you can remove the mysql folder created in the directory
of this project. CAUTION: Once removed or erased data will be lost

**add the volume for the mysql project to the ignore file of git**

```

# Step 3:

https://nisanthsojan.com/django-mysql-gunicorn-nginx-with-docker%E2%80%8A-a-step-by-step-guide/

### Note

```
You rebuild the docker images anytime
    - you make changes to your requirements.txt
    - wants to add a new linux package to the ubunto os
    - wants to copy a file or folder into the ubuntu os
```

### Note

Incase any errors occurs concerning a table no existing, remember you must have migrate your project. To do that using docker commands do the following

- run your docker docker-compose up
- open another command tab and enter the command

```
docker-compose exec app python3 manage.py migrate
```

### Note

If will be using virtualenv in your project, always initiate the environment
before running manage.py runserver. This can be done in your docker-compose-yml

### Note

In nginx

- Remember that port 8000 has been exposed to be used by the django app
- Then the nginx server will map port 8000 in the container to port AAAA in the host "AAAA:8000" . Check the nginx server for comments. To acess http://localhost:AAAA
- Remeber to add app to the list of allowed host in ALLOWED_HOSTS of settings.py, check nginx config file more details
