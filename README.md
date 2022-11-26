# Allowing Password to EC2 Instance
```
sed -i "s/PasswordAuthentication no/PasswordAuthentication yes/g" /etc/ssh/sshd_config
sudo echo -e "Daeyang1@#\nDaeyang1@#" | sudo passwd ec2-user
```
``` systemctl restart sshd ```
# Changing Port of EC2 Instance
#### The default ssh port for EC2 instance is Port number 22 but we can always change this port for example in this cmd i am going to change the port 22 to port 2220
```
echo 'Port 2220' >> /ect/ssh/sshd_config
```
``` systemctl restart sshd ```
