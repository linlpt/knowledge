#在Linux中，你可以使用以下命令来查看本机的IPv6地址  
ip -6 addr show  
#如果你只想查看特定接口的IPv6地址，比如 eth0，可以使用以下命令     
ip -6 addr show dev eth0  
#红米ax5开放ipv6端口  
ip6tables -I forwarding_rule -p tcp --dport 3389 -j ACCEPT  
ip6tables -I forwarding_rule -p udp --dport 3389 -j ACCEPT  
#红米路由检查开放的ipv6端口
ip6tables -L -v -n | grep "dpt" 
