首先安装面板免费版

Centos安装命令          yum install -y wget && wget -O install.sh http://download.bt.cn/install/install.sh && sh install.sh

Ubuntu/Deepin安装命令  wget -O install.sh http://download.bt.cn/install/install-ubuntu.sh && sudo bash install.sh

Debian安装命令         wget -O install.sh http://download.bt.cn/install/install-ubuntu.sh && bash install.sh

Fedora安装命令         wget -O install.sh http://download.bt.cn/install/install.sh && bash install.sh

然后升级专业版

wget -O update.sh http://download.bt.cn/install/update_pro.sh && bash update.sh pro

找到路径/www/server/panel/class 找到文件名或者直接搜索：common.py


搜索代码164行

data = panelAuth().get_order_status(None)

替换成

data = {'status' : True,'msg' : {'endtime' : 32503651199 }}

完成后，进入 /www/server/panel/data 新建一个文件 文件名为：userInfo.json 

内容空的，如果存在这个文件的删掉重新新建文件。
