# Appliance Formats

SUSE Studio helps you build your appliance in a variety different formats. Each format is used for a different purpose:

##Physical media formats##

**USB stick/hard disk image**
Dump this format on your USB stick or hard disk and boot from it. You may need to instuct the machine's BIOS to boot from an external source if you're usign a USB stick. You can write the disk image using either the `dd` command, or image writing software on any existing OS.

Live USB sticks provide a high-performance option for creating a portable, persistent image using the same data that would be present on a hard drive.

**Live CD/DVD (.iso)**
Use this format if you want to burn your appliance on CD or DVD. This is the easiest way to prepare bootable media; simply download the .iso file, and burn it to disk via any existing OS.

Live discs provide a complete bootable image of your appliance which will run in a computer's memory, rather than loading from the hard drive. This allows end users to experience and evaluate your appliance without installing it or making any changes to their existing system. Live discs are unique because they can run on a computer without a hard drive, or act as rescue systems for computers with a corrupted hard drive or file system.

**Preload ISO (.iso)**
This is an ideal format if you planning to do installations on physical machines, when you do not require a 'live' experience (running from the media *without installing*).  Your appliance's disk image will be wrapped in a simple bootable installer that asks only which hard disk to install to. Your installation media can be prepared on any existing OS by simply burning the .iso file to disc.

##Virtual formats##

**VMware / VirtualBox / KVM (.vmdk)**
Use this format if you want to start your appliance as a virtual machine on VMware, VirtualBox, or KVM-based hypervisors. This is another method to test an appliance without formatting any hard disk. [VirtualBox](https://www.virtualbox.org/) and [VMware](http://www.vmware.com/products/player/) virtualization applications are available for most host operating systems.  [KVM](http://www.linux-kvm.org) virtualization is for Linux only.

**OVF virtual machine (.ovf)**
[Open Virtualization Format (OVF)](http://www.dmtf.org/standards/ovf) is an open, standards-based format for virtual machines.  A variety of hypervisors including SUSE Cloud, VirtualBox, VMware ESX, IBM SmartCloud, and Oracle VM support creating virtual machines by importing an .ovf file.

In order to use the an OVF image, you may require the `ovftool` from VMware. Due to licensing issues we cannot distribute the tools with SUSE Studio at the moment. Download links, installation instructions, and documentation are available at <http://communities.vmware.com/community/vmtn/server/vsphere/automationtools/ovf>.

**Xen guest**
Use this format if you want to run your appliance on a Xen host system, such as SUSE Linux Enterprise Server. Xen guests works only on Xen-enabled Linux hosts, including many virtual hosting providers.

See the [SLES Xen Book](http://www.suse.com/documentation/sles11/book_xen/?page=/documentation/sles11/book_xen/data/book_xen.html) for more information on Virtualization with Xen in SUSE Linux.

**Hyper-V (.vhd)**
This format allows seamless integration with Microsoft's Hyper-V virtualization, available in Windows Server.  Your appliance will include all the necessary drivers to integrate with the Hyper-V management console and provide optimum performance.  A Hyper-V-enabled Microsoft Windows Server is required to run this format.

See [Microsoft's Windows Server Library](http://technet.microsoft.com/library/cc794868%28WS.10%29.aspx) for more information on virtualizing with Hyper-V.

##Cloud formats##

**Amazon EC2 image**
If you plan to use Amazon Web Services to host your server, this format will properly configure the appliance for you do to so. Link your AWS credentials to your Studio account, and you will be able to upload and launch EC2 instances directly from SUSE Studio. See [Use > Amazon EC2](../use/amazon-ec2.html) for more information.

**Azure Image**
Windows Azure is another option for hosting your appliances. The Azure Image format will do the hard work for you, building a .vhd file tailored for hosting on Microsoft's Windows Azure service. Upload your Azure publishsettings file to your Studio account, and you will be able to create images on Windows Azure, then jump over to the management portal to instantiate and manage your virtual machines. See [Use > Windows Azure](../use/windows-azure.html) for more information.
