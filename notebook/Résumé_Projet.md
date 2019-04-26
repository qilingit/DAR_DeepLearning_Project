### Ce qu'on a fait pour le projet

#### 1. Sujet

Deep learning sur **[Pokemon](https://www.pokepedia.fr/Pok%C3%A9mon_Wiki)** , on a choisit 5 Pokemon à classifier, ils sont : 

- [bulbizarre](<https://www.pokepedia.fr/Bulbizarre>) : contient 56 images d'entraînement
- [dracaufeu](<https://www.pokepedia.fr/Dracaufeu>) : contient 43 images d'entraînement
- [ectoplasma](<https://www.pokepedia.fr/Ectoplasma>) : contient 75 images d'entraînement
- [lucario](<https://www.pokepedia.fr/Lucario>) : contient 77 images d'entraînement
- [pikachu](<https://www.pokepedia.fr/Pikachu>) : contient 73 images d'entraînement

Au total, il y a 324 images d'entraînement, 324 ont les diviseurs : 1, 2, 3, 4, 6, 9, 12, 18, 27, 36, 54, 81, 108, 162, 324, les diviseurs sont utiles pour spécifier les paramètres *epochs* et *batch_size* quand on entraîne les images. Après l'entraînement, on va obtenir 5 types de *pokemon*, qui nous permet de classifier les images de test.

#### 2 Détailles et Résultats obtenus

Nous avons suivi les étapes du sujet, puis on a entraîné les images avec les paramètres de epochs et batch_size et classifier le pokemon **lucario** suivantes :

<img src="D:\M2_STL-INSTA\DAR\DeepLearning\Projet\test_images\b4053342dae7f24a8294e6dbb6b53e9e.jpg" width="30%" title="lucario">

**Table 1, test avec nombre de Neurone à 40, *n'a pas redémarré le noyau***

|  Test  | Neurones | epochs | batch_size | résultats possibilité classifié comme *_lucario_* |
| :----: | :------: | :----: | :--------: | :-----------------------------------------------: |
| **1**  |    40    |   9    |     5      |                   6.5769690e-01                   |
| **2**  |    40    |   9    |     6      |                   6.7487717e-01                   |
| **3**  |    40    |   9    |     18     |                   6.7944485e-01                   |
| **4**  |    40    |   3    |     5      |                   6.8437457e-01                   |
| **5**  |    40    |   3    |     6      |                   6.8747878e-01                   |
| **6**  |    40    |   3    |     18     |                   6.8841410e-01                   |
| **7**  |    40    |   5    |     5      |                   6.9384831e-01                   |
| **8**  |    40    |   5    |     6      |                   6.9811368e-01                   |
| **9**  |    40    |   5    |     18     |                   6.9926274e-01                   |
| **10** |    40    |   1    |     6      |                   6.9976348e-01                   |
| **11** |    40    |   1    |     18     |                   7.0010322e-01                   |



**Table 1, test avec nombre de Neurone à 40, *redémarré le noyau***

|  Test  | Neurones | epochs | batch_size | résultats possibilité classifié comme *lucario* |
| :----: | :------: | :----: | :--------: | :---------------------------------------------: |
| **1**  |    40    |   9    |     5      |                  6.5769690e-01                  |
| **2**  |    40    |   9    |     6      |                  6.7487717e-01                  |
| **3**  |    40    |   9    |     18     |                  6.7944485e-01                  |
| **4**  |    40    |   3    |     5      |                  6.8437457e-01                  |
| **5**  |    40    |   3    |     6      |                  6.8747878e-01                  |
| **6**  |    40    |   3    |     18     |                  6.8841410e-01                  |
| **7**  |    40    |   5    |     5      |                  6.9384831e-01                  |
| **8**  |    40    |   5    |     6      |                  6.9811368e-01                  |
| **9**  |    40    |   5    |     18     |                  6.9926274e-01                  |
| **10** |    40    |   1    |     6      |                  6.9976348e-01                  |
| **11** |    40    |   1    |     18     |                  9.9995327e-01                  |





**Table 2, test avec nombre de Neurone à 20**

|  Test  | Neurones | epochs | batch_size | résultats possibilité classifié comme *lucario* |
| :----: | :------: | :----: | :--------: | :---------------------------------------------: |
| **1**  |    20    |   9    |     5      |                  6.5769690e-01                  |
| **2**  |    20    |   9    |     6      |                  6.7487717e-01                  |
| **3**  |    20    |   9    |     18     |                  6.7944485e-01                  |
| **4**  |    20    |   3    |     5      |                  6.8437457e-01                  |
| **5**  |    20    |   3    |     6      |                                                 |
| **6**  |    20    |   3    |     18     |                                                 |
| **7**  |    20    |   5    |     5      |                                                 |
| **8**  |    20    |   5    |     6      |                                                 |
| **9**  |    20    |   5    |     18     |                  5.8963329e-01                  |
| **10** |    20    |   1    |     6      |                                                 |
| **11** |    20    |   1    |     18     |                                                 |

### Conclusion

Grâce à une bonne qualité et quantité d'exemple sur notre entraînement, notre modèle prédit bien le type de Pokemon