# Task 15

## Description:

í ½í´…Create an ansible role myapache to configure Httpd WebServer.

í ½í´…Create another ansible role myloadbalancer to configure HAProxy LB.

í ½í´…We need to combine both of these roles controlling webserver versions  and solving challenge for host ip's  addition  dynamically over  each Managed Node  in  HAProxy.cfg file.


## Solution

created Roles for this:

- myapache          Role     : Role for creating simple webserver
- mylb              Role     : Role for creating loadbalancer
- remove_mylb       Role     : Role for Deleting Simple Webserver
- remove_mylb       Role     : Role for Deleting Loadbalacer Setup
- setup.yml         Playbook : Playbook to create Loadbalancer - webserver Setup
- remove_setup.yml  Playbook : Playbook to Delete Loadbalancer - webserver Setup



<b>

Imp: First make group in inventory with tag as lb and webserver. Then play this playbook.

---
Inventory:

[lb]
Ip0 ... ... ...

[webserver]
ip0 ...  ... ....
ip1 ... ... ...
ip2 ... ... ...
ip3 ... ... ..

...




Command : ansible-playbook setup.yml 
Command : ansible-playbook remove_setup.yml       
</b>

#NOTE: System should have pip and ansible before running this playbook. 

Thank You 


CREATER: Kaushal Soni

