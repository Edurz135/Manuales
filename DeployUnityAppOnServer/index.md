# Allow SSH on Server
## Install
```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install openssh-server
```

## Enable SSH
```
sudo systemctl enable ssh
```
Open port 22 for ssh:
``` 
sudo ufw allow ssh
```
Start SSH
```
sudo systemctl start ssh
```

## More Commands
```
sudo systemctl stop ssh
sudo systemctl restart ssh
sudo systemctl status ssh
```
Extracted from: https://www.cyberciti.biz/faq/how-to-install-ssh-on-ubuntu-linux-using-apt-get/ 

# Transfer Unity App to Server
## Connect via SSH
Option `-l` indicate the user
Option `-P` indicate the port
```
ssh ip_address -l [user] -P [port]
```
Transfer the file (.zip) to the server
```
scp [options] local-file [user@]ip-host[:remote-file]
```
## Unzip the file
Install unzip on the server
```
sudo apt install unzip
```
Extract the .zip on the same directory with
```
unzip file
```

## Run the app
Inside the Unity Server App folder, look up to `.x86_64` and give it privileges:
```
chmod +x file.x86_64
```
Run the app
```
./file.x86_64
```
## Monitor the server
```
top
```