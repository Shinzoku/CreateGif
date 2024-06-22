# GIF Creator

Ce script Python utilise la bibliothèque `imageio` pour créer un GIF à partir d'une série d'images. Ce petit projet est un exercice du site de Codédex.

## Prérequis

Avant d'exécuter ce script, assurez-vous d'avoir installé la bibliothèque `imageio`. Vous pouvez l'installer en utilisant pip :

```bash
pip3 install imageio
```
## Utilisation

Le script lit des fichiers d'image, les combine en une seule animation GIF, et enregistre le résultat dans un fichier team.gif.

## Structure du script

1. #### Importation de la bibliothèque `imageio` :

```python
import imageio.v3 as iio
```
2. #### Définition des chemins des fichiers d'images :

```python
filenames = ['team-pic1.png', 'team-pic2.png']
```
3. #### Initialisation d'une liste pour stocker les images :

```python
images = [ ]
```
4. #### Boucle pour lire les images et les ajouter à la liste images :

```python
for filename in filenames:
    images.append(iio.imread(filename))
```
5. #### Création et enregistrement du GIF :

```python
iio.imwrite('team.gif', images, duration = 500, loop = 0)
```
## Explication des paramètres

+ `'team.gif'` : Le nom du fichier GIF créé.
+ `images` : La liste contenant les données des images lues.
+ `duration = 500` : Durée d'affichage de chaque image dans le GIF, en millisecondes (500 ms = 0.5 seconde).
+ `loop = 0` : Nombre de répétitions du GIF (0 signifie que le GIF se répète indéfiniment).

## Exécution

Pour exécuter le script, assurez-vous que les images (team-pic1.png et team-pic2.png) sont présentes dans le même répertoire que le script Python, puis lancez le script :

```bash
python create_a_gif.py
```
Un fichier nommé team.gif sera généré dans le même répertoire, contenant les images spécifiées.