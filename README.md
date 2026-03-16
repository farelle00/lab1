# lab1

Ce fichier contient la configuration complète du mini-lab réseau réalisé sous Cisco Packet Tracer.  
L’objectif est de mettre en place un réseau multi‑VLAN avec routage inter‑VLAN, DHCP centralisé, NAT pour l’accès Internet et segmentation par usage.

Objectifs du projet

- Configurer 4 VLANs (VoIP, WiFi, PC fixes, Administration)
- Mettre en place un routage inter‑VLAN via un routeur Cisco 1941
- Configurer un serveur DHCP sur le routeur
- Activer l’accès Internet via NAT Overload
- Configurer 3 switchs avec ports access et trunks
- Tester la connectivité entre VLANs et vers Internet

Topologie du réseau

- 1 routeur Cisco 2911
- 3 switchs 2960
- 3 points d’accès WiFi
- 3 PC portables
- 6 PC fixes
- 3 téléphones IP Cisco 7960

VLANs et plan d’adressage

 VLAN    Usage           Réseau            Passerelle         DHCP 

 1      VoIP            192.168.0.0/24      192.168.0.1   192.168.0.10–50 
 10     WiFi            192.168.10.0/24     192.168.10.1  192.168.10.10–50 
 20     PC fixes  1     192.168.20.0/24     192.168.20.1  192.168.20.10–50 
 30     Administration  192.168.30.0/24     192.168.30.1  192.168.30.10–50 

Processus de configuration

 Création des VLANs sur les switchs
VLAN 1 : VoIP  
VLAN 10 : WiFi  
VLAN 20 : PC fixes  
VLAN 30 : Administration

Configuration des ports
Ports 2–3 : VLAN 1  
Ports 4–5 : VLAN 10  
Ports 6–7 : VLAN 20  
Port 8 : VLAN 30  
Ports 1 et 9 : Trunk

onfiguration du routeur
Sous‑interfaces g0/0.x pour chaque VLAN  
DHCP pour chaque réseau  
NAT Overload pour l’accès Internet

Tests
Ping inter‑VLAN  
Ping Internet  
Vérification DHCP

