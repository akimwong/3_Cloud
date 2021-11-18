## INTRODUCTION TO SECURITY GROUPS

- They control how traffic is allowed into of our EC2 instances (they only contain **allow** rules)
- Rules can reference by IP (where your computer is from) or by other security groups 
- Security groups are a firewall on our EC2 instances and they're going to regulate:
1. Access to ports
2. Authorised IP ranges - IPv4 and IPv6
3. Control of inbound network (from the outside to the instance)
4. Control of outbound network (from the instance to the outside)

- Security Group Rules:
<p align="center">
  <img src="/Journey/10203/sg.PNG" width="750" height="180"></p>
1. Type
2. Protocol
3. Port Range.  Where the traffic can go through on the instance
4. Source.  IP address range
