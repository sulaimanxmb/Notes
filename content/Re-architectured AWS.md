#### Services :
Elastic Beenstalk --> Instead of EC2, autoscalling instance to run tomcat frontend
ELB in beenstalk --> instead of ELB
RDS --> for Database
Active MQ --> instead of Rabbit MQ
Elastic cache --> instead of Memcached
Route 53
Cloudfront --> Content delivery network

#### Architecture diagram :

![[Pasted image 20250825115648.png]]

#### Steps :
##### Security groups :

First we have the backend SG for all backend services ie RDS, Active MQ, elastic cache etc. set thier inbound rules to `All traffic from that own SG`

##### RDS :
To change the configuration of a RDS first create a __parameter group__ with desired configurations and then make.a RDS with that parameter group selected

After creating parameter group create __DB subnet group__ selecting your VPC

now create a RDS with everything (we used SQL 8.0.39)

##### Elasti cache :
Create a Parameter group first (We used memecached 1.6)
Also create a Subnet Group
Now create a Elasti-cache 












