# change root password
passwd root
# install wget
yum -y install wget
# install shadowsocks
wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-go.sh  
chmod +x shadowsocks-go.sh  
./shadowsocks-go.sh 2>&1 | tee shadowsocks-go.log

使用命令：
启动：/etc/init.d/shadowsocks start
停止：/etc/init.d/shadowsocks stop
重启：/etc/init.d/shadowsocks restart
状态：/etc/init.d/shadowsocks status

# install python3
yum -y update
yum -y install yum-utils
yum -y groupinstall development
yum -y install https://centos7.iuscommunity.org/ius-release.rpm
yum -y install python36u
python3.6 -V
yum -y install python36u-pip
yum -y install python36u-devel

# set up virtual enviroment
mkdir environments
cd environments
python3.6 -m venv my_env

# load virtual enviroment
source my_env/bin/activate

# xvfb for headless server 
yum install xorg-x11-server-Xvfb

# install firefox
yum install firefoxfir

# install geckodriver
wget https://github.com/mozilla/geckodriver/releases/download/v0.18.0/geckodriver-v0.18.0-linux64.tar.gz
tar -xvzf geckodriver-v0.18.0-linux64.tar.gz 
chmod +x geckodriver

# install python3 module
pip3.6 install openpyxl selenium pyvirtualdisplay

# google drive API install
pip install --upgrade google-api-python-client

# gdrive
https://github.com/prasmussen/gdrive/

