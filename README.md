sudo su


cd /home/ubuntu
git clone https://github.com/nitesh8860/anskube.git
git checkout final
cd anskube/
sh installansible

mkdir /etc/ansible/group_vars
cp inventory/group_vars/all.yml /etc/ansible/group_vars/
cp inventory/localhost.ini /etc/ansible/
cd /etc/ansible/
cp hosts hosts.original
mv localhost.ini hosts

run above commands on all VM
setup ssh connectivity on all nodes
try to connect with every nodes using ssh manually  OR ssh-keyscan
ansible -m ping all


