![Install WinServ2022 thumbnail](https://github.com/jonathansantacruz3/How-to-set-up-Windows-Server-2022-on-a-Hyper-V-virtual-machine/assets/151465848/82f3328a-5cad-4df8-8b04-9ceb2bb2b563)


<h1>How to set up Windows Server 2022 on a Hyper-V Virtual Machine</h1>
This tutorial summarizes the prerequisites and installation of Windows Server 2022 on a Hyper-V Virtual Machine .<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Hyper-V (Virtual Machines/Compute)
- Microsoft Official Evaluation Center

<h2>Operating Systems Used </h2>

- Windows 10</b> (22H2)

<h2>List of Prerequisites</h2>

- Hyper-V enabled
- Windows Server 2022 ISO Image

<h2>Installation Steps</h2>

Gain experience in server administration by deploying Windows Server 2022 using Hyper-V's virtual machines. I will walk through where to download a fully operational image of the OS and how to install it. By the end of the video, you will be that much more confident and tech savvy.

To do this project, make sure you have 2 things:

Hyper-V enabled & a fully functional ISO image of Windows Server 2022.

I already have my Hyper-V enabled and to download the image of the operating system head over to the official Microsoft downloads page by clicking on the link below.

https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2022  

This is the spot to download Server products and resources used for projects like this one. Download the ISO copy, enter the required information, choose the English 64-bit edition, and let's get this started.

![image](https://github.com/jonathansantacruz3/How-to-set-up-Windows-Server-2022-on-a-Hyper-V-virtual-machine/assets/151465848/fbb1eb97-0f34-45b1-ab58-2afcc0888758)


To open Hyper-V, type in Hyper-V in the search bar and select it from the option listed. There are multiple ways to create a virtual machine within this console. In the action drop down menu select create a new virtual machine.

This brings up the New Virtual Machine wizard to set up the configurations.

Specify name and location:

It is best practice to name it something simple and easy to remember. In this case WnServ22. The wizard gives the option to store the VM in a different location from the default which is the C drive. In this project we will stick with the default.
Specify Generation:

The wizard presents you with 2 options of the generation associated with the new VM. Generation 1 is suitable for legacy systems and generation 2 has more functionality and supports newer systems such as Server 2022. In this case we will go with Gen 2.

Assign memory:

The next step is assigning RAM memory. By default, it is 1 Gb, but I will assign it 4 Gb for faster processing. The dynamic memory option gives the machine the authority to adjust the memory it uses based on how much it needs which equals to better memory machine management.

Configure networking:

This step is sets the type of desired connectivity when dealing with the virtual switch. Since this is a project to practice let's choose a private switch to isolate from the host and other networks. The VM will still be able to connect with any other VM in the environment it is in.

Connect with Virtual hard disk:

It is time to set the amount of storage memory for the VM. The default allocates a maximum of 127 Gb of dynamically expanding memory. This means that it will monitor and only use what is necessary up to the configured memory size.

Installation Options:

In this window we will select to install the OS from a bootable image file. We will navigate to the location of our ISO image we downloaded from Microsoft and select it.

Summary:

The wizard will finally give us a summary of the configurations set for the new machine and since everything looks right, we will create it by pressing the "Finish" button.

After it is done doing its thing we will select the machine by right clicking it and press connect. The new window that populates will give a Start option which we choose to start the boot process.

It brings us to the OS installation wizard and follow the steps. It gives us a few options of what type of interface we would like to install. For this video we will choose the standard desktop experience to interface with the OS with a GUI instead of the command line.

We will accept the terms and conditions and select the custom install to designate the desired drive we wish to install the OS.


Set a password and press finish. After signing on it will set up the services and user settings that come with the OS.

Ready to go!
