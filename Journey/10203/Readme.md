## INTRODUCTION TO SECURITY GROUPS (SG)

- They control how traffic is allowed into of our EC2 instances (they only contain **allow** rules)
- Rules can reference by IP (where your computer is from) or by other SG
- If more than one rule is specified for a particular port then **the most permissive** rule holds precedence. For example, if you have a Rule 1 that allows access to port 22 from IP address 192.168.0.1 and Rule 2 that allows access to port 22 from everyone, Rule 2 will be effective. Everyone will have access to port 22
- SG are a firewall on our EC2 instances and they're going to regulate:
1. Access to ports
2. Authorised IP ranges - IPv4 and IPv6
3. Control of inbound network (from the outside to the instance)
4. Control of outbound network (from the instance to the outside)

### SG RULES

- There's not a one to one relationship between SG and instances.  SG can be attached to multiple instances, an instance can have multiple SG too
- Are locked down to a Region-VPC combination
- SG live outside the EC2.  If the traffic is blocked the EC2 instance won't even see it
- It's good to maintain one separate SG for SSH access (usually SSH access is the most complicated thing and you really wanna make sure that one is done correctly)
- If your application is not accesible (time out), then it's a SG issue
- Is yoy receive a connection "refused error", then it's an application error or it's not launched
- All inbound traffic is blocked by default
- All outbound traffic is authorised by default

<p align="center">
  <img src="/Journey/10203/sg.PNG" width="750" height="180"></p>

1. Type
2. Protocol.  Protocol that we wish to allow
3. Port Range.  Where the traffic can go through on the instance
4. Source.  To specify the source or destination for the traffic. We can specify a IPv4 address, IPv6 address, range of IPv4 or IPv6 addresses, **another security group** and so on
5. Description.  To add some description to the rule for documentation purposes

### SG ACCESS BASED ON IP ADDRESS

<p align="center">
  <img src="/Journey/10203/sg2.png" width="450" height="180"></p>

As per the rule only our computer with a certain IP address can access the EC2 instance over port 22. All other computers are unauthorized. By default, the outbound access is open.

This approach is known as **Filtering based on IP and Port**

### SG RULES REFERED BY OTHER SG

<p align="center">
  <img src="/Journey/10203/sg3.png" width="450" height="180"></p>
  
We have an EC2 instance with SG1. We have authorized SG1 & SG2 to have inbound access to the same. Now, other EC2 instances associated with SG1 & 2 can access the first EC2 instance. However, the third EC2 instances having SG3 cannot access the first EC2 instance

## CLASSIC PORTS TO KNOW

- 22 = SSH (Secure Shell) - log into a LINUX instance
- 21 = FTP (File Transfer Protocol) - Is used to upload files into a file share
- 22 = SFTP (Secure File Transfer Protocol) - Upload files using SSH
- 80 = HTTP - Access unsecuresd websites
- 443 = HTTPS - Access secured websites
- 3389 = RDP (Remote Desktop Protocol) - log into a Windows instance


