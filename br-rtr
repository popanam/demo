#!bin/bash\r





hostnamectl set-hostname br-rtr;

cat > /etc/sysconfig/network <<EOF
NETWORKING=yes
CONFMETHOD=etcnet
HOSTNAME=br-rtr.au-team.irpo
DOMAINNAME=localdomain
RESOLV_MODS=yes
EOF

#Chrony
sed -i 's/pool pool.ntp.org iburst/pool 172.16.1.1 iburst/g'
systemctl restart chronyd




#Время
apt-get update
apt-get install tzdata
find /usr/share/zoneinfo -name Krasnoyarsk
timedatectl set-timezone Asia/Krasnoyarsk
timedatectl

exec bash
