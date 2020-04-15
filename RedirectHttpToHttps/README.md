# Redirect Http to Https

In this section, I will discuss the redirected user from the HTTP protocol to HTTPS protocol. The main reason why I am doing this because HTTP is not a secure protocol for passing data. On the other hand, Https can pass our data with security.

On the contrary, for the website, suppose the two protocol is open right now. when the user tries to hit the website URL using a browser where he wants to visit. At first, he will get the HTTP protocol website by default. However, it is not the perfect way to handle user on those HTTP protocol website. As a result, the website owner should redirect his/her visitors to the HTTPS protocol website.

As I am working with the Microsoft Azure virtual machine. thus, I will discuss for the windows operating hosting websites, how they can do this task from the IIS manager.

To begin with, we need the main element which will do this task. The element name is `URL Rewrite`. we can find it to our IIS manager directly or if we do not find it there, then we can install it by ourselves. 

In this case, I am installing the `URL Rewrite` to my IIS manager, because I did not find this element in my IIS manager.

![alt text](https://github.com/Maxyee/azuredevops/blob/master/RedirectHttpToHttps/screenshots/IIsmanager.png)

As a result, I have to download the URL Rewrite module from the below link:

- [Url Rewrite module download](https://www.microsoft.com/en-us/download/confirmation.aspx?id=47337)

Now we downloaded the module from the website. However, let's install it and then apply it to our SSL manager.

![alt text](https://github.com/Maxyee/azuredevops/blob/master/RedirectHttpToHttps/screenshots/installUrlRewrite.png)

Here we successfully installed the Url Rewrite module to our IIS manager. Let's check it again from the application interface.

![alt text](https://github.com/Maxyee/azuredevops/blob/master/RedirectHttpToHttps/screenshots/showingUrlrewrite_LI.jpg)

Finally, we can see that there is an option now visible to the IIS manager and the option name is called `Url Rewrite`

Let's start our main task by using this module Url Rewrite. Open the module by clicking it. we will see there is another interface that will open. from here we will set rules for our redirect task.

![alt text](https://github.com/Maxyee/azuredevops/blob/master/RedirectHttpToHttps/screenshots/urlrewriteinterface.png)

Furthermore, we need to click the Add rules button from the Interface(look at the top photo for help to find out the `Add Rule` button). we can find this add rule button on the top side right corner of the Url Rewrite Interface. After clicking the Add rule button we will see another Interface.Select the Blank rule section and click OK

![alt text](https://github.com/Maxyee/azuredevops/blob/master/RedirectHttpToHttps/screenshots/addRule.png)

When we pressed the ok button we will see another Interface. From here we will write all the necessary things which will create our rules for redirecting user Http port to Https port.

![alt text](https://github.com/Maxyee/azuredevops/blob/master/RedirectHttpToHttps/screenshots/editInboundRule.png)
