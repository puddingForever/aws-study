## EC2 기초

### Amazon EC2

- EC2 is one of the most popular of AWS's offering
- EC2 = Elastic Compute Cloud = Infrastructure as a Service
- Consists in the capability of
  - Renting Virtual Machines(EC2)
  - Storing data on virtual drives (EBS)
  - Distributing load across machines (ELB)
  - Scaling the services using an auto-scaling group (ASG)

### EC2 sizing & configuration options

- Operating System : Linux, Windows or Mac OS
- How much compute power & cores (CPU)
- How much random-access memory(RAM)
- How much storage space :
  - Network-attached (EBS & EFS)
  - hardware (EC2 Instance Store)
- Network card : Speed of the card, Public IP address
- Firwall rules : security group
- Bootstrap script (configure at first launch) : EC2 User Data

### EC2 User Data

- It is possible to bootstrap our instances using an EC2 User Data script
- boostrapping means launching commands when a machine starts
- That script is only run once at the instance first start
- EC2 user data is used to automate boot tasks such as :
  - Installing updates
  - Installing software
  - Downloading common files from the internet
  - Anything you can think of
- The EC2 User Data Script runs with the root user

  - should start command 'sudo'

  ### 인스턴스 실습

  - 인스턴스 중지 후 , 다시 시작하면 public IPv4 주소가 변함
    - private IPv4는 변하지않음
