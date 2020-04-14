# Adding an SSL certificate to Microsoft Azure Cloud Service virtual machine.

I will describe the full procedure one by one, how we can add an SSL certificate to our website which is running on the virtual machine

## Virtual Machine Connection

To begin with, I need to connect our virtual machine to our local machine first. for doing that I need an RDP file that can be downloaded from the Azure portal virtual machine section.

![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/RDPscreen.jpg)

After downloading the RDP file, I need to open that file and then give the credentials for the Azure Virtual machine such as username, password.

## Server Manager

However, successfully connected to the Azure virtual machine, I need to open the server manager application from the virtual machine.

![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/serverManager.png)

## IIS Service Manager

Furthermore, there is a section called tools on the upper right corner of that application, then I clicked on that section for opening the Internet Information Services (IIS) Manager. Below Screenshot will give a more clear idea.

![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/InkedtoolsServices_LI.jpg)

This will open another application window into the virtual machine like this

![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/ISSmanager.png)

From the IIS Manager application, I click the virtual machine from the left sidebar and then click the sites folder. However, from the site folder, we will see the website folder for this website we will implement the certificate. The below screenshot will help us to find out what I want to say.

![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/websiteScreen.png)

On the contrary, For implementing the Http SSL service certificate, the website should enable port number 80. Moreover, if we want to implement the SSL certificate for Https service, we should enable the port number 443. Because Http can recognize port 80. On the other hand, Https can recognize the port number  443.

## Bindings

![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/bindingShot.jpg)

After clicking the binding option, we will find the port number adding section. Now If anybody needs any port for adding the SSL certificate, he/she can add the port number here. For my working purpose, I will connect my SSL certificate to the port number 443 because I want to use the https service.

![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/addPort.png)

## Server Certificates

Collect cer certificate file form an SSL service company. In this case, My company glostars brought an SSL certificate from a company called Digicert. After buying the certificate, the company sends me a .cer file which I will add to my IIS server manager. However, now I have to navigate the `server certificates` section. The option can be found in this way.

![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/serverCertificates.jpg)

## Complete certificate request

When I open the server certificate section, I get another interface. From that interface, I click the button called `complete certificate request`. The screenshot is given below-

![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/completeRequest.jpg)

this complete certificate request open another interface and from there I can upload the .cer file. The most important thing in this section is that I have to give a friendly name for my certificate. Thus, my point of view, I give the friendly name as `glostarsCr` and then press the ok button. This screenshot will give a clear idea.

![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/uploadCerFile.png)

Now we can see that my certificate is added to the server certificate section.

![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/showuploadedCertificate.jpg)

## Assigning Certificate With Https 443

Ninety percent (90%) work done. We are very close to finishing our tasks. Therefore, we should connect this certificate with our https port which is 443. As I mentioned earlier, We had made two port which is into the website `binding` section. Just open that binding section again from the IIS server manager. Finally, select the `https` from that binding and click on the `Edit` button.  

![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/siteBindingsEdit.jpg)

When we clicked the edit button we will see that there is another dropdown section below that interface. select the friendly name which we already mentioned when we uploaded the .cer certificate on the server certificates section.

![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/assignFriendlyaddress.png)

## Restart

Now all set, last one task left which is so simple. Just restart the IIS manager server and check the Url. We will see that our SSL certificate is attached with our website domain.

![alt text](https://github.com/Maxyee/azuredevops/blob/master/AzureVmSSL/screenshots/restart_LI.jpg)

Thank you. Happy DevOps !!!
