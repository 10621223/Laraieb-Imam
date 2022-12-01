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

Amazon EC2 provide wide section of use cases, since Hubspot is medium entreprise I would suggest M4 as it is suitable for such scaleable enterprise. Hupspot's seems to fit perfectly in this category. EC2 provides a balance of compute, memory and networking resources, and can be used for a variety of diverse workloads. Under M4 Hubspot can select m4.2xlarge Instance where they will get 8 vCPU's which will provide EBS Strorage type with 1000mbps of dedicated EBS bandwidth.
CRM company Hubspot is data driven company and will required Large storage hence, FSX cluster file storage system will suit the needs of the company.
Hubspot needs small instance to host CRM applications. Along with M4 and storage system, Cloud Watch will be an useful tool to include in the package. Cloud watch is a monitoring tool which helps to track the usage of cloud. 

Features of EC2 M4

Custom built Amazon Graviton2 Processor with 64-bit Arm Neoverse cores

Support for Enhanced Networking with Up to 25 Gbps of Network bandwidth

EBS-optimized by default

Powered by the Amazon Nitro System, a combination of dedicated hardware and lightweight hypervisor

Instance storage offered via EBS or NVMe SSDs that are physically attached to the host server


Cost Estimate - 1mn and 29mn
12month upfront cost estimate - 0	2473271.417	29679257	USD

No. of EC2 (M4) instance4s required 900
Expected Utilisation rate is 80%
900 instances x 0.111 USD x 584 hours in a month = 58,341.60 USD (monthly onDemand cost)
Amazon EC2 On-Demand instances (monthly): 58,341.60 USD

Amazon Elastic Block Storage (EBS)
30 GB x 0.11 USD x 900 instances = 2,970.00 USD (EBS Storage Cost)
EBS Storage Cost: 2,970.00 USD
Amazon Elastic Block Storage (EBS) pricing (monthly): 2,970.00 USD

My Estimate	Europe (Ireland)		Amazon EC2	0	109666.8	1316001.6	USD	"Operating system (Windows Server)

<h1>Non-cloud Recommendation</h1>

Small instance to host crm app.
Cost of AWS nad hubspot combined together -and offered to client . this highly benefits the cliet.
VPC need
Large Storage FSx cluster file system storage system.



