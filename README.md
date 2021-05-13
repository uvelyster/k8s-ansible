# k8s-ansible

## set ip 
nmcli con mod "enp0s8" ipv4.address 172.16.0.201/24 ipv4.gateway 172.16.0.1 ipv4.method manual  

## no default route 
nmcli con mod enp0s8 ipv4.never-default yes  

## connection down & up
nmcli con down enp0s8  
nmcli con up enp0s8  
nmcli con up enp0s3  

## enable 
nmcli con mod "enp0s8" connection.autoconnect yes  
nmcli con mod "enp0s3" connection.autoconnect yes  

## set hostname
hostnamectl set-hostname master  

## check point  
2 core of master cpu  
more than 1700mb memory  
dns query
