# 🎨 TexLoader CXFR

Mod de remplacement de textures stable pour CarX Drift Racing Online.

---
![animiertes-gif-von-online-umwandeln-de_2](https://github.com/user-attachments/assets/4204ad0a-caf2-4647-b850-3662a6c00588)

## 🚀 Nouveautés de la version 2.2.2 (Stable & 3D POM Update)

Cette nouvelle version apporte non seulement une refonte totale de la stabilité et de la mémoire, mais introduit surtout **le support des textures de hauteur (Height Maps)** pour un rendu 3D ultra-réaliste inédit dans le jeu de base !

### ✨ Nouvelles Fonctionnalités
* **Support du Relief 3D (Parallax Occlusion Mapping) :** La version 2.2.2 ajoute le support des textures de hauteur (`_height.png`), une fonctionnalité non disponible de base dans le jeu. Cela permet de donner un véritable effet de volume et de profondeur aux routes et murs.
* **Génération Automatique :** Si vous ne fournissez pas de textures personnalisées pour le relief ou les reflets, le jeu gardera automatiquement ses textures `_normal` et `_pack` d'origine.

### 🛠️ Optimisations et Corrections (Stable Mode)
* **VRAM et Mémoire optimisées :** Les anciennes textures sont désormais proprement nettoyées de la carte graphique lors d'un changement de pack.
* **Restauration "Default" parfaite :** Le retour aux textures d'origine du jeu se fait désormais sans aucun bug ou résidu des packs précédents.
* **Protection des maps système :** Le mod bloque intelligemment les sauvegardes dans les menus du jeu ou le garage pour éviter de corrompre vos fichiers.

### 🖥️ Interface (UI)
* L'interface (toujours accessible via `Ctrl + P`) fait peau neuve avec un thème "Soft Dark" plus lisible.
* Ajout de la ligne **"Pack :"** dans le menu de statut pour voir immédiatement quel pack est actif.

---

## 📂 Comment structurer vos Packs de Textures ?

Voici comment nommer vos fichiers pour profiter de toutes les options de la v2.2.2 :

**Exemple de contenu d'un pack :**
* `0x67c863e8_base.png` ➔ ✅ **Requis :** Remplace la texture principale.
* `0x67c863e8_height.png` ➔ ✅ **NOUVEAU / OPTIONNEL :** Active l'effet 3D POM (Relief).
* `0x67c863e8_normal.png` ➔ ✅ **OPTIONNEL :** Remplace la normal map du jeu par la vôtre.
* `0x67c863e8_ao.png` ➔ ✅ **OPTIONNEL :** Ajoute votre propre texture d'Occlusion Ambiante.

> **Note :** Le jeu garde automatiquement les `_normal` et les `_pack` du jeu de base si vous n'en fournissez pas dans votre dossier !

---

## 📥 Installation

1. Téléchargez la dernière version dans l'onglet [Releases](https://github.com/Silv3r25/TexLoader-CXFR/releases).
2. Extrayez le fichier `TexLoaderFix_CXFR.dll`.
3. Placez-le dans le dossier `kino/mods/` de votre jeu.
4. Démarrez le jeu !

---

## 🎮 Contrôles

* `CTRL + P` : Ouvrir/Fermer le Menu
* `SHIFT + 1` : Rechargement rapide des textures

---
*Développé par l'équipe CarX France*
