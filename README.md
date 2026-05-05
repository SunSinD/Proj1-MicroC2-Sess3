<a id="readme-top"></a>

[![Licence Unlicense][license-shield]][license-url]

<br />
<div align="center">
  <img src="https://i.imgur.com/Eqy6dM9.png" alt="Projet 1" width="600" height="800">

  <h1 align="center">Projet 1 - Testeur d'interface matrice</h1>

  <p align="center">
    Projet d'école pour le cours <strong>243-33A-MO : Microcontrôleur 2</strong><br />
    Réalisé avec PlatformIO, Arduino et C++.
  </p>
</div>

## Description

![Collège Montmorency][product-screenshot]

Ce dépôt contient mon premier projet pour le cours de Microcontrôleur 2. Le but du programme est de tester une interface matrice avec un Arduino Mega 2560 et une matrice RGB 64x32.

Le programme lit les entrées de la carte, affiche les valeurs sur la matrice et envoie aussi des informations dans le moniteur série. Il sert surtout à vérifier que les boutons, l'encodeur, les entrées analogiques, les DEL RGB et la matrice fonctionnent correctement.

## Fonctionnalités

- Affichage des valeurs du potentiomètre, de la photorésistance et de l'encodeur.
- Affichage de l'état des boutons haut, bas, gauche, droite, A, B et C.
- Lecture de l'encodeur avec une interruption.
- Test des DEL RGB avec les boutons A, B et C.
- Messages dans le port série quand un bouton est appuyé.
- Modes d'animation sur la matrice :
  - `Gauche + Bas + B` active ou désactive l'animation de couleurs.
  - `Haut + Bas + C` active ou désactive l'animation personnalisée.

## Fait avec

- [![C++][cpp-shield]][cpp-url]
- Arduino Mega 2560
- PlatformIO
- Arduino Framework
- MOMO RGB Matrix

## Structure du projet

```text
.
|-- platformio.ini          # Configuration PlatformIO
|-- src/main.cpp            # Code principal
|-- src/bits_manip.cpp      # Fonctions pour manipuler les bits
|-- include/bits_manip.h    # Déclarations des fonctions
|-- lib/MOMO_RGB_Matrix/    # Librairie de la matrice RGB
`-- README.md
```

## Compilation

Pour compiler le projet avec PlatformIO :

```bash
pio run
```

Pour téléverser le programme sur l'Arduino Mega 2560 :

```bash
pio run -t upload
```

Pour ouvrir le moniteur série :

```bash
pio device monitor
```

## Note

Ce projet a été fait pour un travail scolaire. Le README a été écrit pour décrire mon dépôt et mon programme, au lieu de simplement copier le texte du document de l'enseignant.

## Licence

Distribué sous licence Unlicense. Voir [LICENSE](LICENSE) pour plus d'informations.

<p align="right">(<a href="#readme-top">Retour en haut</a>)</p>

[product-screenshot]: https://www.collegesinstitutes.ca/wp-content/uploads/2022/10/montmorency.png
[cpp-shield]: https://img.shields.io/badge/C++-00599C?style=flat-square&logo=C%2B%2B&logoColor=white
[cpp-url]: https://isocpp.org/
[license-shield]: https://img.shields.io/github/license/SunSinD/Proj1-MicroC2-Sess3?style=for-the-badge
[license-url]: LICENSE
