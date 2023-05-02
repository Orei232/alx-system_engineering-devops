Secured and Monitored Web Infrastructure
Visit Board

Description
This is a 3-server web infrastructure that is secured, monitored, and serves encrypted traffic.
Firewall filters network tarffic in and out a machine

HTTPS is setup so that if someone intercepts the ttraffic, it cannot be read.


Mointoring can be used to check if somthing is broken or slow.


The monitoring setup is composed of a client collecting and sending data and sending it to the monitoring syatem.


Configure monitoring to:collect web server data and have an alert triggered if QPS is getting out of control.


Terminating SSL at the laod balancer level is an issue because the traffic between the load balancer and the web servers is unencrypted.

`
Having only one MySQL server capable of accepting writes is an issue because if the master goes down, the application cannot write to the database anymore.


Having servers with all the smae componets (database, web server and application server) might be a problem because their consumption will not grow the same way between each of them (we might want to have more database servers than application servers for instance).


Having servers with all the same components (database, web server and application server) might be a problem because when there is maintenance performed on a server for a specific component, it will affect other componeents that are on it.


Load-balancer is a SPOF

Specifics About This Infrastructure
The purpose of the firewalls.
The firewalls are for protecting the network (web servers, anyway) from unwanted and unauthorized users by acting as an intermediary between the internal network and the external network and blocking the incoming traffic matching the aforementioned criteria.
The purpose of the SSL certificate.
The SSL certificate is for encrypting the traffic between the web servers and the external network to prevent man-in-the-middle attacks (MITM) and network sniffers from sniffing the traffic which could expose valuable information. The SSL certs ensure privacy, integrity, and identification.
The purpose of the monitoring clients.
The monitoring clients are for monitoring the servers and the external network. They analyse the performance and operations of the servers, measure the overall health, and alert the administrators if the servers are not performing as expected. The monitoring tool observes the servers and provides key metrics about the servers' operations to the administrators. It automatically tests the accessibility of the servers, measures response time, and alerts for errors such as corrupt/missing files, security vulnerabilities/violations, and many other issues.
Issues With This Infrastructure
Terminating SSL at the load balancer level would leave the traffic between the load balancer and the web servers unencrypted.
Having one MySQL server is an issue because it is not scalable and can act as a single point of failure for the web infrastructure.
Having servers with all the same components would make the components contend for resources on the server like CPU, Memory, I/O, etc., which can lead to poor performance and also make it difficult to locate the source of the problem. A setup such as this is not easily scalable.