# DynaliteCGI
A CGI like (C# and ASP.Net) Web Application that sends and receives 8 byte DyNet Messages to / from the Philips Dynalite home automation system

I used Windows with IIS and .Net 4.6 Installed.
I used the Philips Dynalite DDNG100BT as the the DyNet GateWay (configured with Passive TCP and UDP enabled)

First You need to have a Web Server that Hosts ASP.Net Web Applications.

Instructions To Use with Internet Information Services (IIS):

Create a folder inside where IIS is hosting (default is C:\Inetpub\wwwroot\) to place the files
Copy the files from the zip file to the folder
Inside the (Internet Information Services (IIS) Manager) convert the folder to a Web Application


Inside DyNet.aspx.cs File - Modify the three lines below to your TCP Port, UDP Port, And the IP of the DyNet GateWay

    private const int UDP_PORT = 12345;  //Change Port to the UDP port to your DyNet Ethernet gateway
    private const int TCP_PORT = 12345;  //Change Port to the TCP port to your DyNet Ethernet gateway
    private const string DYNET_IP = "192.168.1.2";   //Change IP to your DyNet Ethernet gateway
