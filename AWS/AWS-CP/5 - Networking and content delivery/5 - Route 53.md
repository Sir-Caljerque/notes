# Route 53

- Is a highly available and scalable Domain Name System (DNS) web service
- Is used to route end users to internet applications by translating names (like www.example.com) into numeric IP addresses (like 192.0.2.1) that computers use to connect to each other
- Is fully compliant with IPv4 and IPv6
- Connects user requests to infrastructure running in AWS and also outside of AWS
- Is used to check the health of your resources
- Features traffic flow
- Enables you to register domain names

Amazon Route 53 is a highly available and scalable cloud Domain Name System (DNS) web service. It is designed to give developers and businesses areliable and cost-effective way to route users to internet applications by translating names (like *www.example.com*) into the numeric IP addresses (like *192.0.2.1*) that computers use to connect to each other. In addition, Amazon Route 53 is fully compliant with IPv6. See more on Domain Name Systems at https://aws.amazon.com/route53/what-is-dns/.

Amazon Route 53 effectively connects user requests to infrastructure running in AWS—such as Amazon EC2 instances, Elastic Load Balancing load balancers, or Amazon S3 buckets—and can also be used to route users to infrastructure that is outside of AWS. 
You can use Amazon Route 53 to configure DNS health checks so you that can route traffic to healthy endpoints or independently monitor the health of your application and its endpoints. 

Amazon Route 53 traffic flow helps you manage traffic globally through several routing types, which can be combined with DNS failover to enable various low-latency, fault-tolerant architectures. You can use Amazon Route 53 traffic flow’s simple visual editor to manage how your users are routed to your application’s endpoints—whether in a single AWS Region or distributed around the globe.

Amazon Route 53 also offers Domain Name Registration—you can purchase and manage domain names (like example.com), and Amazon Route 53 will automatically configure DNS settings for your domains.

## Amazon Route 53 DNS resolution
![[Pasted image 20240813135506.png]]

## Route 53 supported routing

Amazon Route 53 supports several types of routing policies, which determine how Amazon Route 53 responds to queries:
- *Simple routing (round robin)*–Use for a single resource that performs a given function for your domain (such as a web server that serves content for the example.com website).
- *Weighted round robin routing* –Use to route traffic to multiple resources in proportions that you specify. Enables you to assign weights to resource record sets to specify the frequency with which different responses are served. You might want to use this capability to do A/B testing, which is when you send a small portion of traffic to a server where you made a software change. For instance, suppose you have two record sets that are associated with one DNS name: one with weight 3 and one with weight 1. In this case, 75 percent of the time, Amazon Route 53 will return the record set with weight 3, and 25 percent of the time, Amazon Route 53 will return the record set with weight 1. Weights can be any number between 0 and 255.
- *Latency routing (LBR)* –Use when you have resources in multiple AWS Regions and you want to route traffic to the Region that provides the best latency. Latency routing works by routing your customers to the AWS endpoint (for example, Amazon EC2 instances, Elastic IP addresses, or load balancers) that provides the fastest experience based on actual performance measurements of the different AWS Regions where your application runs. 
- *Geolocation routing* –Use when you want to route traffic based on the location of your users. When you use geolocation routing, you can localize your content and present some or all of your website in the language of your users. You can also use geolocation routing to restrict the distribution of content to only the locations where you have distribution rights. Another possible use is for balancing the load across endpoints in a predictable, easy-to-manage way, so that each user location is consistently routed to the same endpoint. 
- *Geoproximity routing*–Use when you want to route traffic based on the location of your resources and, optionally, shift traffic from resources in one location to resources in another. 
- *Failover routing (DNS failover)*–Use when you want to configure active-passive failover. Amazon Route 53 can help detect an outage of your website and redirect your users to alternate locations where your application is operating properly. When you enable this feature, Amazon Route 53 health-checking agents will monitor each locationor endpoint of your application to determine its availability. You can take advantage of this feature to increase the availability of your customer-facing application. 
- *Multivalue answer routing*–Use when you want Route53 to respond to DNS queries with up to eight healthy records that are selected at random. You can configure Amazon Route53 to return multiple values—such as IP addresses for your web servers—in response to DNS queries. You can specify multiple values for almost any record, but multivalueanswer routing also enables you to check the health of each resource so that Route53 returns only values for healthy resources. It's not a substitute for a load balancer, but the ability to return multiple health-checkable IP addresses is a way to use DNS to improve availability and load balancing.

# Multi-region deployment (use case)

![[Pasted image 20240813140111.png]]

Multi-Region deployment is an example use case for Amazon Route 53. With Amazon Route 53, the user is automatically directed to the Elastic Load Balancing load balancer that’s closest to the user.

The benefits of multi-region deployment of Route 53 include:
- Latency-based routing to the Region
- Load balancing routing to the Availability Zone

# DNS failover

Improve the availability of your applications that run on AWS by:
- Configuring backup and failover scenarios for your own applications
- Enabling highly available multi-region architectures on AWS
- Creating health checks to monitor the health and performance of your web applications, web servers, and other resources. Each health check that you create can monitor one of the following—the health of a specified resource, such as a web server;the status of other health checks; and the status of an Amazon CloudWatch alarm.
![[Pasted image 20240813140308.png]]

# DNS failover for a multi-tiered web app

This diagram indicates how DNS failover works in a typical architecture for a multi-tiered web application. Route 53 passes traffic to a load balancer, which then distributes traffic to a fleet of EC2 instances.

You can dothe following tasks with Route 53 to ensure high availability:
1. Create two DNS records for the Canonical Name Record (CNAME) www with a routing policy of Failover Routing. The first record is the primary route policy, which points to the load balancer for your web application. The second record is the secondary route policy, which points to your static Amazon S3 website.
2. Use Route 53 health checks to make sure that the primary is running. If it is, all traffic defaults to your web application stack. Failover to the static backup site would be triggered if either the web server goes down (or stops responding),or the database instance goes down.

# 2 - Key takeaways

Some keytakeaways from this section of the module include:
- Amazon Route 53 is a highly available and scalable cloud DNS web service that translates domain names into numeric IP addresses.
- Amazon Route 53 supports several types of routing policies.
- Multi-Region deployment improves your application’s performance for a global audience.
- You can use Amazon Route 53 failover to improve the availability of your applications.

