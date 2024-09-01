## Amazon EFS - Elastic File System

- Managed NFS (network file system) that can be mounted on many EC2
- EFS works with EC2 instances in multi-AZ
- Highly available . scalable , expensive (3x gp2), pay per use
- Use cases : content management, web serving, data sharing, Wordpress
- Uses NFSv4.1 protocol
- Uses security group to control access to EFS
- Compatible with Linux based AMI(not windows)
- Encryption at rest using KMS (at rest : 저장된 상태)
- POSIX file system (~Linux) that has a standard file API
- File system scales automatically, pay-per-use, no capacity planning !
