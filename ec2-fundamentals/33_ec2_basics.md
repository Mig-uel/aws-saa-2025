# EC2 Fundamentals

## Amazon EC2 (Elastic Compute Cloud)

Amazon EC2 is a web service that provides resizable compute capacity in the cloud. It allows users to run virtual servers, known as instances, on-demand. EC2 is designed to make web-scale cloud computing easier for developers.

- EC2 is one of the most popular services in the AWS ecosystem.
- EC2 stands for Elastic Compute Cloud and is Infrastructure as a Service (IaaS).

EC2 consists of several components:

- Renting virtual servers (instances) in the cloud (EC2)
- Storing data on virtual drives (EBS)
- Distributing load across machines (ELB)
- Scaling the services using an auto-scaling group (ASG)

Knowing how to use EC2 is fundamental to understand how the cloud works. It is the first service that most people use when they start with AWS.

## EC2 Sizing & Configuration

When launching an EC2 instance, you need to choose the right size and configuration based on your workload requirements.

## Configuration options include:

- Operating System (OS)
  - Choose from various OS options like Linux, Windows, etc.
- How much compute power and cores are needed (CPU)
  - Select instance types based on CPU requirements (e.g., t2.micro, m5.large)
- How much memory is needed (RAM)
  - Choose instance types with appropriate RAM (e.g., t2.micro has 1GB, m5.large has 8GB)
- How much storage is needed (EBS & EFS)
  - Network-attached storage options like EBS (Elastic Block Store) and EFS (Elastic File System)
  - Hardware attached storage options like instance store volumes
- How much network bandwidth is needed (Network)
  - Consider instance types with different network performance levels (e.g., low, moderate, high)
- Firewall rules (Security Groups)
  - Configure security groups to control inbound and outbound traffic
- Bootstrapping scripts (User Data)
  - Use user data to run scripts at instance launch for initial setup

## EC2 User Data

User data is a feature that allows you to pass scripts or commands to an EC2 instance at launch time. This can be used for bootstrapping, such as installing software or configuring the instance.

User data can be provided in the form of a shell script or cloud-init directives.

- It is possible to bootstrap our instances using an EC2 User Data script.
- In general, bootstrapping is the process of preparing an instance for use by installing software, configuring settings, etc.
- The script is executed only once when the instance is launched.

EC2 User Data can be used to automate boot tasks such as:

- Installing updates
- Installing software packages
- Downloading common files from the internet
- Configuring the instance (e.g., setting up a web server)

The EC2 User Data script is executed as the **root** user, so it has full permissions to perform any necessary tasks during the instance initialization.

## EC2 Instance Types

EC2 instances come in various types, each optimized for different use cases. The instance types are categorized based on their CPU, memory, storage, and networking capabilities.

Here are 5 common EC2 instance families:

| Instance    | vCPU | Memory (GiB) | Storage Type     | Use Case          | Network Performance | EBS Bandwidth  |
| ----------- | ---- | ------------ | ---------------- | ----------------- | ------------------- | -------------- |
| t2.micro    | 1    | 1            | EBS              | General Purpose   | Low to Moderate     | Up to 100 Mbps |
| t2.xlarge   | 4    | 16           | EBS              | General Purpose   | Moderate            | Up to 300 Mbps |
| c5d.4xlarge | 16   | 32           | 1 x 400 NVMe SSD | Compute Optimized | Up to 10 Gigabit    | 4,750 Mbps     |
| r5.16xlarge | 64   | 512          | EBS              | Memory Optimized  | 20 Gbps             | 13,600 Mbps    |
| m5.8xlarge  | 32   | 128          | EBS              | General Purpose   | 10 Gbps             | 6,800 Mbps     |
