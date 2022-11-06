# Animation Flipper French Community

![](FrenchCommunityAnimation.gif)

## Intégrer l'animation à votre Flipper

--- 
Référence: [LAB401 academy: Custom animations on your Flipper zero! Everything you need to know.](https://www.youtube.com/watch?v=Nq5DXhOMo5s)
---

1. Récupérer les sources de votre firmwares
2. Intégrer le dossier `assets/dolphin/external/FlipperFrenchCommunity` dans l'arborescence de votre firmware
3. Modifier le fichier `assets/dolphin/external/Manifest.txt` pour y ajouter l'animation (ou copier le Manifest.txt de ce dépot)
4. A la racine du dépot du firmware, lancer la commande
  ```
  ./fbt icons proto dolphin_internal dolphin_ext resources
  ```
5. Copier le dossier `assets/resources/dolphin/FlipperFrenchCommunity` sur la carte sd du Flipper dans le dossier `dolphin` ainsi que le fichier `assets/resources/dolphin/Manifest.txt`

## Modifier et générer l'animation avec Krita

* Cette animation a été créée avec Krita
* Le rendu est de 7 images
* Après avoir fait le rendu, il faut renommer les images dans le format approprié:
  ```
  ls *.png | while read img;do mv $img $(echo $img | sed 's/^.*\([0-9]\{1\}\)/frame_\1/g');done
  ```

