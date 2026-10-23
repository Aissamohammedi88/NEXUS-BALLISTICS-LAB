# NEXUS-BALLISTICS-LAB
Simulateur balistique 3D en temps réel (Fusil de précision &amp; Bazooka). 100% local, zéro dépendance cloud. Prototype pour créer et calibrer des armes avant de les scripter sur Roblox. Moteur physique, explosions et recul.
<div align="center">

<!-- Bannière Animée SVG -->
<svg width="800" height="180" viewBox="0 0 800 180" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="bgGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#05050a"/>
      <stop offset="100%" stop-color="#0a0a14"/>
    </linearGradient>
    <linearGradient id="neonGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#ff00c8">
        <animate attributeName="stop-color" values="#ff00c8;#00e5ff;#ff00c8" dur="3s" repeatCount="indefinite"/>
      </stop>
      <stop offset="100%" stop-color="#00e5ff">
        <animate attributeName="stop-color" values="#00e5ff;#ff00c8;#00e5ff" dur="3s" repeatCount="indefinite"/>
      </stop>
    </linearGradient>
  </defs>

  <rect width="800" height="180" fill="url(#bgGrad)" rx="12"/>
  <rect x="1" y="1" width="798" height="178" fill="none" stroke="url(#neonGrad)" stroke-width="2" rx="11" opacity="0.5"/>

  <text x="400" y="80" text-anchor="middle" font-family="ui-monospace, monospace" font-size="36" font-weight="900" fill="url(#neonGrad)">
    NEXUS BALLISTICS LAB
    <animate attributeName="opacity" values="1;0.8;1" dur="2s" repeatCount="indefinite"/>
  </text>
  <text x="400" y="120" text-anchor="middle" font-family="ui-monospace, monospace" font-size="14" fill="#8b9dc3" letter-spacing="4">
    WEAPON PROTOTYPING ENGINE
  </text>
  <text x="400" y="150" text-anchor="middle" font-family="ui-monospace, monospace" font-size="12" fill="#ff00c8" letter-spacing="2">
    ZERO DEPENDENCIES · LOCALHOST ONLY · ROBLOX READY
  </text>
</svg>

<br/>

[![Status](https://img.shields.io/badge/STATUS-OPERATIONAL-00ff88?style=for-the-badge)](#)
[![Port](https://img.shields.io/badge/PORT-1337-ff00c8?style=for-the-badge)](#)
[![Engine](https://img.shields.io/badge/ENGINE-Three.js-00e5ff?style=for-the-badge)](#)
[![License](https://img.shields.io/badge/LICENSE-NEXUS--OPEN--3.0-white?style=for-the-badge)](#)

<br/>

**Un simulateur balistique 3D en temps réel pour prototyper des armes (Fusil de précision & Bazooka).**
**100% Local. 100% Open Source. Prêt à être traduit en scripts Roblox.**

</div>

---

## 🎯 Le Concept

**NEXUS BALLISTICS LAB** n'est pas un simple jeu. C'est un environnement de test pour développeurs et créateurs de jeux (comme sur Roblox). 

Il permet de visualiser et de calibrer en temps réel :
- La **vélocité** des projectiles.
- Le **recul (recoil)** de la caméra.
- Le **raycasting** (détection de collision).
- Les **explosions** avec physique de particules (gravité, dispersion).

Tout tourne dans ton navigateur via une architecture client-side pure (HTML/CSS/JS + Three.js). Aucun serveur distant, aucun cloud. Tu lances le script Bash, et le laboratoire s'ouvre sur `localhost:1337`.

---

## ⚡ Fonctionnalités

| Fonctionnalité | Description |
|----------------|-------------|
| **Arme 1 : Fusil de Précision** | Cadence rapide, projectiles cyan, faible recul, idéal pour le tir de précision. |
| **Arme 2 : Bazooka** | Cadence lente, gros projectiles roses, recul massif, explosion de particules à l'impact. |
| **Moteur Physique** | Gestion des vecteurs de vélocité, de la gravité (sur les explosions) et du raycasting (distance cible-projectile). |
| **Environnement 3D** | Sol texturé, grille néon, éclairage dynamique, et cibles destructibles (sphères rouges). |
| **Switch d'arme** | Touches `1` et `2` pour changer d'arme à la volée. Le modèle 3D de l'arme change instantanément. |
| **Zéro Dépendance** | Le script Bash génère l'interface et lance un serveur HTTP (via `socat` ou `nc`). Pas besoin de Node.js ou Python. |

---

## 🚀 Utilisation

### Prérequis
Le script a besoin d'un serveur HTTP basique. Assure-toi d'avoir `socat` ou `netcat` installé :
```bash
sudo apt install socat # Recommandé
