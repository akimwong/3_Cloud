## INTRODUCTION TO SECURITY GROUPS (SG)

- They control how traffic is allowed into of our EC2 instances (they only contain **allow** rules)
- Rules can reference by IP (where your computer is from) or by other SG 
- SG are a firewall on our EC2 instances and they're going to regulate:
1. Access to ports
2. Authorised IP ranges - IPv4 and IPv6
3. Control of inbound network (from the outside to the instance)
4. Control of outbound network (from the instance to the outside)

### SG RULES REFERED BY IP
<p align="center">
  <img src="/Journey/10203/sg.PNG" width="750" height="180"></p>

1. Type
2. Protocol
3. Port Range.  Where the traffic can go through on the instance
4. Source.  IP address range

<p align="center">
  <img src="/Journey/10203/sg2.png" width="450" height="180"></p>
  
- There's not a one to one relationship between SG and instances.  SG can be attached to multiple instances, an instance can have multiple SG too
- Are locked down to a Region-VPC combination
- SG live outside the EC2.  If the traffic is blocked the EC2 instance won't even see it
- It's good to maintain one separate SG for SSH access (usually SSH access is the most complicated thing and you really wanna make sure that one is done correctly)
- If your application is not accesible (time out), then it's a SG issue
- Is yoy receive a connection "refused error", then it's an application error or it's not launched
- All inbound traffic is blocked by default
- All outbound traffic is authorised by default

### SG RULES REFERED BY OTHER SG


<p align="center">
  <img src="/Journey/10203/sg3.png" width="450" height="180"></p>
  
We have an EC2 instance with SG 1. We have authorized SG 1 & 2 to have inbound access to the same. Now, other EC2 instances associated with SG 1 & 2 can access the first EC2 instance. However, the third EC2 instances having SG 3 cannot access the first EC2 instance
