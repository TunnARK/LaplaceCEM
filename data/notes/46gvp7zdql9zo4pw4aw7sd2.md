
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

- Convertisseur basique (resistance + résistance variable)
    - +: très robuste
    - -: rendement très faible (trop de perte)

- Convertisseur type régulateur linéaire
    - ...

- Convertisseur type Hasher
    - commutation d'interrupteur
    - pas de puissance sur position ouvert et ferme d'un interrupteur
    - par contre a chaque switch une puissance (très grande) est émise (d'où la nécessité d'un dissipateur de chaleur)

- Problème du hasher c'est impossibilité parfois de permuter entre charge et décharge (i.e. charger telephone) -> nécessité d'un filtre 

- Cellule de commutation
    - cellule simple
    - monophasé -> convertisseur ondulatoire
    - triphasé -> moteur de voiture
![](/assets/images/whiteboard.20220701.CelluleCommutation.png)

## Discussion sur la maquette de TP

- Observer le courant parasite absorbé par le bus continu avec un tor ou un rsil

- rsil = reseau stabilisateur d'impédance de ligne

- Evaluer le spectre de perturbation electro-magnétique après variation du découpage/rapport cyclique

- notions à voir: courant commun, mode différentielle, cellule de commutation