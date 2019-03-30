this is a demo to deploy darknet yolov3 on AWS lambda. using a docker amazonlinux to compile the code.


sudo docker run -it dacut/amazon-linux-python-3.6

yum clean all
yum makecache
yum update
#as China GFW make some rpm undownloadable.we use this package.
yum install -y busybox
#busybox wget http://10.162.2.100/amazonLinuxRPM.tar
busybox tar xf amazonLinuxRPM.tar 
yum install -y *.rpm

yum install -y git
yum install -y vim
git clone https://github.com/pjreddie/darknet
cd darknet
make


