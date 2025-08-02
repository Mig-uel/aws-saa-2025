# AWS Cloud Overview (Regions & Availability Zones)

## AWS Cloud History

- 2002
  - AWS (Amazon Web Services) was launched internally
- 2003
  - Amazon infrastructure is one of their core strength idea to market. "Maybe we can do IT as a service?"
- 2004
  - Amazon publicly launched with SQS (Simple Queue Service)
- 2006
  - Amazon expanded their offerings and re-launched publicly with SQS (Simple Queue Service), S3 (Simple Storage Service), and EC2 (Elastic Compute Cloud)
- 2007
  - AWS expands to Europe with the launch of the EU (Ireland) region

Fast-forward to today, so many applications run on AWS, and it is the largest cloud provider in the world (Dropbox, Netflix, Airbnb, etc.).

## AWS Cloud Facts

- In 2023, AWS had $90 billion in annual revenue
- AWS accounts for 31% of the global cloud market share in Q1 2024 (Microsoft Azure is second with 25%)
- Pioneer and leader of the AWS Cloud Market for the 13th consecutive year
- AWS has over 1M active customers

## AWS Cloud Use Cases

- AWS enables you to build sophisticated and scalable applications
- Applicable to a diverse set of industries and use cases
- Companies like McDonald's, 21st Century Fox, Activision, Netflix and more all use the AWS Cloud
- Use cases include:
  - Enterprise IT
  - Backup and storage
  - Big data analytics
  - Website hosting
  - Mobile and web applications
  - Gaming

## AWS Global Infrastructure

We have a global infrastructure that is designed to be secure, reliable, and scalable. The AWS Cloud is built around the following key components:

- **AWS Regions**: Geographical areas that contain multiple Availability Zones. Each region is isolated from others to provide fault tolerance and stability.
- **Availability Zones (AZs)**: Physically separate data centers within a region. Each AZ is designed to be independent and isolated from failures in other AZs, providing high availability and redundancy
- **Edge Locations/Points of Presence (PoPs)**: Locations that deliver content to end users with low latency. They are used for services like Amazon CloudFront, AWS Global Accelerator, and AWS Lambda@Edge

## AWS Regions

The first important concept to understand are AWS Regions. An AWS Region is a geographical area that contains multiple Availability Zones (AZs). Each region is isolated from others to provide fault tolerance and stability. AWS currently has 32 regions globally, with more on the way

- AWS has Regions all around the world, including North America, South America, Europe, Asia Pacific, and the Middle East
- Names can be `us-east-1` (N. Virginia), `eu-west-1` (Ireland), `ap-southeast-2` (Sydney), etc
- A region is a **cluster of data centers** in a specific geographic area
- Most AWS services are region-scoped, meaning they are available in specific regions

## How to Choose an AWS Region

If you need to launch a new application, where should you do it? It depends on several factors:

- **Compliance**: Some regions have specific compliance requirements (e.g., GDPR in Europe)

  - Compliance with data governance and legal requirements is crucial
  - Data never leaves a region without your explicit permission

- **Latency**: Choose a region that is geographically close to your users to minimize latency
  - The closer the region is to your users, the lower the latency will be
  - This is especially important for applications that require real-time interactions

**Availability**: Ensure the region you choose has the AWS services you need

- Not all AWS services are available in every region
- Check the [AWS Regional Services List](https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/) to see which services are available in each region

- **Cost**: AWS pricing can vary by region, so consider the cost implications of your choice
  - Some regions may have lower costs for certain services
  - Compare pricing across regions to find the most cost-effective option

## AWS Availability Zones (AZs)

AWS Availability Zones (AZs) are actually what make up an AWS Region. An AZ is a physically separate data center within a region. Each AZ is designed to be independent and isolated from failures in other AZs, providing high availability and redundancy.

- Each region has multiple AZs (usually 3, min is 3, max is 6)

  - Example: The Sydney region has 3 AZs, `ap-southeast-2a`, `ap-southeast-2b`, and `ap-southeast-2c`

- Each availability zone is one or more discrete data centers with redundant power, networking, and connectivity

  - Each AZ is designed to be independent and isolated from failures in other AZs
  - This means that if one AZ goes down, the others will still be operational

- They are separate from each other to ensure high availability and fault tolerance

- Availability Zones are connected to each other with high bandwidth, ultra-low latency networking

  - This allows you to build applications that are highly available and fault-tolerant
  - You can run your application across multiple AZs to ensure that it remains operational even if one AZ goes down
  - All linked together they form a single region

## AWS Edge Locations/Points of Presence (PoPs)

Edge Locations, also known as Points of Presence (PoPs), are locations that deliver content to end users with low latency. They are used for services like Amazon CloudFront, AWS Global Accelerator, and AWS Lambda@Edge.

- Amazon has 400+ Points of Presence (PoPs) (400+ Edge Locations & 10+ Regional Caches) in 90+ cities across 40+ countries
- Content is delivered to end users with lower latency by caching content at these locations
- Edge Locations are used for services like:
  - Amazon CloudFront (Content Delivery Network)
  - AWS Global Accelerator (Improves availability and performance of applications)
  - AWS Lambda@Edge (Run code closer to users for lower latency)

## Quick Tour of the AWS Console

- AWS has Global Services that are not region-scoped, such as:

  - IAM (Identity and Access Management)
  - Route 53 (DNS Service)
  - CloudFront (Content Delivery Network)
  - WAF (Web Application Firewall)

- Most AWS services are region-scoped, meaning they are available in specific regions. Some examples include:

  - EC2 (Elastic Compute Cloud) (Infrastructure as a Service)
  - Elastic Beanstalk (Platform as a Service)
  - Lambda (Function as a Service)
  - Rekognition (Software as a Service)

- Region table can be found at [AWS Global Infrastructure](https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/)
