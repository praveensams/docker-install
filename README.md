# docker-install

rpm -q ansible || {
yum install epel-release -y 
yum install git -y
yum install ansible -y
}

rpm -q ansible || { echo " Unable to install ansible " ; exit 9 ; }

 ansible-pull -i localhost -U https://github.com/praveensams/docker-install.git docker.yml
