# AWS

## EC2       

![image](https://user-images.githubusercontent.com/73632896/224479630-3666e517-cb01-41ae-9ff1-32bfb419db0c.png)


- EC2 is one of the most popular of AWS’ offering
- EC2 = **Elastic Compute Cloud** = Infrastructure as a Service
- It mainly consists in the capability of:
    - Renting virtual machines (EC2)
    - Storing data on virtual drives (EBS)
    - Distributing load across machines (ELB)
    - Scaling the services using an auto-scaling group (ASG)
- Knowing EC2 is fundamental to understand how the Cloud works


### EC2 sizing & configuration options

- Operating System (OS): **Linux, Windows or Mac OS**
- How much compute power & cores **(CPU)**
- How much random-access memory **(RAM)**
- How much storage space:
    - Network-attached (EBS & EFS)
    - hardware (EC2 Instance Store)
    - Network card: speed of the card, Public IP address
- Firewall rules: **security group**
- **Bootstrap script** (configure at first launch): **EC2 User Data**

### EC2 User Data

- It is possible to bootstrap our instances using an **EC2 User data** script.
- **bootstrapping** means launching commands when a machine starts
- That script is only **run once** at the instance **first start**
- EC2 user data is used to automate boot tasks such as:
    - Installing updates
    - Installing software
    - Downloading common files from the internet
    - Anything you can think of
- **The EC2 User Data Script runs with the root user**

### Hands-On:
  
- Launching an EC2 Instance running Linux
- We’ll be launching our first virtual server using the AWS Console
- We’ll get a first high-level approach to the various parameters
- We’ll see that our web server is launched using EC2 user data
- We’ll learn how to start / stop / terminate our instance.
