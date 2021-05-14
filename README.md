Command to run docker image in the backgrund 

docker run -d -it -v /Users/manjur/Project/inputdata:/csvserver/inputdata --name csvserver infracloudio/csvserver:latest


manjur@MacBook-Pro Project % docker ps
CONTAINER ID        IMAGE                           COMMAND                  CREATED             STATUS              PORTS               NAMES
8a9df676f7b3        infracloudio/csvserver:latest   "/csvserver/csvserver"   4 seconds ago       Up 3 seconds        9300/tcp            csvserver


manjur@MacBook-Pro shipmunk % docker ps
CONTAINER ID        IMAGE                           COMMAND                  CREATED             STATUS              PORTS               NAMES
8a9df676f7b3        infracloudio/csvserver:latest   "/csvserver/csvserver"   12 minutes ago      Up 12 minutes       9300/tcp            csvserver
manjur@MacBook-Pro shipmunk % docker logs csvserver
2021/05/08 10:52:03 listening on ****

[root@8a9df676f7b3 csvserver]# curl http://localhost:9300/raw
Y3N2c2VydmVyIGdlbmVyYXRlZCBhdDogMTYyMDQ3MTEyMw==
CSVSERVER_BORDER: nil
