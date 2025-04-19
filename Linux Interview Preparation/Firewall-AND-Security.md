ufw enable

ufw allow

ufw deny

ufw status

iptables -L

iptables -A INPUT -p tcp --dport 22 -j ACCEPT

iptables -D

iptables-save

iptables-restore

firewall-cmd --state

firewall-cmd --list-all

firewall-cmd --add-port=80/tcp

firewall-cmd --reload

semanage port -l

getenforce

setenforce

selinuxenabled

auditctl

ausearch

fail2ban-client status

chkrootkit

rkhunter

pam-auth-update

passwd -l

passwd -u

chage -l user

gpg

openssl

ssh-keygen

ssh-copy-id

