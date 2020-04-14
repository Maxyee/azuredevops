# Redirect Http to Https

In this section, I will discuss the redirected user from the HTTP protocol to HTTPS protocol. The main reason why I am doing this because HTTP is not a secure protocol for passing data. On the other hand, Https can pass our data with security.

On the contrary, for the website, suppose the two protocol is open right now. when the user tries to hit the website URL using a browser where he wants to visit. At first, he will get the HTTP protocol website by default. However, it is not the perfect way to handle user on those HTTP protocol website. As a result, the website owner should redirect his/her visitors to the HTTPS protocol website.

As I am working with the Microsoft Azure virtual machine. thus, I will discuss for the windows operating hosting websites, how they can do this task from the IIS manager.

To begin with, we need the main element which will do this task. The element name is `URL Rewrite`. we can find it to our IIS manager directly or if we do not find it there, then we can install it by ourselves. 

In this case, I am installing the `URL Rewrite` to my IIS manager, because I did not find this element in my IIS manager.


