# Adding an SSL certificate to Microsoft Azure Cloud Service virtual machine.

I will describe the full procedure one by one, how we can add an SSL certificate to our website which is running on the virtual machine

To begin with, I need to connect our virtual machine to our local machine first. for doing that I need an RDP file that can be downloaded from the Azure portal virtual machine section.

![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/RDPscreen.jpg)

After downloading the RDP file, I need to open that file and then give the credentials for the Azure Virtual machine such as username, password.

However, successfully connected to the Azure virtual machine, I need to open the server manager application.

![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/serverManager.png)

Furthermore, there is a section called tools on the upper right corner of that application, then I clicked on that section for opening the Internet Information Services (IIS) Manager. Below Screenshot will give a more clear idea.

![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/InkedtoolsServices_LI.jpg)

This will open another application window into the virtual machine like this

![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/ISSmanager.png)

From the IIS Manager application, I click the virtual machine from the left sidebar and then click the 
