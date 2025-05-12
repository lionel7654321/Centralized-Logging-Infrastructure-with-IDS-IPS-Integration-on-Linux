# Centralized-Logging-Infrastructure-with-IDS-IPS-Integration-on-Linux
🎯 Objectif
Ce projet met en place une infrastructure complète de journalisation composée de plusieurs machines virtuelles sous Linux, configurées pour centraliser les journaux systèmes et web, surveiller l’activité réseau, et implémenter une politique de sécurité automatisée avec Fail2Ban.

🧰 Étapes principales
1. Mise en place de l’infrastructure
Création de 3 à 4 machines virtuelles : Serversyslog, Clientsyslog, Testeursyslog/Testeusesyslog

Configuration réseau en NAT

Vérification de la connectivité (ping)

Installation de services sur Clientsyslog : SSH et Apache2

2. Journalisation centralisée
Suppression des règles de pare-feu existantes

Interception du trafic syslog lors de connexions SSH (succès et échecs)

Configuration de Rsyslog sur Serversyslog pour n'accepter que les logs de Clientsyslog

Redirection des logs web Apache depuis Clientsyslog vers Serversyslog

3. Détection et prévention d’intrusions (IDS/IPS)
Installation et configuration de Fail2Ban sur Clientsyslog

Mise en œuvre d'une politique de blocage automatique après 2 échecs de connexion SSH

Analyse du comportement avec et sans les règles du pare-feu actives

🇬🇧 Project Overview (English)
🎯 Objective
This project involves building a complete centralized logging infrastructure using multiple Linux-based virtual machines. It includes log aggregation, network activity monitoring, and automated security enforcement with Fail2Ban.

🧰 Key Steps
1. Infrastructure setup
Creation of 3 to 4 VMs: Serversyslog, Clientsyslog, Testeursyslog/Testeusesyslog

NAT-based networking and connectivity verification via ping

Installation of key services on Clientsyslog: SSH and Apache2

2. Logging and monitoring
Removal of existing firewall rules

Capturing syslog traffic during successful and failed SSH login attempts

Rsyslog configuration on Serversyslog to accept logs only from Clientsyslog

Redirecting Apache web server logs from Clientsyslog to Serversyslog

3. Intrusion detection and prevention (IDS/IPS)
Installing and configuring Fail2Ban on Clientsyslog

Implementing a policy to block IPs after 2 failed SSH logins

Testing the behavior with firewall rules enabled and disabled
