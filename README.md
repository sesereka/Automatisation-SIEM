# Automatisation-SIEM

## Introduction

Ce projet vise à automatiser la détection, l’analyse et la réponse aux menaces en utilisant Wazuh, Shuffle et TheHive. L’objectif est de mettre en place un SIEM capable de traiter les événements de sécurité de manière efficace, avec des actions de réponse automatisées.

Le SIEM suit le flux de traitement suivant :

1. **Windows 10** envoie des événements au **Wazuh Manager**.
2. **Wazuh Manager** déclenche des alertes et exécute des actions de réponse.
3. **Shuffle** reçoit les alertes de Wazuh et exécute différentes actions :
   - Enrichissement OSINT des IOCs.
   - Création d'alertes dans TheHive pour la gestion des incidents.
   - Envoi d'emails et exécution d’actions de remédiation.

Un document détaillant l'architecture du SIEM est disponible dans ce dépôt.

## Documentation du projet

Le projet est accompagné d’une documentation complète comprenant :

- **[Rapport de configuration]** : Explication détaillée des configurations appliquées.
- **[Schéma d'architecture]** : Diagramme détaillant le fonctionnement et les flux du SIEM.
- **[Manuel d’utilisation]** : Explication de l’utilisation du SIEM et des scénarios de tests.
- 
## Architecture

### Flux de traitement

- Windows 10 → Wazuh Manager (analyse et détection d’anomalies).
- Wazuh Manager → Shuffle (envoi des alertes).
- Shuffle → Enrichissement OSINT des IOCs.
- Shuffle → Création d’alertes dans TheHive pour la gestion des incidents.
- Shuffle → Envoi d’emails et exécution de réponses automatisées.

### Technologies utilisées

- **Wazuh** : Surveillance des événements et détection des menaces.
- **Shuffle** : Automatisation des workflows de réponse.
- **TheHive** : Gestion des incidents de cybersécurité.
- **OSINT APIs** : Enrichissement des indicateurs de compromission.
- **Docker / Machines virtuelles** : Environnement de déploiement.

