### 在Linux中，你可以使用以下命令来查看本机的IPv6地址  
ip -6 addr show  
### 如果你只想查看特定接口的IPv6地址，比如 eth0，可以使用以下命令     
ip -6 addr show dev eth0  
### 红米ax5开放ipv6端口  
ip6tables -I forwarding_rule -p tcp --dport 56889 -j ACCEPT  
ip6tables -I forwarding_rule -p udp --dport 56889 -j ACCEPT  
设置开机自启（使用到rc.local服务）        1、命令行输入    vi /etc/rc.local   2、按 i  进入编辑模式，然后使用方向键移动光标到exit 0 上方，将上方两行代码粘贴进入3、按键盘左上方ESC键，推出编辑模式，紧接着输入  :wq  并按回车即推出保存！  
### 红米路由检查开放的ipv6端口  
ip6tables -L -v -n | grep "dpt"   
### md转docx   
python -c "import requests; exec(requests.get('https://raw.githubusercontent.com/linlpt/tool/main/md_to_docx.py').text)"
### plex无法添加媒体库的原因
你启动后没有被Plex认证为服务端。如果是docker安装的话，要添加一个环境变量PLEX_CLAIM，变量值是用账号登录Plex官网获得的token，有效时间4分钟，有效期内用token启动容器才能激活服务端功能。
如果是其他平台，如群晖套件的plex，没有媒体库选项的话大概也是这个原因
### 挂载smb目录到本地
sudo mount -t cifs -o username=****,password=*****,vers=3.0,uid=1000,gid=1001,file_mode=0777,dir_mode=0777 //192.168.0.111/other /vol1/1000/smb2   
其中uid和gid可以通过 id命令获取
