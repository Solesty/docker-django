# Step 1:
- http://nisanthsojan.com/django-mysql-with-docker%e2%80%8a-a-step-by-step-guide-for-local-development-part-1/


# Step2 :
- http://nisanthsojan.com/django-mysql-with-docker%e2%80%8a-a-step-by-step-guide-for-local-development-part-2/

``` Please follow the step and understand the  reason why we are using mysql_native_password
Mysql Version stopped using this and the tutorial tries to fallback to the previous authentication mechanism. It is to be noted that not all servers stops the caching 
References
https://dev.mysql.com/doc/refman/8.0/en/caching-sha2-pluggable-authentication.html
https://mysqlserverteam.com/mysql-8-0-4-new-default-authentication-plugin-caching_sha2_password/

To remove a container 
docker container rm <containerid>

## Incase you have issues with the mysql you can remove the mysql folder created in the directory
of this project. CAUTION: Once removed or erased data will be lost

**add the volume for the mysql project to the ignore file of git**

```
