# 📺 ESPHome Advanced Media & Smart Dashboard (CYD 2-USB)

> **🌐 English version available below** / Version française juste ici.

---

## 🇫🇷 Version Française

Bienvenue dans ce projet de panneau de contrôle domotique ultra-optimisé pour le **CYD (Cheap Yellow Display)**, modèle **ESP32-2432S028R** (version révisée avec 2 ports USB : Micro-USB et USB-C). 

Ce projet pousse ESPHome et la bibliothèque graphique **LVGL** dans leurs derniers retranchements avec une configuration robuste de **plus de 3 600 lignes de code**, entièrement nettoyée, compressée et exempte de lignes superflues pour garantir une compilation stable sur ESP32.

![Interface Principale](batterie-look%20%284%29.jpg)

### ✨ Caractéristiques principales

- **Gestion Multimédia Avancée :** Intégration complète avec les lecteurs de médias de Home Assistant (idéal pour *Music Assistant*).
- **Navigation Fluide :** Menu tactile à onglets permettant de basculer instantanément entre le lecteur principal et la sélection des listes de lecture personnalisées.
- **Contrôle Précis :** Curseurs (*sliders*) de volume synchronisés en temps réel et boutons tactiles parfaitement dimensionnés pour l'écran résistif de 2.8".
- **Optimisation du Code :** Architecture YAML conçue pour l'efficacité, évitant les surcharges de mémoire au moment de la compilation C++ en ligne de commande.

### 🛠️ Le Hardware / Astuce DIY d'Ergonomie

L'un des points forts de ce montage est son ergonomie physique et sa polyvalence. En fixant un bloc batterie externe **INIU de format poche (5000mAh avec chargeur Apple Watch intégré)** directement dos à dos sur la partie supérieure arrière du CYD, l'appareil se transforme en véritable station de bureau :
1. Un excellent lestage pour une tenue stable sur un bureau sans support supplémentaire.
2. Un angle d'inclinaison parfait pour la lecture et l'utilisation du stylet.
3. Un d'égagement optimal au bas du boîtier permettant de laisser le **chargeur magnétique de montre de la batterie INIU entièrement accessible**, transformant le tout en station de recharge bonus.
4. L'utilisation d'un connecteur USB-C en "coude" pour relier le câble intégré proprement.

| Vue de Profil | Détails du Montage Arrière |
| :---: | :---: |
| ![Vue Profil Inclinaison](batterie-look%20%283%29.jpg) | ![Montage Batterie Arrière](batterie-look%20%281%29.jpg) |

### 📸 Galerie des Widgets et Interfaces

Voici un aperçu des différents menus et widgets développés pour optimiser l'espace de l'écran 2.8" :

| Météo & Statuts | Contrôles Domotiques | Sélection Listes | Menu Playlists |
| :---: | :---: | :---: | :---: |
| ![Widget 1](passe-partout%20%281%29.jpg) | ![Widget 2](passe-partout%20%282%29.jpg) | ![Widget 3](passe-partout%20%283%29.jpg) | ![Menu Playlists](batterie-look%20%285%29.jpg) |

*(Aperçu global de l'intégration arrière et des composants)*
| Intégration des composants | Vue complémentaire widget |
| :---: | :---: |
| ![Détails arrière](batterie-look%20%287%29.jpg) | ![Widget 4](passe-partout%20%284%29.jpg) |

### 🖼️ Nouveaux Menus, Cadre Photo & Solution Wi-Fi

L'interface s'est récemment enrichie d'une matrice d'onglets réorganisée pour accueillir de nouvelles fonctionnalités majeures, incluant un panneau de gestion système et un mode cadre numérique interactif.

| Menu Principal (Matrice) | Mode Diaporama (En construction) | Page de Configuration Terminée |
| :---: | :---: | :---: |
| ![Menu Principal Actuel](config-diapo%20%281%29.jpg) | ![Mode Cadre Numérique](config-diapo%20%282%29.jpg) | ![Page de Configuration](config-diapo%20%283%29.jpg) |

#### ⚙️ Page « Configuration » (Complétée)
Ce panneau technique permet un contrôle complet du comportement de l'appareil en local :
- **Gestion de la veille :** Réglage dynamique du délai d'extinction de l'écran (avec affichage du statut actif/inactif et boutons `+` / `-`).
- **Bouton de Redémarrage (Solution Wi-Fi Zombie) :** Les microcontrôleurs gèrent difficilement le *roaming* automatique (itinérance) entre des routeurs d'architectures différentes (comme une borne principale Bell Giga Hub et un routeur secondaire TP-Link Archer). L'ESP32 pouvant rester accroché à un signal fantôme ou être rejeté par le protocole agressif de routage, l'intégration d'un bouton matériel `Redémarrage` (via la plateforme native `restart` d'ESPHome) offre un contournement logiciel parfait. Un simple clic relance l'appareil en moins de 2 secondes pour qu'il s'associe instantanément à la borne la plus proche, évitant ainsi d'avoir à manipuler physiquement les câbles d'alimentation.
- **Rétroaction audio :** Bouton de test du haut-parleur interne et indicateur d'état des bips système (`ACTIF` / `MUET`).
- **Contrôle de la LED RVB arrière :** Boutons d'activation directe des couleurs (`Bleu`, `Vert`, `Rouge`) ou extinction complète (`OFF`).
- **Diagnostics Réseau en Temps Réel :** Affichage en direct du nom d'hôte local (`.local`), de l'heure système précise et de la force réelle du signal Wi-Fi mesurée en `dBm`.

#### 🖼️ Projet « Diaporama » (En développement)
L'onglet **Diaporama** pose les bases d'un mode cadre photo numérique. Ce module est conçu pour afficher des grilles d'images et des photos de paysages récupérées de manière automatisée. Le déploiement à venir prévoit l'utilisation d'un script Python externe chargé de traiter, redimensionner en lot et sérialiser les images locales afin qu'elles soient parfaitement adaptées à la mémoire et à la résolution native de l'écran du CYD.

### 🗂️ Structure du Répertoire

- `passe-partout.yaml` : Le fichier de configuration principal ESPHome (3600+ lignes).
- `secrets.yaml` *(Non inclus)* : À créer chez vous pour vos accès Wi-Fi et clés d'API.

---

## 🇺🇸 English Version

Welcome to this ultra-optimized smart home control panel project for the **CYD (Cheap Yellow Display)**, model **ESP32-2432S028R** (revised version featuring 2 USB ports: Micro-USB and USB-C).

This project pushes ESPHome and the **LVGL** graphics library to their absolute limits with a robust configuration of **over 3,600 lines of code**, fully cleaned, compressed, and free of unnecessary lines to ensure stable compilation and flashing via command line (PowerShell).

### ✨ Key Features

- **Advanced Media Management:** Full integration with Home Assistant media players (perfectly tailored for *Music Assistant*).
- **Smooth Navigation:** A tabbed touch menu allowing instant switching between the main player and custom playlist selections.
- **Precise Control:** Real-time synchronized volume sliders and touch buttons perfectly sized for the 2.8" resistive screen.
- **Code Optimization:** YAML architecture engineered for efficiency, preventing memory overhead during C++ compilation.

### 🛠️ Hardware & Ergonomics DIY Hack

A major highlight of this build is its physical design and versatility. By attaching a **pocket-sized INIU power bank (5000mAh with a built-in Apple Watch charger)** back-to-back on the upper rear section of the CYD, the device transforms into a clever desktop docking station:
1. Excellent weight distribution for rock-solid stability on a desk without needing an extra stand.
2. Perfect viewing and stylus angle.
3. Great clearance at the bottom, keeping the **INIU's integrated magnetic smartwatch charger fully accessible** for bonus charging utility.
4. Uses a right-angle USB-C connector to route the built-in cable cleanly.

### 📸 Widgets & UI Gallery

Here is a look at the various menus and widgets designed to make the most out of the 2.8" display:

| Weather & Status | Smart Home Controls | List Selection | Playlist Menu |
| :---: | :---: | :---: | :---: |
| ![Widget 1](passe-partout%20%281%29.jpg) | ![Widget 2](passe-partout%20%282%29.jpg) | ![Widget 3](passe-partout%20%283%29.jpg) | ![Playlist Menu](batterie-look%20%285%29.jpg) |

| Hardware Layout | Custom Widget View |
| :---: | :---: |
| ![Rear Details](batterie-look%20%287%29.jpg) | ![Widget 4](passe-partout%20%284%29.jpg) |

### 🖼️ New Menus, Photo Frame & Wi-Fi Workaround

The main interface has been upgraded with a new grid-based tab layout to accommodate advanced system monitoring controls and an upcoming interactive media frame.

| Main Matrix Menu | Slideshow Mode (WIP) | Completed Settings Page |
| :---: | :---: | :---: |
| ![Main Menu Matrix](config-diapo%20%281%29.jpg) | ![Digital Photo Frame](config-diapo%20%282%29.jpg) | ![Configuration Page](config-diapo%20%283%29.jpg) |

#### ⚙️ "Configuration" Page (Completed)
This newly deployed technical panel gives full local control over hardware behavior:
- **Display Timeout Handling:** Dynamically adjust the screen sleep timeout delay using dedicated `+` and `-` buttons (complete with On/Off status visualization).
- **Reboot Button (Wi-Fi Zombie Fix):** Microcontrollers often struggle with seamless *roaming* between distinct router brands (e.g., a primary ISP Bell Giga Hub and a secondary TP-Link Archer access point). The ESP32 can get trapped in "zombie connection" loops or rejected by aggressive band-steering protocols. Integrating a software `Redémarrage` (Reboot) button via ESPHome's native `restart` platform offers an elegant solution. A single tap safely reboots the CYD in less than 2 seconds, forcing it to immediately hook into the nearest available router without needing to manually unplug power cords.
- **Audio Diagnostics:** Instant internal speaker testing trigger and system buzzer state modifier (`ACTIVE` / `MUTED`).
- **Rear RGB LED Controller:** Directly override and trigger custom back-lighting colors (`Blue`, `Green`, `Red`) or turn it completely `OFF`.
- **Live Infrastructure Telemetry:** Monitors and prints local mDNS hostname (`.local`), precise system clock sync, and real-time Wi-Fi signal strength values measured in `dBm`.

#### 🖼️ "Diaporama" Slideshow Project (Work in Progress)
The **Diaporama** tab serves as the interface foundation for a custom digital picture frame. The feature is being built to showcase automated photo grids and landscapes. Future updates will introduce an automated external Python script optimized to process, batch-resize, and serialize local image folders so they match the hardware limitations and native layout resolution of the CYD display.

### 🚀 Quick Start

1. Create a dedicated folder for this project in your ESPHome directory.
2. Drop the provided `passe-partout.yaml` configuration file into it, adjusting it to match your Home Assistant entity names.
3. Create your own `secrets.yaml` file with your Wi-Fi credentials and API keys.
4. Flash your CYD using your PowerShell terminal environment (`esphome run your_file.yaml`) and enjoy!

---
*Developed with passion by a smart home enthusiast for the open-source community.*
