# Autocorrect

## Introduction 

Bon il s'agit de corriger les mots qui ont été mal orthographiés, en gros ceux qui n'existent pas dans un dictionnaire. Si le mot existe réellement, on ne fait rien, même si compte tenu du contexte, il y a vraisemblablement une erreur. Ca fonctionne de la façon suivante :
 1. identifier les mots mal orthographiés
 2. rechercher les mots situés à une distance edit de n
 3. sélectionner des mots candidats
 4. trouver le candidat le plus probable



## Edit distance

#### Définition

On peut modifier une chaine de caracteres par le biais de 4 opérations possibles. La edit distance entre deux mots est le nombre minimum d'opérations nécessaires pour passer d'un mot à l'autre. On peut attribuer des poids différents aux différentes opérations. Ci -dessous les 4 opérations possibles :

 1. Ajouter une lettre
 2. Enlever une lettre
 3. Permuter deux lettres adjacentes
 4. Modifier une lettre


#### Probabilité d'un mot

Métrique simple qui représente la fréquence d'un mot pour un corpus donné. En gros le nombre d'occurences d'un mot sur l'ensemble des mots constituant le corpus