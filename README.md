# kafka-windows10

Having trouble with getting kafka and zookeeper work in docker on windows 10.  So, have to run both without docker


## lessons learned

1. Name of install path needs to be short, so c:\kafka.  Otherwise, start.bat will have issues with max path length.
2. Update server.properties with
   listeners=PLAINTEXT://localhost:9092
   log.dirs=C:\kafka\logs
3. go to bin/window
   kafka-server-start.bat  ..\\..\config\server.properties
