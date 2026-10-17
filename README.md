# StatX

<p align="center">
  <img src="https://cdn.discordapp.com/icons/1540284392365101177/89efbc719cbb81c54beeb661ca895827.webp?size=128" alt="Logo StatX" width="120" height="120">
</p>

<p align="center">
  <a href="https://github.com/votre-compte/StatX-releases/releases"><img src="https://img.shields.io/github/v/release/votre-compte/StatX-releases?style=flat-square&color=blue" alt="GitHub release"></a>
  <a href="https://github.com/votre-compte/StatX-releases/blob/main/LICENSE"><img src="https://img.shields.io/badge/license-MIT-green.svg?style=flat-square" alt="License"></a>
  <img src="https://img.shields.io/badge/platform-Windows%2010%2F11-blueviolet?style=flat-square" alt="Platform">
</p>

**StatX** est une interface de bureau moderne et légère (basée sur Electron) conçue pour surveiller les ressources de votre PC en temps réel : CPU (global et par cœur), mémoire RAM, disques, réseau, GPU et températures.

---

## Fonctionnalités

- **Performances en temps réel** : Surveillance complète du CPU, de la RAM, du stockage, de la bande passante réseau et du GPU.
- **Bibliothèque de jeux unifiée** : Centralise vos jeux installés issus de 9 plateformes (Steam, Epic Games, Xbox/Game Pass, Rockstar, GOG, Battle.net, Ubisoft Connect, EA app, itch.io) avec un accès au lancement direct et au suivi du temps de jeu.
- **Gestionnaire de mises à jour** : Détecte et installe les mises à jour logicielles via `winget`.
- **Programmes au démarrage** : Contrôle total sur les applications lancées au démarrage de Windows (équivalent au Gestionnaire de tâches).
- **Bilan de santé** : Diagnostic automatique de la machine pour identifier les points de vigilance (espace disque critique, températures élevées, fuites mémoire).
- **Outil de nettoyage** : Libération rapide d'espace disque (corbeille, fichiers temporaires, caches de navigateurs et fichiers volumineux du profil utilisateur).

---

## Installation

1. Téléchargez la dernière version de l'installateur (`StatX Setup <version>.exe`) depuis la [page des Releases](https://github.com/votre-compte/StatX-releases/releases).
2. Lancez l'exécutable et suivez les instructions de l'installateur.

> **Avertissement SmartScreen** : L'application n'étant pas signée numériquement pour le moment, Windows Defender SmartScreen peut afficher une alerte (« Windows a protégé votre PC ») au premier lancement. Cliquez sur **Informations complémentaires**, puis sur **Exécuter quand même**.

---

## Prérequis : Températures CPU

Pour permettre à StatX d'afficher les **températures de votre processeur (CPU)**, deux conditions sont nécessaires :

1. **Installer le pilote PawnIO** (requis pour l'accès aux sondes matérielles sous Windows) :
   Ouvrez un terminal (PowerShell ou Invite de commandes) et exécutez la commande suivante :
   ```bash
   winget install namazso.PawnIO
   ```
   Validez l'invite UAC qui s'affiche.

2. **Exécuter l'application en administrateur** :
   Faites un clic droit sur l'icône de StatX et sélectionnez **« Exécuter en tant qu'administrateur »**.

*Si ces conditions ne sont pas remplies, le reste de l'application fonctionnera normalement, mais la section des températures CPU affichera « — ».*

---

## Utilisation

- **Zone de notification (Tray)** : La fermeture de la fenêtre principale (croix ✕) réduit l'application dans la barre des tâches à côté de l'horloge afin de maintenir la surveillance en arrière-plan. Un clic sur l'icône restaure la fenêtre, et un clic droit ouvre le menu contextuel rapide.
- **Intégration Discord** : Option de liaison de compte Discord pour afficher votre profil (avatar et pseudo) dans l'interface.

---

## Dépannage

- **Le pont de capteurs indique "non compilé" ou les températures restent vides** : Assurez-vous que le pilote `PawnIO` est installé et que l'application est bien lancée avec les privilèges administrateur.
- **Mises à jour** : L'application intègre un mécanisme d'auto-update via GitHub. Un message de notification vous préviendra dès qu'une nouvelle version sera disponible.
