# Vagrant Centos Lattice Diamond

## Overview

## Getting Started

### Prerequisites 

* [Vagrant](https://www.vagrantup.com)
* [VirtualBox](https://www.virtualbox.org)
* Lattice Diamond RPM file
* Lattice Diamond License.dat
* The `vagrant-vbguest` plugin

```
vagrant plugin install vagrant-vbguest
```


### Start VM

```
vagrant up
```

Wait quite a while for everything to install

Connect using 

```
vagrant ssh -- -Y
```

Run the Diamond IDE

```
/usr/local/diamond/3.12/bin/lin64/diamond &
```

You can copy files into the `work` directory so that they can be accessed 
from `/vagrant/work` in the IDE.



## References

### Vagrant

* [Vagrant Jenkins Example](https://github.com/Hiklas/vagrant-jenkins-deployment)
* [Vagrant shell example](https://github.com/Hiklas/vagrant_get_into_tech_php/blob/master/Vagrantfile)
* [Setting Mac address of VM](https://stackoverflow.com/questions/12538162/setting-a-vms-mac-address-in-vagrant)
* [CentOS7 and vbguest additions](https://github.com/hashicorp/vagrant/issues/8374)
* 

### Lattice

* [Download Diamond Software](http://www.latticesemi.com/latticediamond)
* [Get free license](http://www.latticesemi.com/Support/Licensing/DiamondAndiCEcube2SoftwareLicensing/DiamondFree.aspx)

### TinyFPGA

* [A-Series getting started guide](https://tinyfpga.com/a-series-guide.html)

