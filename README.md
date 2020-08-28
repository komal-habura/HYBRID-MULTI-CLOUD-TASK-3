# HYBRID-MULTI-CLOUD-TASK-3

SOMETHING ABOUT VPC (VIRTUAL PRIVATE CLOUD)

What is VPC?

Amazon Virtual Private Cloud (Amazon VPC) enables you to launch AWS resources into a virtual network that you've defined. This virtual network closely resembles a traditional network that you'd operate in your own data center, with the benefits of using the scalable infrastructure AWS.

Amazon VPC concepts

Amazon VPC is the networking layer for Amazon EC2. If you're new to Amazon EC2, see What is Amazon EC2? in the Amazon EC2 User Guide for Linux Instances to get a brief overview.
The following are the key concepts for VPCs:
•	Virtual private cloud (VPC) — A virtual network dedicated to your AWS account.
•	Subnet — A range of IP addresses in your VPC.
•	Route table — A set of rules, called routes, that are used to determine where network traffic is directed.
•	Internet gateway — A gateway that you attach to your VPC to enable communication between resources in your VPC and the internet.
•	VPC endpoint — Enables you to privately connect your VPC to supported AWS services and VPC endpoint services powered by PrivateLink without requiring an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection. Instances in your VPC do not require public IP addresses to communicate with resources in the service. Traffic between your VPC and the other service does not leave the Amazon network.


Accessing Amazon VPC


You can create, access, and manage your VPCs using any of the following interfaces:
•	AWS Management Console — Provides a web interface that you can use to access your VPCs.
•	AWS Command Line Interface (AWS CLI) — Provides commands for a broad set of AWS services, including Amazon VPC, and is supported on Windows, Mac, and Linux. For more information, see AWS Command Line Interface.
•	AWS SDKs — Provides language-specific APIs and takes care of many of the connection details, such as calculating signatures, handling request retries, and error handling. For more information, see AWS SDKs.
•	Query API — Provides low-level API actions that you call using HTTPS requests. Using the Query API is the most direct way to access Amazon VPC, but it requires that your application handle low-level details such as generating the hash to sign the request, and error handling



HYBRID MULTI CLOUD COMPUTING TASK-3


Statement: I  have to create a web portal for our company with all the security as much as possible.
So, we use Wordpress software with dedicated database server.
Database should not be accessible from the outside world for security purposes.
Here only public  the WordPress to clients .
So here are the steps for proper understanding!
Steps:
1) Write a Infrastructure as code using terraform, which automatically create a VPC.
2) In that VPC we have to create 2 subnets:
    a)  public  subnet [ Accessible for Public World! ] 
    b)  private subnet [ Restricted for Public World! ]
3) Create a public facing internet gateway for connect our VPC/Network to the internet world and attach this gateway to our VPC.
4) Create  a routing table for Internet gateway so that instance can connect to outside world, update and associate it with public subnet. 
5) Launch an ec2 instance which has Wordpress setup already having the security group allowing  port 80 so that our client can connect to our wordpress site.
Also attach the key to instance for further login into it.
6) Launch an ec2 instance which has MYSQL setup already with security group allowing  port 3306 in private subnet so that our wordpress vm can connect with the same.
Also attach the key with the same.
Note: Wordpress instance has to be part of public subnet so that our client can connect our site. 
mysql instance has to be part of private  subnet so that outside world can't connect to it.
Don't forgot to add auto ip assign and auto dns name assignment option to be enabled.

This will give u proper understanding of workflow of task.

if you facing any issue go through this artical it's more clear with images.

https://www.linkedin.com/pulse/hybrid-multi-cloud-computing-task-3-komal-habura/?published=t
