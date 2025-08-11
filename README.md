# linuxlab
bash scripting mastery cc4.1
echo -n "CPU Info" 
lscpu | grep Model

echo -n "CPU Info" 
cat /proc/cpuinfo | grep MHz

user=$(whoami)
hostname=$(hostname)
echo "current user: $user@$hostname"

Memory=$free_memory
echo -n "Free Memory"
free -h |grep Mem

Swap=$free_swap
echo -n "Swap Space"
free -h | grep Swap

Partitions=$free_Space
echo -n "Free ext4"
df -hT | grep ext4

Partitions=$free_Space
echo -n "Free XFS"
df -hT | grep xfs

IPaddress=$IPAddress
echo -n "IP Address/CIDR"
nmcli dev show | grep 'IP4\.ADDRESS\|IP4.NETMASK'
