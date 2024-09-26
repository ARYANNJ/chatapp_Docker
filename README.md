This are dockerfille to create images of frontend ,backend and database for django based application 
NOTE: Dont forget to set env variables where needed as they were set during the RUN time
......
docker run -d --name chatapp-backend --network=chatapp-network -e CHATDB=chatapp -e CHATDBUSER=chatapp -e CHATDBPASSWORD=chatapp123 -e CHATDBHOST=chatapp-database chatapp-backend-image:latest
138  ls
  139  docker build -t database-img .
  140  cd ..
  141  cd backend/
  142  docker build -t backend-img .
  143  cd ..
  144  cd frontend/
  145  docker build -t frontend-img
  146  docker build -t frontend-img .
  147  docker images
  148  docker run -it --name mysqldb database-img
  149  docker ps 
  150  docker network create --help
  151  docker network create chatapp-network
  152  docker networks ls
  153  docker network ls
  154  docker run -d --name backend-server --network=chatapp-network -e CHATDB=chatapp -e CHATDBUSER=chatapp -e CHATDBPASSWORD=12345678 -e CHATDBHOST=mysqldb backend-server
  155  docker run -d --name backend-server --network=chatapp-network -e CHATDB=chatapp -e CHATDBUSER=chatapp -e CHATDBPASSWORD=12345678 -e CHATDBHOST=mysqldb backend-img
  156  docker ps 
  157  docker ps -a
  158  docker network connect chatapp-network mysqldb
  159  docker rm backend-server
  160  docker ps -a
  161  docker run -d --name backend-server --network=chatapp-network -p 8000:8000 -e CHATDB=chatapp -e CHATDBUSER=chatapp -e CHATDBPASSWORD=12345678 -e CHATDBHOST=mysqldb backend-img
  162  docker ps -a
  163  docker images
  164  docker run -it --network chatapp-network -p 80:80 --name frontend-nginx  frontend-img
  165  ps -a
  166  docker ps
  167  history
root@ip-18-0-15-76:/home/ubuntu/frontend# 
