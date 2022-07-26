
# Compatibilité Electro-Magnétique

## Définition

> Source: ![La CEM appliquée à
l’électronique de puissance, Bertrand REVOL, édité le 12/03/2018](/assets/NotesDeCours.SystemesEtCompoPassifs2021.pdf) ([download](https://eduscol.education.fr/sti/sites/eduscol.education.fr.sti/files/ressources/pedagogiques/9699/9699-la-cem-appliquee-lelectronique-de-puissance-ensps.pdf))

- **Emission** et **Susceptibilité** sont les deux mots clés de la compatibilité électromagnétique.

- **Emission** = aptitude d'un appareil à transmettre des signaux perturbateurs à son
entourage

- **Susceptibilité** =  capacité de ce même dispositif à être perturbé par l'extérieur

- **Auto-perturbation** = possibilité d'un système de se perturber lui-même => **CEM intra-système**

- **Sources** = les générateurs de perturbations

- **Chemins** = équipements permettant la propagation des perturbations

- **Victimes** = équipements recevant une perturbation

![](/assets/images/schema.EnvironnementElectromagnetique.png){max-width: 300px, display: block, margin: 0 auto}



# Notions Importantes

## Gammes de Fréquences Concernées

![](/assets/images/courbe.GammeFreqCEM.png){max-width: 600px, display: block, margin: 0 auto}

## Mode Commun et Mode Différentiel

> Source: ![La CEM appliquée à
l’électronique de puissance, Bertrand REVOL, édité le 12/03/2018](/assets/NotesDeCours.SystemesEtCompoPassifs2021.pdf) ([download](https://eduscol.education.fr/sti/sites/eduscol.education.fr.sti/files/ressources/pedagogiques/9699/9699-la-cem-appliquee-lelectronique-de-puissance-ensps.pdf))

- Mode différentiel = mode symétrique = mode transversale

$$
\begin{cases}
i_{MD} = \dfrac{\,i_1 - i_2\,}{2}\\[0.5cm]
v_{MD} = i_1 - i_2\\[0.25cm]
\end{cases}
$$

- Mode commun = mode asymétrique

$$
\begin{cases}
i_{MC} = i_1 + i_2\\[0.5cm]
v_{MC} = \dfrac{\,v_1 + v_2\,}{2}\\[0.25cm]
\end{cases}
$$

> Source: page 10-12 de !["Systèmes et Composants Passifs 2021"](/assets/NotesDeCours.SystemesEtCompoPassifs2021.pdf) 
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