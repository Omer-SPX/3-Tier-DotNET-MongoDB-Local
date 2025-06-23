# 3-Tier-DotNET-MongoDB-Local
# INSTALL INETSDK 8.0
sudo apt-get update && \
sudo apt-get install -y dotnet-sdk-8.0

# INSTALL INET Runtime

sudo apt-get update && \
sudo apt-get install -y aspnetcore-runtime-8.0

# INSTALL MangoDB
#1. Add MongoDB's GPG Key

curl -fsSL https://www.mongodb.org/static/pgp/server-7.0.asc  | \
sudo gpg --dearmor -o /usr/share/keyrings/mongodb-server-7.0.gpg

#Add MongoDB Repository

echo "deb [ arch=amd64 signed-by=/usr/share/keyrings/mongodb-server-7.0.gpg ] https://repo.mongodb.org/apt/ubuntu  $(lsb_release -cs)/mongodb-org/7.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-7.0.list

#Install MongoDB

sudo apt update
sudo apt install -y mongodb-org

#Start and enable MongoDB:

sudo systemctl start mongod
sudo systemctl enable mongod

# Verify status

sudo systemctl status mongod

# Connect to MongoDB

mongosh

