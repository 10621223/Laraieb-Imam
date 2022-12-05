# Laraieb-Imam
CA1
Enterprise Name: Hubspot

<img src="Images/OIP.jpg" alt=logo/>

<h1>Background</h1>

HubSpot is an American developer and marketer of software products for inbound marketing, sales, and customer service, was founded in 2006. It is is a CRM platform that offers softwares to manage different kinds of businesses - Marketing Automation Software, Sales CRM Softwares, CMS (Content Management Software), Operations Software, Customer Service Software. Its products and services aim to provide tools for customer relationship management, social media marketing, content management, lead generation, web analytics, search engine optimization, live chat, and customer support. It was founded on "inbound", the notion that people don't want to be interrupted by marketers or harassed by salespeople — they want to be helped.(www.hubspot.com). More than 150,000 companies using HubSpot to scale, it's time to celebrate those that inspire us to innovate, to imagine, and to grow better. (www.hubspot.com). Hubspot's 2021 Revenue was $1.3 Billion.(www.hubspot.com).


<h1>Current IT Setup</h1>

HubSpot supports regional data hosting. Prior to July 2021, HubSpot's AWS (Amazon web services) environment was solely located in the United States. As of July 2021, HubSpot has a new AWS environment in the European Union. HubSpot accounts are hosted in one of these data hosting locations, and customer data is processed and stored in that location. (www.hubspot.com)


<h1>Cloud Recommendations</h1>

Amazon EC2 provide wide section of use cases, since Hubspot is medium entreprise I would suggest m4.large as it is suitable for such scaleable enterprise. Hupspot's seems to fit perfectly in this category. EC2 provides a balance of compute, memory and networking resources, and can be used for a variety of diverse workloads. Under <b>m4</b> they will get 2 vCPU's which will provide EBS Strorage type with 1000mbps of dedicated EBS bandwidth.

CRM company Hubspot is data driven company and will required Large storage hence, FSx cluster file storage system will suit the needs of the company.
Hubspot will need small instance to host CRM applications. Along with <b>m4.large</b> and storage system, <b>Cloud</b> Watch will be an useful tool to include in the package. Cloud watch is a monitoring tool which helps to track the usage of cloud. 
In Summary, recommendation for HubSpot is Operating system (Linux), Quantity (900), Pricing strategy (On-Demand Instances), Storage amount (16 TB), Instance type (m4.large).

<h3>Features of EC2 m4</h3>

- Custom built Amazon Graviton2 Processor with 64-bit Arm Neoverse cores

- Support for Enhanced Networking with Up to 25 Gbps of Network bandwidth

- EBS-optimized by default

- Powered by the Amazon Nitro System, a combination of dedicated hardware and lightweight hypervisor

- Instance storage offered via EBS or NVMe SSDs that are physically attached to the host server (www.aws.amazon.com)

<h3>EC2 m4.large Requirement</h3>

EC2 is  Elastic Compute Cloud. It allows users to rent virtual computers on which they run their own computer applications. A user can create, launch, and terminate server-instances as neededand pay by the second for active servers. EC2 provides users with control over the geographical location of instances that allows for latency optimization and high levels of redundancy. 900 instances will be enough considering the size of the business. It's a CRM company expected Utilisation rate is assumed to be 80% that will account to 584hours in a month. Hourly rate by AWS is 0.111 USD.

<b>Price Calculation excluding taxes</b>: 900 instances x 0.111 USD x 584 hours in a month = <b>58,341.60 USD (monthly onDemand cost)</b>

<h3>Amazon Elastic Block Storage (EBS)</h3>
EBS is a block level stroage which is used with EC2 cloud to store data. With EBS data can be stored even after EC2 is shutdown. Hubspot requires a lot of data storage as any CRM company does. 16 TB is recommendated, that is 16384 GB. Price is 0.11 USD per month offered by AWS.


<ul>
  <li><b>Unit conversions</b>: Storage amount: 16 TB x 1024 GB in a TB = 16384 GB</li>
  <li><p><b>Price Calculation excluding taxes</b>: 16,384 GB x 0.11 USD x 900 instances = <b>1,622,016.00 USD (EBS Storage Monthly Cost)</b> </li>
</ul>


<h3>Cloud Watch Requirement</h3>
Cloud watch is a monitoring tool which helps to track the usage of cloud. It is offered free of cost by AWS. It is offered free of cost by AWS.

<h3>Virtual Private Cloud (VPC)</h3>
Virtual private cloud (VPC) is virtual network dedicated to user, an isolated section of Amazon Web Services (AWS) Cloud. EC2 can be accessed here with other services. Under VPC few things will be needed by Hubspot like VPN, Data Transfer, Traffic Monitoring, Gateway Load Balancer.

1. VPN - Virtual Private Network will be required since the client might use it outside Ireland then he will need VPN to access the services.

<b>Unit conversions:</b>
Average duration for each connection: 24 hours per day * (730 hours in a month / 24 hours in a day) = 730 hours per month
<b>Pricing calculations:</b> 900 connnections x 0.05 USD x 730 hours per month = <b>32,850.00 USD (Site to Site VPN usage monthly cost)</b>

2. Data Transfer - Data transfer because CRM tool has big data size due to customer information or purchase and other factors so Hubspot needs data transfer option for analysis and projection

<b>Calculations</b>: 
Unit conversions (Inbound)

<b>Internet:</b> 16 TB per month x 1024 GB in a TB = 16384 GB per month
<b>Intra region:</b> 16 TB per month x 1024 GB in a TB = 16384 GB per month

Outbound:
Internet: 16 TB per month x 1024 GB in a TB = 16384 GB per month

<b>Pricing calculations</b>

<b>Inbound:</b>

Internet: 16384 GB x 0 USD per GB = 0.00 USD
Intra region: (16384 GB x 0.01 USD per GB outbound) + (16384 GB x 0.01 USD per GB inbound) = 327.68 USD

<b>Outbound:</b>
Internet: Tiered pricing for 16384 GB: 10240 GB x 0.09 USD per GB = 921.60 USD

6144 GB x 0.085 USD per GB = 522.24 USD

Data Transfer cost (monthly): 1,771.52 USD

3. Traffic Monitoring - Traffic monitoring because if the account user usage crosses the load the network can handle it will crash so it's required to keep that in check. 
900 sessions x 730 hours in a month x 0.018 USD per session-hr = 11,826.00 USD

Total Traffic Mirroring charge (monthly): 11,826.00 USD

4. Gateway Load Balancer - Load balancer so that if the usage increases load balancer will create another instance to handle the traffic.

100 availability zones x 0.014 USD x 730 hours in a month = 1,022.00 USD

Total hourly charges for all Gateway Load Balancers (monthly): 1,022.00 USD  
  
Non-cloud Recommadations
1. Outsource customer grevience centres
2. 

<h1>References</h1>
www.hubspot.com. <i>HubSpot | Software, Tools, and Resources to Help Your Business Grow Better</i> [Online] Available at: https.www.hubspot.com [Accessed 1 Dec 2022].

www.hubspot.com. <i>Our Story | HubSpot - Internet Marketing Company</i> [Online]. Available at: https://www.hubspot.com/our-story [29 Nov 2022].

www.hubspot.com. <i>158,000 HubSpot Customers and Growing</i> [Online]. Available at: https://www.hubspot.com/customer-spotlight [30 Nov 2022]

www.hubspot.com. <i>HubSpot Reports Q4 and Full Year 2021 Results</i> [Online]. Available at: https://ir.hubspot.com/news/hubspot-reports-q4-and-full-year-2021-results [01 Dec 2022]

www.aws.amazon.com <i>Secure and resizable cloud compute - Amazon EC2 - Amazon Web Services</i> [Online]. Available at: https://aws.amazon.com/ec2/?nc2=h_ql_prod_fs_ec2 [01 Dec 2022]
                      


                
