# Wifi-MITM Threate & WireGuard Mitigation

<h1>Description</h2>
In this Wifi MITM project, we examine the privacy concern connected with WIFI in general. We examine the use of VPN, more specifically installing an VPN instance on the cloud for minimal to no logs for optimal privacy in order to protect our digital privacy against hackers, WIFI admins and ISP or other agencies which have the capability to intercept our network traffic, compromising personal privacy.
<br />

<h1>Languages and Utilities Used</h1>
- <b>Linux Command Line Interface</b> 

<h1>Environments Used </h1>

- <b>Azure Cloud</b>

<h1>Initial Threats analysis</h1>
<br>
<br>
<h2>Configuring Bettercap</h2>
<p>On our Kali Linux machine, connect to the open wifi network (or any wifi you're allowed to sniff) using a bridges connection in your VM.</p><<br>
<p>Identify which interface you connect to the wifi (normally eth0):</p>

```scss
ifconfig
```

<br>
<p>Then using wlan0 as where to operate bettercap on</p>

```scss
sudo bettercao -iface eth0
```
<p>First using <b>net.probe on</b> to scan for all endpoints in the network and list it out using <b>net.show</b></p>
<br>
<img width="862" height="169" alt="image" src="https://github.com/user-attachments/assets/d663d55d-4f9b-44a4-94c9-cb95e364bd8a" />



