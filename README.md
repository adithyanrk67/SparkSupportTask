# SparkSupport AWS Task
                                                                         Iam user adithyan
                                                                        Aws region =  Asia Pacific (Mumbai)ap-south-1

Step1:

⦁	Select EC2 instance service

⦁	On the left side of the page select -load balancing - Load balacers -

⦁	Click create load balancer

⦁	Click create application load balance which support HTTP and HTTPS

	Load balancer name = Spark
  
	scheme = internet-facing
  
	IP address type = IPv4
  
 	Availability zones = Selected all the availability zones
  
	Listener = HTTP:80
  
⦁	Created a target group 

	Target group name = SparkGroup
  
  
  

Step2:

⦁	Launch a new ec2 instance

⦁	Create  Ubuntu Server 20.04 LTS (HVM)

⦁	select  t2 micro free tier 

⦁	Rivew and launch the instance giving the necessary details

⦁	click the running instance and click connect

- Installed PuTTY on my windows machine and connected to the ubantu server

-used following commands
 
	$sudo apt-get update
  
 	$sudo apt install nginx
  
	$sudo systemctl restart nginx
  
	$cd /var/www/html
  
	$ls
  
  $sudo rm index.nginx-debian.html
  
	$sudo nano index.nginx-debian.html 
  
  -(I have rewrite the code given in task index1.html)
  
	$clear
  
	-It is working fine in the ip address 13.233.22.38 also the web page is visible.
  
  
  
  
Step3:


⦁	Launch a new EC2 instance and repeat step 2

	-When it reached to
  
$sudo nano index.nginx-debian.html
  
	-(Rewrite the code given in task index2.html)
  
	-It is working fine in the ip address 3.110.31.20 also the web page is visible.
  
  

Step4:

⦁	Now go to Target groups

⦁	Select SparkGroup

⦁	Go to targets

⦁	Register targets 

⦁	Select our instances

⦁	Include as pending targets

⦁	Register pending targets



Load balancer endpoint result

!!  Two targets successfully registerd into spark group

Total targets = 2

Healthy = 2

Unhealthy = 0 

 
