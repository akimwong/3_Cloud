<p align="left">
  <img src="EC2.png" width="50" height="50">

## EC2
1. To provide Infrastructure As A Service (IAAS) in AWS
2. Can be use as OS Linux, Windows an Mac
3. You can select how much:
- Compute power & cores (CPU)
- RAM
- Storage (network attached EBS-EFS, EC2 instance store)
- Network card (speed of the card and public IP)
- Firewall rules (security group)
- Bootstrap script (EC2 user data, to use at first launch)

### EC2 user data
1. Bootstrapping means launching commands when a machine starts.  
2. That sript is **only run once** at the instant **first start**
3. 'EC2 user data' is used to automate boot task such as:
- Installing updates
- Installing software
- Downloading common files from the internet
- ...
4. The EC2 User Data Script runs with the root user

  
** When you stop an instance and then started again after a little while, the public IPv4 is going to be changed.  So we're going to get a new public IPv4.  The private IPv4 will not have change.
