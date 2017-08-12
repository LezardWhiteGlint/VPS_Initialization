# change root password
passwd root
# install wget
yum -y install wget
# install shadowsocks
wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-go.sh  
chmod +x shadowsocks-go.sh  
./shadowsocks-go.sh 2>&1 | tee shadowsocks-go.log
