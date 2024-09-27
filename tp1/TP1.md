1) Récolte d'informations

    🌞 Adresses IP de ta machine


PS C:\Users\felix> ipconfig

Carte réseau sans fil Wi-Fi :

   Suffixe DNS propre à la connexion. . . :
   Adresse IPv6 de liaison locale. . . . .: fe80::fe38:80f6:e38e:fcd2%18
   Adresse IPv4. . . . . . . . . . . . . .: 10.33.75.249
   Masque de sous-réseau. . . . . . . . . : 255.255.240.0
   Passerelle par défaut. . . . . . . . . : 10.33.79.254



PS C:\Users\felix> ipconfig /all

Carte Ethernet Ethernet 2 :

   Suffixe DNS propre à la connexion. . . :
   Description. . . . . . . . . . . . . . : VirtualBox Host-Only Ethernet Adapter
   Adresse physique . . . . . . . . . . . : 0A-00-27-00-00-07
   DHCP activé. . . . . . . . . . . . . . : Non
   Configuration automatique activée. . . : Oui
   Adresse IPv6 de liaison locale. . . . .: fe80::2928:d75e:bfbb:302a%7(préféré)
   Adresse IPv4. . . . . . . . . . . . . .: 192.168.56.1(préféré)
   Masque de sous-réseau. . . . . . . . . : 255.255.255.0
   Passerelle par défaut. . . . . . . . . :
   IAID DHCPv6 . . . . . . . . . . . : 587857959
   DUID de client DHCPv6. . . . . . . . : 00-01-00-01-2E-1F-FA-B3-00-EE-BC-DB-8B-B1
   NetBIOS sur Tcpip. . . . . . . . . . . : Activé


    🌞 **Si t'as un accès internet normal, d'autres infos sont forcément dispos...**


   PS C:\Users\felix> ipconfig /all

   Carte réseau sans fil Wi-Fi :

   Suffixe DNS propre à la connexion. . . :
   Description. . . . . . . . . . . . . . : Intel(R) Wi-Fi 6E AX211 160MHz
   Adresse physique . . . . . . . . . . . : 64-32-A8-E1-14-B4
   DHCP activé. . . . . . . . . . . . . . : Oui
   Configuration automatique activée. . . : Oui
   Adresse IPv6 de liaison locale. . . . .: fe80::fe38:80f6:e38e:fcd2%18(préféré)
   Adresse IPv4. . . . . . . . . . . . . .: 10.33.75.249(préféré)
   Masque de sous-réseau. . . . . . . . . : 255.255.240.0
   Bail obtenu. . . . . . . . . . . . . . : vendredi 27 septembre 2024 09:01:48
   Bail expirant. . . . . . . . . . . . . : samedi 28 septembre 2024 09:01:49
   Passerelle par défaut. . . . . . . . . : 10.33.79.254
   Serveur DHCP . . . . . . . . . . . . . : 10.33.79.254
   IAID DHCPv6 . . . . . . . . . . . : 174338728
   DUID de client DHCPv6. . . . . . . . : 00-01-00-01-2E-1F-FA-B3-00-EE-BC-DB-8B-B1
   Serveurs DNS. . .  . . . . . . . . . . : 8.8.8.8
                                       1.1.1.1
   NetBIOS sur Tcpip. . . . . . . . . . . : Activé


    🌟 BONUS : Détermine s'il y a un pare-feu actif sur ta machine


   Get-NetFirewallProfile

Name                            : Domain
Enabled                         : True
DefaultInboundAction            : NotConfigured
DefaultOutboundAction           : NotConfigured
AllowInboundRules               : NotConfigured
AllowLocalFirewallRules         : NotConfigured
AllowLocalIPsecRules            : NotConfigured
AllowUserApps                   : NotConfigured
AllowUserPorts                  : NotConfigured
AllowUnicastResponseToMulticast : NotConfigured
NotifyOnListen                  : True
EnableStealthModeForIPsec       : NotConfigured
LogFileName                     : %systemroot%\system32\LogFiles\Firewall\pfirewall.log
LogMaxSizeKilobytes             : 4096
LogAllowed                      : False
LogBlocked                      : False
LogIgnored                      : NotConfigured
DisabledInterfaceAliases        : {NotConfigured}

2) Utiliser le réseau


    🌞 Envoie un ping vers...


PS C:\Users\felix> ping 10.33.75.249

Envoi d’une requête 'Ping'  10.33.75.249 avec 32 octets de données :
Réponse de 10.33.75.249 : octets=32 temps<1ms TTL=128
Réponse de 10.33.75.249 : octets=32 temps<1ms TTL=128
Réponse de 10.33.75.249 : octets=32 temps<1ms TTL=128
Réponse de 10.33.75.249 : octets=32 temps<1ms TTL=128

Statistiques Ping pour 10.33.75.249:
    Paquets : envoyés = 4, reçus = 4, perdus = 0 (perte 0%),
Durée approximative des boucles en millisecondes :
    Minimum = 0ms, Maximum = 0ms, Moyenne = 0ms


PS C:\Users\felix> 127.0.0.1

Envoi d’une requête 'Ping'  127.0.0.1 avec 32 octets de données :
Réponse de 127.0.0.1 : octets=32 temps<1ms TTL=128
Réponse de 127.0.0.1 : octets=32 temps<1ms TTL=128
Réponse de 127.0.0.1 : octets=32 temps<1ms TTL=128
Réponse de 127.0.0.1 : octets=32 temps<1ms TTL=128

Statistiques Ping pour 127.0.0.1:
    Paquets : envoyés = 4, reçus = 4, perdus = 0 (perte 0%),
Durée approximative des boucles en millisecondes :


    🌞 On continue avec ping. Envoie un ping vers... ta passerelle


PS C:\Users\felix> ping 10.33.79.254

Envoi d’une requête 'Ping'  10.33.79.254 avec 32 octets de données :
Délai d’attente de la demande dépassé.
Délai d’attente de la demande dépassé.
Délai d’attente de la demande dépassé.
Délai d’attente de la demande dépassé.

Statistiques Ping pour 10.33.79.254:
    Paquets : envoyés = 4, reçus = 0, perdus = 4 (perte 100%),

un(e) pote sur le réseau

PS C:\Users\felix> ping 10.33.66.78

Envoi d’une requête 'Ping'  10.33.66.78 avec 32 octets de données :
Réponse de 10.33.66.78 : octets=32 temps=9 ms TTL=64
Réponse de 10.33.66.78 : octets=32 temps=15 ms TTL=64
Réponse de 10.33.66.78 : octets=32 temps=16 ms TTL=64
Réponse de 10.33.66.78 : octets=32 temps=64 ms TTL=64

Statistiques Ping pour 10.33.66.78:
    Paquets : envoyés = 4, reçus = 4, perdus = 0 (perte 0%),
Durée approximative des boucles en millisecondes :
    Minimum = 9ms, Maximum = 64ms, Moyenne = 26ms

un site internet

PS C:\Users\felix> ping google.com

Envoi d’une requête 'ping' sur google.com [142.250.178.142] avec 32 octets de données :
Réponse de 142.250.178.142 : octets=32 temps=18 ms TTL=117
Réponse de 142.250.178.142 : octets=32 temps=30 ms TTL=117
Réponse de 142.250.178.142 : octets=32 temps=23 ms TTL=117
Réponse de 142.250.178.142 : octets=32 temps=27 ms TTL=117

Statistiques Ping pour 142.250.178.142:
    Paquets : envoyés = 4, reçus = 4, perdus = 0 (perte 0%),
Durée approximative des boucles en millisecondes :
    Minimum = 18ms, Maximum = 30ms, Moyenne = 24ms


    🌞 Faire une requête DNS à la main


PS C:\Users\felix> nslookup
Serveur par dÚfaut :   dns.google
Address:  8.8.8.8

> www.thinkerview.com
Serveur :   dns.google
Address:  8.8.8.8

Réponse ne faisant pas autorité :
Nom :    www.thinkerview.com
Addresses:  2a06:98c1:3120::7
          2a06:98c1:3121::7
          188.114.96.7
          188.114.97.7


> www.wikileaks.org
Serveur :   dns.google
Address:  8.8.8.8

Réponse ne faisant pas autorité :
Nom :    wikileaks.org
Addresses:  80.81.248.21
          51.159.197.136
Aliases:  www.wikileaks.org


> www.torproject.org
Serveur :   dns.google
Address:  8.8.8.8

Réponse ne faisant pas autorité :
Nom :    www.torproject.org
Addresses:  2a01:4f8:fff0:4f:266:37ff:fe2c:5d19
          2620:7:6002:0:466:39ff:fe32:e3dd
          2620:7:6002:0:466:39ff:fe7f:1826
          2a01:4f9:c010:19eb::1
          2a01:4f8:fff0:4f:266:37ff:feae:3bbc
          116.202.120.166
          204.8.99.146
          95.216.163.36
          116.202.120.165
          204.8.99.144


3) Sniffer le réseau

4) Network scanning et adresses IP


    🌞 Effectue un scan du réseau auquel tu es connecté


PS C:\Users\felix> nmap.exe -sn -PR  10.33.64.0/20

Nmap scan report for 10.33.66.78
Host is up (0.0060s latency).
MAC Address: E4:B3:18:48:36:68 (Intel Corporate)
Nmap scan report for 10.33.67.113
Host is up (0.087s latency).
MAC Address: D2:91:DE:DF:9A:6E (Unknown)
Nmap scan report for 10.33.69.68
Host is up (0.28s latency).
MAC Address: EE:E8:D9:89:3F:F1 (Unknown)
Nmap scan report for 10.33.69.89
Host is up (0.52s latency).
MAC Address: AC:C9:06:10:14:B6 (Apple)
Nmap scan report for 10.33.69.90
Host is up (0.045s latency).
MAC Address: 60:E9:AA:DD:EE:4D (Cloud Network Technology Singapore PTE.)
Nmap scan report for 10.33.69.92
Host is up (0.39s latency).
MAC Address: D2:8A:D4:B4:A0:6E (Unknown)
Nmap scan report for 10.33.69.96
Host is up (0.12s latency).
MAC Address: 3E:59:E5:D6:30:1F (Unknown)
Nmap scan report for 10.33.69.102
Host is up (0.35s latency).
MAC Address: F6:F2:C4:53:28:F5 (Unknown)
Nmap scan report for 10.33.69.124
Host is up (0.85s latency).
MAC Address: CC:08:FA:83:C8:7B (Apple)

[...] 
Nmap done: 4096 IP addresses (539 hosts up) scanned in 153.19 seconds


    🌞 Changer d'adresse IP


PS C:\Users\felix> ipconfig

Carte réseau sans fil Wi-Fi :

   Suffixe DNS propre à la connexion. . . :
   Adresse IPv6 de liaison locale. . . . .: fe80::fe38:80f6:e38e:fcd2%18
   Adresse IPv4. . . . . . . . . . . . . .: 10.33.79.235
   Masque de sous-réseau. . . . . . . . . : 255.255.240.0
   Passerelle par défaut. . . . . . . . . : 10.33.79.254