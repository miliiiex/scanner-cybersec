# Network Vulnerability Scanner

Outil d'audit et de reconnaissance réseau automatisé développé en Python, conçu pour cartographier un réseau local, identifier les services exposés et détecter les vulnérabilités connues.

## Fonctionnalités

- **Découverte d'hôtes :** Identification des machines actives sur un réseau local.
- **Scan de ports TCP :** Analyse rapide et optimisée par **multi-threading** pour détecter les ports ouverts.
- **Analyse applicative (Banner Grabbing) :** Extraction des signatures et bannières des services actifs (ex: versions de serveurs FTP, SSH, HTTP).
- **Détection des vulnérabilités (CVE) :** Croisement automatisé des bannières récupérées avec une base de règles locale au format JSON.
- **Scoring de risque :** Évaluation et attribution d'un niveau de criticité par machine auditée.
- **Rapports dynamiques :** Génération automatique de rapports d'audit clairs et visuels en HTML.

## Architecture du Projet

Voici la structure modulaire du projet, alignée avec les bonnes pratiques de développement Python :

```text
scanner-cybersec/
├── modules/
│   ├── host_discovery.py    # Algorithmes de découverte des hôtes actifs
│   ├── port_scanner.py      # Scanner de ports TCP multi-threadé
│   ├── vuln_checker.py      # Moteur d'analyse et de correspondance CVE
│   └── report_generator.py  # Générateur de rapports dynamiques en HTML
├── rules/
│   └── vulnerabilities.json # Base de signatures et règles de vulnérabilités
├── .gitignore
├── README.md
├── requirements.txt         # Dépendances du projet
└── scanner.py               # Point d'entrée principal de l'application
