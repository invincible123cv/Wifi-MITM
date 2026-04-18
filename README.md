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
[ARP spoofing](https://www.google.com/search?q=ARP+spoofing&rlz=1C1FKPE_enVN1170VN1170&oq=what+is+arp+spoofing&gs_lcrp=EgZjaHJvbWUyBggAEEUYOTIHCAEQABiABDIHCAIQABiABDIHCAMQABiABDIHCAQQABiABDIICAUQABgWGB4yCAgGEAAYFhgeMggIBxAAGBYYHjIICAgQABgWGB4yCAgJEAAYFhge0gEINDQ4N2owajeoAgiwAgHxBeNRIDn27A4C&sourceid=chrome&ie=UTF-8&mstk=AUtExfC97F44yJOFPAzNHk6TQjFQPVxxzoTalO6TKBsnZZIJPqKfntvU8iWEH2GZHStagsLsuIt5_FgdeXh5OoUvvLKLEiZaoie047_pUqUm-QLYHGAZnjZsAsYBl_Nn3H6P1Rfy6TwlT7vDDXAbeNY-NI2w7JUVOgUI5W2FHyzzqW8vPB3F8yqOdi5A232b7qsFk3oQV79HWTpe43u2N_txmk_Wpbuv2FdXoBzEB-UQ6b0_MtJ21legVIc51BCKQCXk697QSotxlW8WkIz_A2tsZe3K&csui=3&ved=2ahUKEwjjmfSTiMeSAxVKSGcHHdbhE3kQgK4QegQIARAB) (or ARP poisoning) is a malicious technique where an attacker sends falsified Address Resolution Protocol (ARP) messages over a local area network (LAN). It links the attacker's MAC address with the IP address of a legitimate node (like a default gateway), allowing them to intercept, modify, or block traffic. This is a common form of a [Man-in-the-Middle (MitM) attack](https://www.imperva.com/learn/application-security/arp-spoofing/).
</p>


