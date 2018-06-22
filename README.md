# Vagrant file for of-config along with netopeer-cli

<big> Refer to the link for  [of-config](https://github.com/openvswitch/of-config)

<big> of-config is a netconf agent for OpenVSwitch

<big> Refer to the link for  [netopeer](https://github.com/CESNET/netopeer) 

<big> netopeer serves as a netconf client.

<big> This vagrantfile works seemlessly with an installed [Virtualbox](https://www.virtualbox.org/)

```
virtualbox --help
Oracle VM VirtualBox Manager 5.1.34_Ubuntu
```

<big>Copy the Vagrantfile on to a directory and issue the commands

```
vagrant up
vagrant ssh
```
<big> To open multiple ssh connections with the VM
```
vagrant global-list
vagrant ssh <VM_id>
```
<big> Inside the VM the following command starts the of-config server
```
sudo su
ofc-server -v 3 -f
```
<big> On another ssh terminal 
```
sudo su
netopeer-cli
netconf> connect --login vagrant localhost
vagrant@localhost password: vagrant
netconf> get
netconf> get-config running
```





