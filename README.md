# Laraieb-Imam
CA1
Enterprise Name: Hubspot

<img src="Images/screenshot.png" alt="test"/>

<h1>Background</h1>

HubSpot is an American developer and marketer of software products for inbound marketing, sales, and customer service. HubSpot was founded in 2006. It is is a CRM platform that offers softwares to manage different kinds of businesses - Marketing Automation Software, Sales CRM Softwares, CMS (Content Management Software), Operations Software, Customer Service Software. Its products and services aim to provide tools for customer relationship management, social media marketing, content management, lead generation, web analytics, search engine optimization, live chat, and customer support. It was founded on "inbound", the notion that people don't want to be interrupted by marketers or harassed by salespeople — they want to be helped.
More than 150,000 companies using HubSpot to scale, it's time to celebrate those that inspire us to innovate, to imagine, and to grow better. (find reference if it's true)..
Last year Revenue was $1.3 Billion



<h1>Current IT Setup</h1>

HubSpot supports regional data hosting. Prior to July 2021, HubSpot's AWS (Amazon web services) environment was solely located in the United States. As of July 2021, HubSpot has a new AWS environment in the European Union. HubSpot accounts are hosted in one of these data hosting locations, and customer data is processed and stored in that location.


<h1>Cloud Recommendations</h1>

Amazon EC2 provide wide section of use cases, since Hubspot is medium entreprise I would suggest M4 as it is suitable for such scaleable enterprise. Hupspot's seems to fit perfectly in this category. EC2 provides a balance of compute, memory and networking resources, and can be used for a variety of diverse workloads. Under M4 they will get 2 vCPU's which will provide EBS Strorage type with 1000mbps of dedicated EBS bandwidth.
CRM company Hubspot is data driven company and will required Large storage hence, FSX cluster file storage system will suit the needs of the company.
Hubspot needs small instance to host CRM applications. Along with M4 and storage system, Cloud Watch will be an useful tool to include in the package. Cloud watch is a monitoring tool which helps to track the usage of cloud. 
Summary: Operating system (Linux), Quantity (900), Pricing strategy (On-Demand Instances), Storage amount (16 TB), Instance type (m4.large)

EC2 is  Elastic Compute Cloud. It allows users to rent virtual computers on which they run their own computer applications. 
EC2 encourages scalable deployment of applications by providing a web service with which a user can boot an Amazon Machine Image (AMI) to configure a virtual machine, an "instance" is what Amazon calls it. A user can create, launch, and terminate server-instances as needed, paying by the second for active servers – hence the term "elastic". EC2 provides users with control over the geographical location of instances that allows for latency optimization and high levels of redundancy.In November 2010, Amazon switched its own retail website platform to EC2 and AWS.

<h3>Features of EC2 M4</h3>

Custom built Amazon Graviton2 Processor with 64-bit Arm Neoverse cores

Support for Enhanced Networking with Up to 25 Gbps of Network bandwidth

EBS-optimized by default

Powered by the Amazon Nitro System, a combination of dedicated hardware and lightweight hypervisor

Instance storage offered via EBS or NVMe SSDs that are physically attached to the host server

<h3>EC2 M4 Requirement</h3>
900 instances will be enough considering the size of the business. It's a CRM company expected Utilisation rate is assumed to be 80% that will account to 584hours in a month. Hourly rate is 0.111 USD (given).

<b>Price Calculation excluding taxes</b>: 900 instances x 0.111 USD x 584 hours in a month = 58,341.60 USD (monthly onDemand cost)
Amazon EC2 On-Demand instances (monthly): 58,341.60 USD

<h3>Amazon Elastic Block Storage (EBS)</h3>
EBS is a block level stroage which is used with EC2 cloud to store data. With EBS data can be stored even after EC2 is shutdown. Hubspot requires a lot of data storage as any CRM company does. 16 TB will be recommendated, that is 16384 GB. Price is 0.11 USD per month.

<b>Unit conversions</b>: Storage amount: 16 TB x 1024 GB in a TB = 16384 GB
<b>Price Calculation excluding taxes</b>: 16,384 GB x 0.11 USD x 900 instances = 1,622,016.00 USD (EBS Storage Cost)
EBS Storage Cost: 1,622,016.00 USD
Amazon Elastic Block Storage (EBS) pricing (monthly): 1,622,016.00 USD

<h3>Cloud Watch Requirement</h3>

Cloud watch is a monitoring tool which helps to track the usage of cloud. It is offered free of cost by AWS. 

<h3>Amazon Elastic Block Storage (EBS)</h3>

<h1>Virtual Private Cloud (VPC)</h1>
1. VPN - As the client might use it outside Ireland then he will need VPN

2. Data Transfer - Data transfer because CRM tool has big data size due to customer information or purchase and other factors so u need data transfer option for analysis and projection

3. Traffic Monitoring - Traffic monitoring because if the account user usage crosses the load the network can handle it will crash so it's required to keep that in check

4. Gateway Load Balancer - Load balancer so that if the usage increases load balancer will create another instance to handle the traffic
  
Non-cloud Recommadations  
1. Outsource customer grevience centres
2. 
Small instance to host crm app.
Cost of AWS nad hubspot combined together -and offered to client . this highly benefits the cliet.
VPC need
Large Storage FSx cluster file system storage system.



