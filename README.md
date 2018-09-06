# Laravel-project
This is an educational project developed on the framework of Laravel. Written for educational practice at the university on April 20, 2018.


To start, you need a Vagrant-box - Homestead

Installation & Setup
First Steps
Before launching your Homestead environment, you must install VirtualBox 5.2, VMWare, Parallels or Hyper-V as well as Vagrant. All of these software packages provide easy-to-use visual installers for all popular operating systems.

To use the VMware provider, you will need to purchase both VMware Fusion / Workstation and the VMware Vagrant plug-in. Though it is not free, VMware can provide faster shared folder performance out of the box.

To use the Parallels provider, you will need to install Parallels Vagrant plug-in. It is free of charge.

Because of Vagrant limitations, The Hyper-V provider ignores all networking settings.

Installing The Homestead Vagrant Box
Once VirtualBox / VMware and Vagrant have been installed, you should add the  laravel/homestead box to your Vagrant installation using the following command in your terminal. It will take a few minutes to download the box, depending on your Internet connection speed:

vagrant box add laravel/homestead
If this command fails, make sure your Vagrant installation is up to date.

Installing Homestead
You may install Homestead by cloning the repository. Consider cloning the repository into a  Homestead folder within your "home" directory, as the Homestead box will serve as the host to all of your Laravel projects:

git clone https://github.com/laravel/homestead.git ~/Homestead
You should check out a tagged version of Homestead since the master branch may not always be stable. You can find the latest stable version on the GitHub Release Page:

    cd ~/Homestead

// Clone the desired release...

    git checkout v7.16.1

Once you have cloned the Homestead repository, run the bash init.sh command from the Homestead directory to create the Homestead.yaml configuration file. The Homestead.yaml file will be placed in the Homestead directory:

// Mac / Linux...

    bash init.sh

// Windows...

    init.bat


Configuring Homestead

Setting Your Provider

The provider key in your Homestead.yaml file indicates which Vagrant provider should be used:  virtualbox, vmware_fusion, vmware_workstation, parallels or hyperv. You may set this to the provider you prefer:

    provider: virtualbox

   Configuring Shared Folders
The folders property of the Homestead.yaml file lists all of the folders you wish to share with your Homestead environment. As files within these folders are changed, they will be kept in sync between your local machine and the Homestead environment. You may configure as many shared folders as necessary:

folders:

    - map: ~/code
      to: /home/vagrant/code
      
