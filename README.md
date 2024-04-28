# db2community
The Free DB2 Community Container Image

This is the free DB2 Community Image, I rebuilt from the IBM Container Registry making it available on Docker Hub for many folks to download and use..

It has the DB2 Sample Database pre-installed and ready to go. Instructions given below.

Pull the image
docker pull anilmahadev/db2community

Run the image:
**docker run -h db2server --name db2server --restart=always --detach --privileged=true -p  50000:50000 -v <host data directorypath> :<container data directory path> /database anilmahadev/db2community:latest**


I have used /database for the container data directory path.

Connect using your favorite DBAdmin tool to connect to the container:
Here are the key elements:

**Hostname: localhost /0.0.0.0

User: db2inst1

Password: db2rocks

Port: 50000

**

Once connected.

Make sure you switch to the db2inst1 user and run the command

**db2 connect to SAMPLE
**

You should get a message like this.

**[db2inst1@db2server /]$ db2 connect to sample

Database Connection Information

Database server = DB2/LINUXX8664 11.5.9.0 SQL authorization ID = DB2INST1 Local database alias = SAMPLE**

**Congratulations! You can now enjoy the FREE To use DB2 Community Edition! Now on Docker Hub!**

Enjoy!
