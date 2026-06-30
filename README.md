# 📺 ESPHome Advanced Media & Smart Dashboard (CYD 2-USB)

> **🌐 English version available below** / Version française juste ici.

---

## 🇫🇷 Version Française

Bienvenue dans ce projet de panneau de contrôle domotique ultra-optimisé pour le **CYD (Cheap Yellow Display)**, modèle **ESP32-2432S028R** (version révisée avec 2 ports USB : Micro-USB et USB-C). 

Ce projet pousse ESPHome et la bibliothèque graphique **LVGL** dans leurs derniers retranchements avec une configuration robuste de **plus de 3 500 lignes de code**, entièrement nettoyée, compressée et exempte de lignes superflues pour garantir une compilation stable sur ESP32.

![Interface Principale](batterie-look%20%284%29.jpg)

### ✨ Caractéristiques principales

- **Gestion Multimédia Avancée :** Intégration complète avec les lecteurs de médias de Home Assistant (idéal pour *Music Assistant*).
- **Navigation Fluide :** Menu tactile à onglets permettant de basculer instantanément entre le lecteur principal et la sélection des listes de lecture personnalisées.
- **Contrôle Précis :** Curseurs (*sliders*) de volume synchronisés en temps réel et boutons tactiles parfaitement dimensionnés pour l'écran résistif de 2.8".
- **Optimisation du Code :** Architecture YAML conçue pour l'efficacité, évitant les surcharges de mémoire au moment de la compilation C++.

### 🛠️ Le Hardware / Astuce DIY d'Ergonomie

L'un des points forts de ce montage est son ergonomie physique et sa polyvalence. En fixant un bloc batterie externe **INIU de format poche (5000mAh avec chargeur Apple Watch intégré)** directement dos à dos sur la partie supérieure arrière du CYD, l'appareil se transforme en véritable station de bureau :
1. Un excellent lestage pour une tenue stable sur un bureau sans support supplémentaire.
2. Un angle d'inclinaison parfait pour la lecture et l'utilisation du stylet.
3. Un dégagement optimal au bas du boîtier permettant de laisser le **chargeur magnétique de montre de la batterie INIU entièrement accessible**, transformant le tout en station de recharge bonus.
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

### 🗂️ Structure du Répertoire

- `cyd-smart-dashboard.yaml` : Le fichier de configuration principal ESPHome (3100+ lignes).
- `secrets.yaml` *(Non inclus)* : À créer chez vous pour vos accès Wi-Fi et clés d'API.

---

## 🇺🇸 English Version

Welcome to this ultra-optimized smart home control panel project for the **CYD (Cheap Yellow Display)**, model **ESP32-2432S028R** (revised version featuring 2 USB ports: Micro-USB and USB-C).

This project pushes ESPHome and the **LVGL** graphics library to their absolute limits with a robust configuration of **over 3,100 lines of code**, fully cleaned, compressed, and free of unnecessary lines to ensure stable compilation on the ESP32.

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

### 🚀 Quick Start

1. Create a dedicated folder for this project in your ESPHome directory.
2. Drop the provided `.yaml` configuration file into it, adjusting it to match your Home Assistant entity names.
3. Create your own `secrets.yaml` file with your Wi-Fi credentials and API keys.
4. Flash your CYD and enjoy!

---
*Developed with passion by a smart home enthusiast for the open-source community.*
