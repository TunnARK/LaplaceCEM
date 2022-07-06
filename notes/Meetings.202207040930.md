---
id: xlmqt8j603149nttemahpc3
title: '202207040930'
desc: ''
updated: 1657101951510
created: 1656922993577
nav_exclude: true
---

> Date: 2022/07/04

> Heure de départ: 09h30

> Heure de fin: 10h20

# Participants

- Vincent BLEY
- Antoine RONK

# Agenda

1. Explication des maquettes
2. Présentation des ressources

# ToDo

- [x] Comprendre les modes différentielles
- [x] Comprendre les modes communs
- [ ] Comprendre le RSIL
- [ ] Etudier les data sheets

# Notes

![](/assets/images/whiteboard.20220704.meeting2.png){max-width: 600px, display: block, margin: 0 auto}

## Schema de la maquette

![](/assets/images/schema.RSILetAnalyseurTore.png){max-width: 600px, display: block, margin: 0 auto}

![](/assets/images/schema.RSILetAnalyseur.png){max-width: 600px, display: block, margin: 0 auto}

## Transformateur / Tore

![](/assets/images/schema.TransformateurTore.png){max-width: 300px, display: block, margin: 0 auto}

- Tore avec bobine de cuivre et anneau magnétique
    - Ne peut pas être utilisé pour du DC mais 'robuste' en haute fréquence (i.e. 150kHz-30MHz)
    - Mesure indirectement le courant $i_1$ via la tension $v_2$ en utilisant le [[Théorème d'Ampère|Lexique.ThmAmpere]]
    - $v_2 = \dfrac{\,R_2\,}{m}\,i_1$
    - avec $m = \dfrac{\,v_2\,}{v_1}$ selon la [[loi de Maxwell-Faraday|Lexique.LoiMaxwellFaraday]]

- Deux façons de faire la mesure avec des tores selon que le courant soit MD ou MC

![](/assets/images/schema.MesureTore.png){max-width: 300px, display: block, margin: 0 auto}

## Courants à Mode Différentiel/Commun (MD/MC) 

> cf page 10-12 de !["Systèmes et Composants Passifs 2021"](/assets/NotesDeCours.SystemesEtCompoPassifs2021.pdf) 
([download](https://github.com/TunnRKA/LaplaceCEM/blob/master/notes/assets/NotesDeCours.SystemesEtCompoPassifs2021.pdf))

![](/assets/images/schema.ModeDiffCom.png){max-width: 450px, display: block, margin: 0 auto}

![](/assets/images/ModeDiffComRepPratique.png){max-width: 450px, display: block, margin: 0 auto}


- Mode différentiel => courant à contre sens
- Mode commun => courant dans le même sens (donc retour via la masse)
- On en déduit :
$$
\begin{cases}
i_{MD} = \dfrac{\,i_1 - i_2\,}{2}\\[0.5cm]
i_{MC} = i_1 + i_2\\[0.25cm]
\end{cases}
$$
En effet, 
$$
\begin{cases}
i_1 = \dfrac{\,i_{MC}\,}{2} +\, i_{MD}\\[0.5cm]
i_2 = \dfrac{\,i_{MC}\,}{2} -\,i_{MD}\\[0.25cm]
\end{cases}
$$

## Perturbation liées aux convertisseurs

> cf page 15 de !["Systèmes et Composants Passifs 2021"](/assets/NotesDeCours.SystemesEtCompoPassifs2021.pdf) 
([download](https://github.com/TunnRKA/LaplaceCEM/blob/master/notes/assets/NotesDeCours.SystemesEtCompoPassifs2021.pdf))

- Unité $dB_{\mu A}$
$$
dB_{\mu A} = 20 \cdot log(\, 10^6 \cdot i_A \,)
$$

- $T_{dec}$ = période de découpage
- $T_m$ = temps de montée

- Fréquence de coupure est proportionnel à l'inverse du temps de montée $T_m$ du convertisseur

    Donc **_"plus le temps de montée est court, plus il faudra filtrer d'amplitudes perturbatrices"_**
    
    car la surface du spectre est plus grande lorsque $T_m$ est petit

- Par contre **_"plus le temps de montée est grand, moins le convertisseur aura un rendement efficace"_**

    car la puissance se calcule ainsi :

$$
P = \big(\, E_{on} + E_{off} \,\big) \cdot f_{commutation} \qquad j \cdot s^{-1} \qquad (Watt)
$$

![](/assets/images/courbe.EnergieCommutation.png){max-width: 300px, display: block, margin: 0 auto}


![](/assets/images/output.CommutationHacheur.png){max-width: 600px, display: block, margin: 0 auto}

## Impédance (à approfondir)

- Impédance Linéaire _(valide pour un signal sinusoïdale)_
$$
\underline{z}_L = j\,L\,\omega
$$

- Impédance Convertisseur
$$
\underline{z}_C = \dfrac{1}{\,j\,L\,\omega\,}
$$

![](/assets/images/schema.ImpedanceConvertisseur.png){max-width: 300px, display: block, margin: 0 auto}

- Calcul d'une impédance
$$
\underline{z} = \dfrac{\,\underline{U}\,}{\underline{I}}
$$

## RSIL (à vérifier et à compléter)

- EST = équipement sous test 

- **L'inducteur agit comme un filtre passe bas** pour empêcher les perturbations à haute fréquence venant de l'alimentation de passer vers l'EST

- **Le capaciteur lui agit comme un filtre passe haut** pour permettre de mesurer les hautes fréquences de l'alimentation

![](/assets/images/schema.RSIL.png){max-width: 450px, display: block, margin: 0 auto}

## Différents types de convertisseurs

- AC/DC -> appelé "redresseur"
- Hacheur
    - ceux en salle de TP
    - Fait de Silicium
- Convertisseur de GanSystems et EPC
    - Fait avec du GaN
