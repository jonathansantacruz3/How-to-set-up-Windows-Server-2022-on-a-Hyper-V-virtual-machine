
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

![image](https://github.com/jonathansantacruz3/How-to-set-up-Windows-Server-2022-on-a-Hyper-V-virtual-machine/assets/151465848/00678824-b5eb-4333-ba7a-5e84cf6b18a5)


To open Hyper-V, type in Hyper-V in the search bar and select it from the option listed. There are multiple ways to create a virtual machine within this console. In the action drop down menu select "NEW" then "Virtual Machine..." to create a new virtual machine.

This brings up the New Virtual Machine wizard to set up the configurations. 

![image](https://github.com/jonathansantacruz3/How-to-set-up-Windows-Server-2022-on-a-Hyper-V-virtual-machine/assets/151465848/64c12348-b8dd-4a2e-a40e-0c0c3d790312)

![image](https://github.com/jonathansantacruz3/How-to-set-up-Windows-Server-2022-on-a-Hyper-V-virtual-machine/assets/151465848/46d597e8-928f-4579-a15c-f0ea266be05f)

Click on "Next" to take you to the configuration setup. 

<h3>Specify name and location:</h3>

It is best practice to name it something simple and easy to remember. In this case, I went with WnServ22. The wizard gives the option to store the VM in a different location from the default which is the C drive. In this project we will stick with the default.

![image](https://github.com/jonathansantacruz3/How-to-set-up-Windows-Server-2022-on-a-Hyper-V-virtual-machine/assets/151465848/d998f5ae-2271-4c4b-9cb2-816040424dc3)


<h3>Specify Generation:</h3>

The wizard presents you with 2 options of the generation associated with the new VM. Generation 1 is suitable for legacy systems and generation 2 has more functionality and supports newer systems such as Server 2022. In this case we will go with Gen 2.

![image](https://github.com/jonathansantacruz3/How-to-set-up-Windows-Server-2022-on-a-Hyper-V-virtual-machine/assets/151465848/c85e71a3-e08d-4787-a796-7a92b94fb44e)


<h3>Assign memory:</h3>

The next step is assigning RAM memory. By default, it is 1 GB, but I will assign it 4 GB (4096 MB) for faster processing. The dynamic memory option gives the machine the authority to adjust the memory used based on how much it needs which equals to better memory machine management. Make sure you have the proper amount of memory to assign your virtual machine or else it will give you an error when it attempts to boot up. You can check your system's utility "System Information", by typing it in the search bar, and it will display how much memory your host machine has available. 

![image](https://github.com/jonathansantacruz3/How-to-set-up-Windows-Server-2022-on-a-Hyper-V-virtual-machine/assets/151465848/7361a4dd-da56-4265-a793-dcf9d15ffcab)


<h3>Configure networking:</h3>

This step is sets the type of desired connectivity when dealing with the virtual switch. Since this is a project to practice in, let's choose a private switch to isolate from the host and other networks. The VM will still be able to connect with any other VM in the environment it is in. If it does not give you an option for a private switch like it did on my computer, then go to the Hyper-V console, and in the "Virtual Switch Manager" option under the "Actions" panel, add Private from the list of switch types. Create a new name for it and click OK. It should now appear in the drop down menu when confuguring your virtual switch in the wizard. 

![image](https://github.com/jonathansantacruz3/How-to-set-up-Windows-Server-2022-on-a-Hyper-V-virtual-machine/assets/151465848/ab8b47c9-5c94-49b5-a7ed-474114c8f8a4)

![image](https://github.com/jonathansantacruz3/How-to-set-up-Windows-Server-2022-on-a-Hyper-V-virtual-machine/assets/151465848/70899dff-f2e1-4b63-9aed-7e44299776d8)

![image](https://github.com/jonathansantacruz3/How-to-set-up-Windows-Server-2022-on-a-Hyper-V-virtual-machine/assets/151465848/82332afb-d41f-4ffc-93bc-0a9d6348f755)


![image](https://github.com/jonathansantacruz3/How-to-set-up-Windows-Server-2022-on-a-Hyper-V-virtual-machine/assets/151465848/1fc139f4-96ec-47bf-bfd8-039d0d3e537d)


<h3>Connect with Virtual hard disk:</h3>

It is time to set the amount of storage memory for the VM. The default allocates a maximum of 127 Gb of dynamically expanding memory. This means that it will monitor and only use what is necessary up to the configured memory size. We can leave it as the default for out educational purposes. It also gives you the option to set a virtual hard disk or attach one later.  

![image](https://github.com/jonathansantacruz3/How-to-set-up-Windows-Server-2022-on-a-Hyper-V-virtual-machine/assets/151465848/b2081241-50e8-4f29-aa77-60b52630ad91)


<h3>Installation Options:</h3>

In this window we will select to install the OS from a bootable image file. We will navigate to the location of our ISO image we downloaded from Microsoft and select it.

![image](https://github.com/jonathansantacruz3/How-to-set-up-Windows-Server-2022-on-a-Hyper-V-virtual-machine/assets/151465848/97ef2953-2230-466a-a772-1204ed22a687)


<h3>Wizard Summary:</h3>

The wizard will finally give us a summary of the configurations set for the new machine and since everything looks right, we will create it by pressing the "Finish" button.

![image](https://github.com/jonathansantacruz3/How-to-set-up-Windows-Server-2022-on-a-Hyper-V-virtual-machine/assets/151465848/1c62e76b-c0e9-470e-85ee-3014e27b5867)


After it is done doing its thing we will select the machine by right clicking it and press connect.

![image](https://github.com/jonathansantacruz3/How-to-set-up-Windows-Server-2022-on-a-Hyper-V-virtual-machine/assets/151465848/881071f8-919a-46fa-974c-3d76e6a5fc47)

The new window that populates will give a Start option which we choose to start the boot process. CTL + ALT + DEL to intercept the boot and start the installation process. 

![image](https://github.com/jonathansantacruz3/How-to-set-up-Windows-Server-2022-on-a-Hyper-V-virtual-machine/assets/151465848/5643a084-e92f-4a9f-9ae0-31ea6bdb8b1c)


It brings us to the OS installation wizard and here we follow the steps. It gives us a few options of what type of interface we would like to install. For this video we will choose the standard desktop experience to interface the OS with a GUI (graphical user interface) instead of the command line. 



![image](https://github.com/jonathansantacruz3/How-to-set-up-Windows-Server-2022-on-a-Hyper-V-virtual-machine/assets/151465848/db24eb73-953c-4f43-893f-6e10d630e08b)


We will accept the terms and conditions and select the custom install to designate the desired drive we wish to install the OS.

![image](https://github.com/jonathansantacruz3/How-to-set-up-Windows-Server-2022-on-a-Hyper-V-virtual-machine/assets/151465848/ab7652ba-96ce-4cf5-9fc9-6b73c07c8e40)


Set a password and press "Finish". After signing on, it will set up the services and user settings that come with the OS.

![image](https://github.com/jonathansantacruz3/How-to-set-up-Windows-Server-2022-on-a-Hyper-V-virtual-machine/assets/151465848/ad0fa1c1-0509-4bf7-964e-2ebf548901d3)


Ready to go!
