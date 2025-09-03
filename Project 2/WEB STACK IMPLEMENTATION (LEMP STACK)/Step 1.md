# STEP 1 – INSTALLING THE NGINX WEB SERVER

In order to display web pages to our site visitors, we are going to employ Nginx, a high-performance web server. We’ll use the apt 
package manager to install this package.

```
sudo apt update
sudo apt install nginx
```

When prompted, enter Y to confirm that you want to install Nginx. Once the installation is finished, the Nginx web server will be 
active and running on your Ubuntu 20.04 server.

To verify that nginx was successfully installed and is running as a service in Ubuntu, run:

```
sudo systemctl status nginx
```

Before we can receive any traffic by our Web Server, we need to open TCP port 80 which is default port that web brousers use to 
access web pages in the Internet.




Our server is running and we can access it locally and from the Internet (Source 0.0.0.0/0 means ‘from any IP address’).

First, let us try to check how we can access it locally in our Ubuntu shell, run:

```
curl http://localhost:80
or
curl http://127.0.0.1:80
```


Now it is time for us to test how our Nginx server can respond to requests from the Internet.
Open a web browser of your choice and try to access following url


```
http://<Public-IP-Address>:80
```

Another way to retrieve your Public IP address, other than to check it in AWS Web console, is to use following command:

```
curl -s http://169.254.169.254/latest/meta-data/public-ipv4
```


The URL in browser shall also work if you do not specify port number since all web browsers use port 80 by default.

If you see following page, then your web server is now correctly installed and accessible through your firewall.


![projje2-step0](https://user-images.githubusercontent.com/85270361/210116186-f5ec30cf-5fe3-410d-9c21-2f26b03c4815.PNG)

