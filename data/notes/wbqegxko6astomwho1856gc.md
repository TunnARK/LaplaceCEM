
> Date : 2022/07/18, 2022/07/19

> Status : In Progress

# Objectif

Reproduire la courbe de rendement du Demo Board ci-dessous en suivant la [[Quick Start Procedure | equipements.DC2726A#quick-start-procedure]] dans le [Demo Manual](https://www.analog.com/media/en/technical-documentation/user-guides/dc2736af.pdf) du [[equipements.DC2726A]]

![](/assets/images/dc2736a.measure.EfficiencyVsLoad.Vout12vFsw500hz.png){max-width: 300px, display: block, margin: 0 auto}

# Set Up

![](/assets/images/exp.MesuresTestDCKEL.SetUpPicAll.png){max-width: 600px, display: block, margin: 0 auto}

# Mesures à $\;T_A = 33°C\;$ et $\;V_{in}=30V\;$

- Nous n'obtenons pas la même courbe de rendement.

- Nous ne sommes pas allés au-delà de $11A$ pour éviter de claquer la carte à cause de la chaleur.

- De plus, le passage de $9A$ à $10A$ se caractérise par un changement drastique de comportement :
    - La carte émet un sifflement ;
    - Les mesures ne se stabilise pas ;
    - On obtient une perte de $10\%$ sur le rendement.


Voici les mesures que nous avons prélevé :
![](/assets/images/exp.MesuresTestDCKEL.ExcelPrint.png){max-width: 800px, display: block, margin: 0 auto}

# Equipements

1. Source : [[equipements.GEN1500W]]
2. Filtre RSIL : [[equipements.ENV216]]
3. Convertisseur : [[equipements.DC2726A]]
4. Charge : [[equipements.KEL103]] 

### 1. GEN1500W

![](/assets/images/exp.MesuresTestDCKEL.PicGen1500w.Front.png){max-width: 600px, display: block, margin: 0 auto}

![](/assets/images/exp.MesuresTestDCKEL.PicGen1500w.Back.png){max-width: 600px, display: block, margin: 0 auto}

### 2. ENV216

![](/assets/images/env216.PicFront.png){max-width: 600px, display: block, margin: 0 auto}

### 3. DC2726A

![](/assets/images/exp.MesuresTestDCKEL.PicDcTop.png){max-width: 600px, display: block, margin: 0 auto}

![](/assets/images/exp.MesuresTestDCKEL.PicDcBot.png){max-width: 600px, display: block, margin: 0 auto}

### 4. KEL103

![](/assets/images/exp.MesuresTestDCKEL.PicKelFront.png){max-width: 600px, display: block, margin: 0 auto}

- Les mesures ont été réalisé avec la méthode des 4 fils :
    - Front (modes 2 fils) : les câbles transportent le courant (donc apparition une chute de tension)
    - Back (modes 4 fils) : les câbles ne transportent pas de courant

![](/assets/images/exp.MesuresTestDCKEL.CircuitMesure4fils.png){max-width: 600px, display: block, margin: 0 auto}

Voici les connectiques utilisées sur le [[equipements.KEL103]] :

![](/assets/images/exp.MesuresTestDCKEL.PicKelMesureFront.png){max-width: 300px, display: block, margin: 0 auto}

![](/assets/images/exp.MesuresTestDCKEL.PicKelMesureBack.png){max-width: 300px, display: block, margin: 0 auto}