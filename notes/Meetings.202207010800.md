---
id: 46gvp7zdql9zo4pw4aw7sd2
title: '202207010800'
desc: ''
updated: 1656662863802
created: 1656622570481
---

> Date: 2022/07/01

> Heure de départ: 08h50

> Heure de fin: 09h35

# Participants

- Vincent BLEY
- Antoine RONK

# Agenda

1. Explication sur les CEs
2. Présentation des cartes

# ToDo

- [ ] Comprendre le fonctionnement des cartes

# Notes

## Discussions sur les convertisseurs d'énergie

- Convertisseur basique (resistance + resitance variable)
    - +: tres robuste
    - -: rendement tres faible (trop de perte)

- Convertisseur type régulateur linéaire
    - ...

- Convertisseur type Hasher
    - commutation d'interrupteur
    - pas de puissance sur position ouvert et ferme d'un interrupteur
    - par contre a chaque switch une puissance (tres grande) est emise (d'où la necessité d'un dissipateur de chaleur)

- Probleme du hasher c'est l'impossibilte parfois de permutter entre charge et decharge (i.e. charger telephone) -> necessité d'un filtre 

- Cellule de commutation
    - cellule simple
    - monophasé -> convertisseur ondulatoire
    - triphasé -> moteur de voiture
![](/assets/images/whiteboard.20220701.CelluleCommutation.png)

## Discussion sur la maquette de TP

- Observer le courant parasite absorbé par le bus continu avec un tor ou un rsil

- rsil = reseau stabilisateur d'impédence de ligne

- Evaluer le spectre de perturbation electro-magnétique apres variation du découpage/rapport cyclique

- notions à voir: courant commun, mode différentielle, cellule de commutation