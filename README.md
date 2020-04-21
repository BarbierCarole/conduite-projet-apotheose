# conduite-projet-apotheose

## 1 - Des exemples d'appli proposant des services similaires

### >>> Appli comme [Moving Planner](https://play.google.com/store/apps/details?id=com.jimbl.movingplanner)
<details>
<summary> Voir les copies d'écran </summary>

<img src="https://lh3.googleusercontent.com/parOJFLgmFa7uzzhkGlLvJjK7lKzYrqDO-WZ6vEwEtKsT2DjTjvOuhMuVS_QqAXPraz_=w967-h916-rw" alt="drawing" width="700"/> <img src="https://lh3.googleusercontent.com/SBzddq7EH4fc7GR0fLUN2zdmwQvPD1R-TLESHoIDxK8IZ-IHdb5CmtYI8FVy1Lfu8vCZ=w967-h916-rw" alt="drawing" width="700"/> <img src="https://lh3.googleusercontent.com/IxoAoi8Ecjc-9VuWvRew5qp20cMUFKes9eF1KhIzw-kKDC8Q1JRw-l_WJiMbIq-RRrAq=w967-h916-rw" alt="drawing" width="700"/> <img src="https://lh3.googleusercontent.com/V3hA0IZhG7L5vgGQ9uB9oVnEyQFNeGmy1mkpYZQoOEcf7QInbSuDy-le2hJ9t5gAUlA=w967-h916-rw" alt="drawing" width="700"/> <img src="https://lh3.googleusercontent.com/WJoyvB0UF590ZmsDb8H1Jh_k5snWMJBRMOC_p3Sai5pwuHYnKg_ptiZFQRJ4SbmDP58=w967-h916-rw" alt="drawing" width="700"/> <img src="https://lh3.googleusercontent.com/MkcSk7NQAK_FbQWH7MA7tPd6gxKhXIQAGUqdRHDEhvXSbPAyQC3pu_wESi0BOY4h5A=w967-h916-rw" alt="drawing" width="700"/>
</details>

#### Ce que j'ai aimé :

- le principe de listes,
- les couleurs des box 
- la checklist check barré
- les options d'affichage 
- la gestion des items
- la simplicité / clarté de l'appli et du design

#### Voir s'il est possible d'ajouter :

"fragile", 
taille du carton: S/M/L

### >>> Appli comme Range-Cartons / I-cartons (apple)
<details>
<summary> Voir les copies d'écran </summary>

<img src="https://www.ateliers14.com/wp-content/uploads/sites/27/2018/08/screenshots-appli-i-cartons.jpg" alt="i-cartons" height="500"/>
<img src="https://www.memoclic.com/medias/var/2015-02/interface-range-cartons.png" alt="i-cartons" wigth="700">
</details>

#### Ce que j'ai aimé :

- les champs : 
  - numéro du carton
  - case à cocher [x] vidé
  - destination (peut etre différent de l'origine dans le cas où les enfants auraient chacun leur chambre ...)
  - origine 
  - contenu possibilité d'y mettre une photo 
  - détail du contenu

- les catégories :
  - pièces
  - contenus
 
#### Voir s'il est possible d'ajouter :

"fragile", 
taille du carton: S/M/L

### >>> Appli comme cool move (dispo gratuit sur android)

  - [Dossier d images](https://drive.google.com/drive/folders/1l67lIkfYDU5baY18oVLCBy7aKRkh4A2f?usp=sharing)



## 2 - User-stories

|En tant que ...| je veux...| pour ...|
|--------|--------|--------|
|    A    |    B    |    B    |
|    C    |    D    |    B    |

## 3 - Maquette

A l'aide d'un wireframe, crayon-papier ...
[https://whimsical.com/wireframes](https://whimsical.com/wireframes)

# Préparation de la BDD

Récap des cours : [https://github.com/O-clock-Alumni/fiches-recap/tree/master/bdd](https://github.com/O-clock-Alumni/fiches-recap/tree/master/bdd)

## 4 - Dictionnaire de données

<details>
<summary>  Qu'est ce qu'un dictionnaire de données  </summary>
A partir des infos disponibles (maquettes, cahier des charges, descriptions fonctionnelles), nous allons **lister toutes les informations nécessaires au fonctionnement** de l'application dans un _dictionnaire de données_, selon cette méthode :

- **Nommer chaque information**, la décrire si besoin.
- **Indiquer son type** (nombre, texte, booléen, calculé à partir d'autres informations).
- Ajouter un commentaire si besoin.

Une fois la liste créée, on doit **la trier** afin de :

- Décomposer les données : **chaque ligne doit contenir une information unique**, indivisible (pas de champ _Adresse_ qui incluerait _Adresse + Ville + Code postal_ par ex.).

Une fois ceci fait nous pouvons **identifier les entités** et y rattacher les données. Selon le contexte cette étape peut même être faite avant l'identification des données.

> Certaines informations ne seront pas rattachées qu'à une seule entité, par ex. le rôle d'un acteur dans un film - entité _Film_ et _Acteur_. Ces informations vont nous aider à construire les relations.

</details>
<details>
<summary>  Exemple  </summary>

de dictionnaire avec des livres

Nom|Description|Type|Commentaire|Entité|
-|-|-|-|-|
Titre|Titre du livre|texte court|-|Livre|
Année|Année de première parution|date|Année sur 4 chiffres|Livre|
Nom|Nom de l'auteur|texte court|-|Auteur|
Prénom|Prénom de l'auteur|texte court|-|Auteur|
Nom|Nom du genre|texte court|-|Genre|

Nous avons identifié 3 entités. Le nom et le prénom de l'auteur ont été décomposés.
</details>


Nom|Description|Type|Commentaire|Entité|
-|-|-|-|-|
...|...|...|...|...|

## MCD
<details>
<summary> Comment définir le Modele Entité-Association ? </summary>

cours : [conception-3](https://github.com/O-clock-Alumni/fiches-recap/blob/master/bdd/conception-03-mcd.md)

Cette modélisation des données permet de représenter de façon rigoureuse un système de données, ou système d'informations, sous forme d'entités et des relations qui les lient.

>A partir des données présentes dans le dictionnaire nous pouvons :
>- **Dessiner nos _entités_**.
>- **Répartir leurs _attributs_** (les données qui les concernent).
>- Définir un attribut qui identifie l'entité de manière unique : >**L'identifiant ou la _clé primaire_**.
>- **Identifier les _relations_** entre les entités et _les nommer_ par un >verbe à l'infinitif.
>- Définir les **_cardinalités_** : nous allons expliquer ce concept via un >exemple.

</details>
