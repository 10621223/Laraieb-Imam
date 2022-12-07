# Laraieb-Imam
CA1
Enterprise Name: Hubspot

<img src="Images/OIP.jpg" alt=logo/>

<h1>Background</h1>

HubSpot is an American developer and marketer of software products for inbound marketing, sales, and customer service, was founded in 2006. It is is a CRM platform that offers softwares to manage different kinds of businesses - Marketing Automation Software, Sales CRM Softwares, CMS (Content Management Software), Operations Software, Customer Service Software. Its products and services aim to provide tools for customer relationship management, social media marketing, content management, lead generation, web analytics, search engine optimization, live chat, and customer support. It was founded on "inbound", the notion that people don't want to be interrupted by marketers or harassed by salespeople — they want to be helped.(www.hubspot.com). More than 150,000 companies using HubSpot to scale, it's time to celebrate those that inspire us to innovate, to imagine, and to grow better. (www.hubspot.com). Current workforce of Hubspot is 5,895. Hubspot's 2021 Revenue was $1.3 Billion.(www.hubspot.com).


<h1>Current IT Setup</h1>

HubSpot supports regional data hosting. Prior to July 2021, HubSpot's AWS (Amazon web services) environment was solely located in the United States. As of July 2021, HubSpot has a new AWS environment in the European Union. HubSpot accounts are hosted in one of these data hosting locations, and customer data is processed and stored in that location. (www.hubspot.com)


<h1>Cloud Recommendations</h1>

Amazon EC2 provide wide section of use cases, since Hubspot is medium entreprise I would suggest m4.large as it is suitable for such scaleable enterprise. Hupspot's seems to fit perfectly in this category. EC2 provides a balance of compute, memory and networking resources, and can be used for a variety of diverse workloads. Under <b>m4.large</b> they will get <b>2 vCPU's (Virtual Centralized Processing Unit)</b> which will provide <b>EBS Strorage</b> type with <b>450mbps</b> of dedicated EBS bandwidth.

It will also include <b>8 Gibibytes (GIB) Microsoft Endpoint Manager (MEM)</b>, which is a cloud-based solution built to solve challenges associated with deploying, managing and securing devices in the enterprise, which includes devices servers, PCs and mobile.

CRM company Hubspot is data driven company and will required Large storage hence, FSx cluster file storage system will suit the needs of the company. Additionally, <b>Cloud Watch</b> will be an useful tool to include in the package. Cloud watch is a monitoring tool which helps to track the usage of cloud. 

In Summary, recommendation for HubSpot is Quantity of instances (900), Pricing strategy (On-Demand Instances) On Demand since it can be made active whenever needed which will save time and cost usually load balancer handles the traffic and actives EC2 as needed, Storage amount (16 TB), Instance type (m4.large).

<h3>Features of EC2 m4</h3>

- Custom built Amazon Graviton2 Processor with 64-bit Arm Neoverse cores

- Support for Enhanced Networking with Up to 25 Gbps of Network bandwidth

- EBS-optimized by default

- Powered by the Amazon Nitro System, a combination of dedicated hardware and lightweight hypervisor

- Instance storage offered via EBS or NVMe SSDs that are physically attached to the host server (www.aws.amazon.com)

<h3>EC2 m4.large</h3>

EC2 is  Elastic Compute Cloud. It allows users to rent virtual computers on which they run their own computer applications. A user can create, launch, and terminate server-instances as neededand pay by the second for active servers. EC2 provides users with control over the geographical location of instances that allows for latency optimization and high levels of redundancy. 

900 instances will be enough assuming the 30% of the workforce (5,895) will be using the instances . It's a CRM company expected Utilisation rate is assumed to be 80% that will account to 584hours in a month. Hourly rate by AWS is 0.111 USD.

- <b>Price Calculation excluding taxes</b>: 900 instances x 0.111 USD x 584 hours in a month = <b>58,341.60 USD (monthly onDemand cost)</b>

<h3>Amazon Elastic Block Storage (EBS)</h3>
<p>EBS is a block level stroage which is used with EC2 cloud to store data. With EBS data can be stored even after EC2 is shutdown. Hubspot requires a lot of data storage as any CRM company does. 16 TB is recommendated, that is 16384 GB. Price is 0.11 USD per month offered by AWS.</p>

<ul>
  <li><b>Unit conversions</b>: Storage amount: 16 TB x 1024 GB in a TB = 16384 GB</li>
  <li><b>Price Calculation excluding taxes</b>: 16,384 GB x 0.11 USD x 900 instances = <b>1,622,016.00 USD (EBS Storage Monthly Cost)</b> </li>
</ul>

<h3>Cloud Watch</h3>
<p>Cloud watch is a monitoring tool which helps to track the usage of cloud. The application automatically collects and provides metrics for CPU utilization, latency and request counts. Users can also get additional metrics to be monitored, such as memory usage, transaction volumes or error rates.</p>

<p>The CloudWatch interface provides current statistics that users can view in graph format. Users can set notification alarms to be sent when something being monitored surpasses a specified threshold. The app can also detect and shut down unused or underused EC2 instances. It is offered free of cost by AWS and will work as an important tool for HubSpot.</p>

<img src="Images/CloudWatch.png" alt=Functions/>


<h3>Virtual Private Cloud (VPC)</h3>
<p>VPC is virtual network dedicated to user, an isolated section of Amazon Web Services (AWS) Cloud. EC2 can be accessed here with other services. Under VPC few things will be needed by Hubspot like VPN, Data Transfer, Traffic Monitoring, Gateway Load Balancer.</p>

<u>
</ul>

<p><b>1. VPN -</b> Virtual Private Network enables users to send and receive data across public networks seemlessly as one would do over private network. It also provides access to resources that cannot be accessed on the public network and typically used for remote workers. Virtual Private Network will be a requirement since the client might use it outside Ireland then he will need VPN to access the services.</p>

<ul>
  <li><b>Unit conversions:</b></li>
  
  Average duration for each connection: 24 hours per day * (730 hours in a month / 24 hours in a day) = 730 hours per month
  
  <li><b>Pricing calculations:</b> 900 connnections x 0.05 USD x 730 hours per month = <b>32,850.00 USD (Site to Site VPN usage monthly cost)</b></li>
 
</ul>

<b>2. Data Transfer -</b> Data transfer is required because CRM tool has big data size due to customer information and purchase information and other factors so Hubspot needs data transfer option for analysis and projection.

<ul>
  <p><li><b>Unit conversions:</b></li>
  
<b>Inbound Internet:</b> 16 TB per month x 1024 GB in a TB = 16384 GB per month

<b>Inbound & Outbound Intra region:</b> 16 TB per month x 1024 GB in a TB = 16384 GB per month</p>

  <li><b>Pricing calculations:</b></li>
  
<b>Inbound:</b>

  <b>Internet:</b> 16384 GB x 0 USD per GB = <b>0.00 USD</b>

  <b>Intra region:</b> (16384 GB x 0.01 USD per GB outbound) + (16384 GB x 0.01 USD per GB inbound) = <b>327.68 USD</b>
</ul>

<ul>
<b>Outbound:</b>

  <b>Internet:</b> Tiered pricing for 16384 GB: 10240 GB x 0.09 USD per GB = <b>921.60 USD</b>

  <b>Intra region:</b> 6144 GB x 0.085 USD per GB = <b>522.24 USD</b>
</ul>
<p><b>Data Transfer cost (monthly): 1,771.52 USD</b></p>


<p><b>3. Traffic Monitoring -</b> Traffic monitoring is required because if the account user usage crosses the load the network can handle it will crash so it's required to keep that in check. </b>

900 sessions x 730 hours in a month x 0.018 USD per session-hr = <b>11,826.00 USD</b>

<b>Total Traffic Mirroring charge (monthly): 11,826.00 USD</b>

<b>4. Gateway Load Balancer -</b> Load balancer is required so if the usage increases load balancer will create another instance to handle the traffic.

100 availability zones x 0.014 USD x 730 hours in a month = 1,022.00 USD

<b>Total hourly charges for all Gateway Load Balancers (monthly): 1,022.00 USD</b>  
  
<h1>Non-cloud Recommadation</h1>
Outsource customer grievance centre - As a CRM company they can have a huge customer call loads and seprating <b>Grievance Department</b> and outsourcing it can shed off work burden on the Hubspot employees so they can focus on new businesses and minor grievances can be resolved by outsourced customer centre.

<h1>References</h1>
www.hubspot.com. <i>HubSpot | Software, Tools, and Resources to Help Your Business Grow Better</i> [Online] Available at: https.www.hubspot.com [Accessed 1 Dec 2022].

www.hubspot.com. <i>Our Story | HubSpot - Internet Marketing Company</i> [Online]. Available at: https://www.hubspot.com/our-story [Accessed 29 Nov 2022].

www.hubspot.com. <i>158,000 HubSpot Customers and Growing</i> [Online]. Available at: https://www.hubspot.com/customer-spotlight [Accessed 30 Nov 2022]

www.hubspot.com. <i>HubSpot Reports Q4 and Full Year 2021 Results</i> [Online]. Available at: https://ir.hubspot.com/news/hubspot-reports-q4-and-full-year-2021-results [Accessed 01 Dec 2022]

www.aws.amazon.com <i>Secure and resizable cloud compute - Amazon EC2 - Amazon Web Services</i> [Online]. Available at: https://aws.amazon.com/ec2/?nc2=h_ql_prod_fs_ec2 [Accessed 01 Dec 2022]
                      
www.techtarget.com <i>What is Amazon <B>CloudWatch</b></i> [Online]. Available at: https://www.techtarget.com/searchaws/definition/CloudWatch [Accessed 04 Dec 2022]

                
