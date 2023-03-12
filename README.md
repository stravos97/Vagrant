Currently doesn't have: 

Shared Folder mounted
Abu Office Printers
QNAP network drive mounted



Setup Instructions:
Download Vagrant, it should be setup in the same os as virtualbox, e.g. if virtualbox is on windows, Vagrant should be used through powershell
Download Virtualbox, will only work with this and not Vmware
Might need to install vagrant extensions too
Whilst in dir of Vagrantfile and .box run the command "vagrant box add winxp winxp.box". 
run "vagrant up" whilst in dir of Vagrantfile (vagrantfile can be edited to provide more cpu, ram)
Even if there is no vagrant file we can run "vagrant up", we just won't have cpu and ram provisioning 


Making a .box file
Complete installation of virtualbox container of running os with everything you need already installed. Convention is username and password should both be vagrant (might be Vagrant)
To create a base box run "vagrant package -h"
run "VBoxManage list vms"
run "vagrant package --base winxp" (after --base is name of vm listed from previous command)
rename package.box to something useful e.g. winxp.box

General
Run vegrant reload if the Vagrantfile is edited and you want to reload the vm without losing important data
