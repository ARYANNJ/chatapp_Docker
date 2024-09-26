This are dockerfille to create images of frontend ,backend and database for django based application 
NOTE: Dont forget to set env variables where needed as they were set during the RUN time
......
docker run -d --name chatapp-backend --network=chatapp-network -e CHATDB=chatapp -e CHATDBUSER=chatapp -e CHATDBPASSWORD=chatapp123 -e CHATDBHOST=chatapp-database chatapp-backend-image:latest
