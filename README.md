# 在Linux中，你可以使用以下命令来查看本机的IPv6地址  
ip -6 addr show  
# 如果你只想查看特定接口的IPv6地址，比如 eth0，可以使用以下命令     
ip -6 addr show dev eth0  
# 红米ax5开放ipv6端口  
ip6tables -I forwarding_rule -p tcp --dport 56889 -j ACCEPT  
ip6tables -I forwarding_rule -p udp --dport 56889 -j ACCEPT  
设置开机自启（使用到rc.local服务）        1、命令行输入    vi /etc/rc.local   2、按 i  进入编辑模式，然后使用方向键移动光标到exit 0 上方，将上方两行代码粘贴进入3、按键盘左上方ESC键，推出编辑模式，紧接着输入  :wq  并按回车即推出保存！  
# 红米路由检查开放的ipv6端口  
ip6tables -L -v -n | grep "dpt"   
### md转docx   
python -c "import requests; exec(requests.get('https://raw.githubusercontent.com/linlpt/tool/main/md_to_docx.py').text)"
