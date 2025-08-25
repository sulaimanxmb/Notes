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









