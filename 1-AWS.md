# AWS

![image](https://user-images.githubusercontent.com/73632896/224480042-5ac3e488-4210-4210-b4a3-fcad428b4b60.png)


## What's AWS?

- AWS (Amazon Web Services) is a cloud provider.
- Provides servers and services that can used on-demand and scale them easily.

## AWS Cloud History

![image](https://user-images.githubusercontent.com/73632896/223426431-de5bc3e6-4fd6-405a-9860-96c2b2bf8fb2.png)

## AWS Cloud Use Cases

- AWS enables you to build sophisticated, scalable applications
- Applicable to a diverse set of industries
- Use cases include
    1. Enterprise IT, Backup & Storage, Big Data analytics
    2. Website hosting, Mobile & Social Apps
    3. Gaming

## AWS Global Infrastructure

- AWS Regions
- AWS Availability Zones 
- AWS Data Centers
- AWS Edge Locations / Points of Presence
- https://infrastructure.aws/

    ### AWS Regions

    - AWS has Regions all around the world
    - Names can be ap-south-1 (Mumbai), eu-west-3…
    - A region is a cluster of data centers
    - Most AWS services are region-scoped
    - https://aws.amazon.com/about-aws/global-infrastructure/

        ####  How to choose an AWS Region?
        If you need to launch a new application where should you do it?

        - **Compliance with data governance and legal requirements:** data never leaves a region without your explicit permission
        - **Proximity to customers:** reduced latency
        - **Available services within a Region:** new services and new features aren’t available in every Region
        - **Pricing:** pricing varies region to region and is transparent in the service pricing page

    ### AWS Availability Zones

    - Each region has many availability zones (usually 3, min is 3, max is 6). Example:
        - ap-southeast-2a
        - ap-southeast-2b
        - ap-southeast-2c
    - Each availability zone (AZ) is one or more discrete data centers with redundant power, networking, and connectivity
    - They’re separate from each other, so that they’re isolated from disasters
    - They’re connected with high bandwidth, ultra-low latency networking

        ![image](https://user-images.githubusercontent.com/73632896/223431631-96cd47bc-73fa-44d9-b1e0-8f396f7a905f.png)

    ### AWS Points of Presence (Edge Locations)

    - Amazon has 216 Points of Presence (205 Edge Locations & 11 Regional Caches) in 84 cities across 42 countries (May change over time)
    - Content is delivered to end users with lower latency


## Tour of the AWS Console

### AWS has Global Services

- Identity and Access Management (IAM)
- Route 53 (DNS service)
- CloudFront (Content Delivery Network)
- WAF (Web Application Firewall)

###  Most AWS services are Region-scoped:

- Amazon EC2 (Infrastructure as a Service)
- Elastic Beanstalk (Platform as a Service)
- Lambda (Function as a Service)
- Rekognition (Software as a Service)
- https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/

**Note - This content is from the [Ultimate AWS Certified Solutions Architect Associate SAA-C03](https://www.udemy.com/course/aws-certified-solutions-architect-associate-saa-c03/) Udemy Course by Stephane Maarek**

