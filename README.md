# create-openvz-templet-Centos-Cpanel
openvz templet Centos Cpanel Creation

Login to OpenVZ(Hardware Node).

Start the VM for the template creation.(replace 105 with your container ID)

vzctl start 105

Remove the IP from the VM.

sudo vzctl set 105 --ipdel all --save

Stop the container.

vzctl stop 105

Create template

cd /vz/private/105/

tar -czf /vz/template/cache/<OS>-<ARCH>.tar.gz ./

Create the configuration file.

cp /etc/vz/dists/centos.conf /etc/vz/dists/template-name.conf


=============================== instant openvz cpanel templet
https://linux-os-templates.googlecode.com/svn/trunk/centos/
or
https://www.dropbox.com/s/rrdv79hpvranh1r/centos-6-cpanel-64-bit.tar.gz?dl=0
