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
<br>
<h2>ARP Spoofing</h2>
<br>
<p>
ARP spoofing (or ARP poisoning) is a malicious technique where an attacker sends falsified Address Resolution Protocol (ARP) messages over a local area network (LAN). It links the attacker's MAC address with the IP address of a legitimate node (like a default gateway), allowing them to intercept, modify, or block traffic. This is a common form of a Man-in-the-Middle (MitM) attack.
</p>
<br>
<p>In order to set a specific target for our attack, use the following command</p>
<br>

```scss
set arp.spoof.targets < Target IP Address>
set arp.spoof.fullduplex true //both the targets and the gateway will be attacked
arp.spoof on
net.sniff on
```
<br>
<p>Then the target would basically be able to sniff your traffic and intercept every website you visit which lead to worse attacks like DNS spoofing to redirect your traffic to another website hosted on the attacker's machine</p>

---
<h1>Setting up your own VPN with no logs</h1>
<br>
<h2 How VPN works></h2>
<br>
<p>Assuming that you have a typical Internet connection like this</p>
<img width="792" height="216" alt="image" src="https://github.com/user-attachments/assets/ff21a7b4-df02-43f1-8c0c-41e75a0fd5c8" />
<br>
<p>If we send a request to the Internet like when we want to visit a website google.com for example, entities such as hackers, admins, ISP or other agencies are going to be able to intercept  that request, compromising personal privacy.  </p>
<br>
<p>Therefore, in order to prevent this, people often use VPN (Virtual Private Network)</p>
<br>
<img width="784" height="206" alt="image" src="https://github.com/user-attachments/assets/512fa314-9303-4927-8735-5fac710a4533" />
<br>
<p>This way, we would send all of our traffic to this private tunnel first, the VPN would encrypt the traffic  and then it will get directed to the website they are visiting. Thus, it'll provide protection from MITM attack, extra layer of encryption, more privacy and the ability to bypass censorship</p>






