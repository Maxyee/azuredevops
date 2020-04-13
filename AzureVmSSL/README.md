# Adding an SSL certificate to Microsoft Azure Cloud Service virtual machine.

I will describe the full procedure one by one, how we can add an SSL certificate to our website which is running on the virtual machine

To begin with, I need to connect our virtual machine to our local machine first. for doing that I need an RDP file that can be downloaded from the Azure portal virtual machine section.

![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/RDPscreen.jpg)

After downloading the RDP file, I need to open that file and then give the credentials for the Azure Virtual machine such as username, password.

However, successfully connected to the Azure virtual machine, I need to open the server manager application from the virtual machine.

![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/serverManager.png)

Furthermore, there is a section called tools on the upper right corner of that application, then I clicked on that section for opening the Internet Information Services (IIS) Manager. Below Screenshot will give a more clear idea.

![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/InkedtoolsServices_LI.jpg)

This will open another application window into the virtual machine like this

![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/ISSmanager.png)

From the IIS Manager application, I click the virtual machine from the left sidebar and then click the sites folder. However, from the site folder, we will see the website folder for this website we will implement the certificate. The below screenshot will help us to find out what I want to say.

![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/websiteScreen.png)

On the contrary, For implementing the Http SSL service certificate, the website should enable port number 80. Moreover, if we want to implement the SSL certificate for Https service, we should enable the port number 443. Because Http can recognize port 80. On the other hand, Https can recognize the port number  443.

![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/bindingShot.jpg)

After clicking the binding option, we will find the port number adding section. Now If anybody needs any port for adding the SSL certificate, he/she can add the port number here. For my working purpose, I will connect my SSL certificate to the port number 443 because I want to use the https service.

![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/addPort.png)
![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/websiteScreen.png)
