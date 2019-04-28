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

|  Test  | Neurones | epochs | batch_size | loss final | acc final | résultats possibilité classifié  *lucario* |
| :----: | :------: | :----: | :--------: | :--------: | :-------: | :----------------------------------------: |
| **1**  |    40    |   9    |     5      |   2.8356   |  0.8241   |               8.8698494e-01                |
| **2**  |    40    |   9    |     6      |   3.8729   |  0.7531   |                9.999938e-01                |
| **3**  |    40    |   9    |     18     |   0.0995   |  0.9938   |               1.0000000e+00                |
| **4**  |    40    |   3    |     5      |   0.8018   |  0.9321   |               7.5087246e-07                |
| **5**  |    40    |   3    |     6      |   6.8477   |  0.5710   |                     1                      |
| **6**  |    40    |   3    |     18     |   0.5347   |  0.9383   |               9.7930348e-01                |
| **7**  |    40    |   5    |     5      |   3.7934   |  0.7531   |               1.0000000e+00                |
| **8**  |    40    |   5    |     6      |   0.4457   |  0.9660   |               1.00000000e+00               |
| **9**  |    40    |   5    |     18     |   0.9685   |  0.9043   |               9.9870980e-01                |
| **10** |    40    |   1    |     6      |   8.7995   |  0.4198   |               1.0000000e+00                |
| **11** |    40    |   1    |     18     |   6.5659   |  0.4537   |               9.9995327e-01                |





**Table 2, test avec nombre de Neurone à 20**

|  Test  | Neurones | epochs | batch_size | loss final | acc final | résultats possibilité classifié comme *lucario* |
| :----: | :------: | :----: | :--------: | ---------- | --------- | :---------------------------------------------: |
| **1**  |    20    |   9    |     5      | 9.6510     | 0.4012    |                  0.0000000e+00                  |
| **2**  |    20    |   9    |     6      | 5.9697     | 0.6296    |                  0.0000000e+00                  |
| **3**  |    20    |   9    |     18     | 0.0145     | 0.9969    |                  9.9998295e-01                  |
| **4**  |    20    |   3    |     5      | 0.5320     | 0.8858    |                   0.19999924                    |
| **5**  |    20    |   3    |     6      | 1.1511     | 0.9105    |                  1.8166089e-07                  |
| **6**  |    20    |   3    |     18     | 0.2049     | 0.9660    |                  9.8527676e-01                  |
| **7**  |    20    |   5    |     5      | 0.2487     | 0.9352    |                   0.44680107                    |
| **8**  |    20    |   5    |     6      | 0.1877     | 0.9599    |                  1.0000000e+00                  |
| **9**  |    20    |   5    |     18     | 0.0590     | 0.9753    |                    0.6501695                    |
| **10** |    20    |   1    |     6      | 4.2475     | 0.6235    |                  7.6487213e-02                  |
| **11** |    20    |   1    |     18     | 6.0379     | 0.4784    |                  9.9788934e-01                  |

### Conclusion

Après les analyses au-cessus, on peut savoir que : 

1, Plus la valeur **epochs** est grande, moins il y aura de perte d'informations, plus le résultat est précis

2, **batch_size** doit être le diviseur de nombre d'exemple à entraîner pour obtenir un résultat plus précis.

3, Avec 20 neurones n'est pas suffit pour prédire le type de Pokémon, c'est à dire que avec 20 neurones, il n'est pas suffit pour entraîner le modèle.



Grâce à une bonne qualité et quantité d'exemple sur notre entraînement, notre modèle prédit bien le type de Pokemon