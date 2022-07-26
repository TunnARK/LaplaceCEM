
> Date : 2022/07/18, 2022/07/19

> Status : In Progress (Requesting Assistance from Manufacturer)

[[Lien vers texte en Français|experimentations.MesuresTestDCKEL]]

# Objective

- Reproduce the Demo Board performance curve of the [[equipements.DC2726A]]

- Follow the [[Quick Start Procedure | equipements.DC2726A#quick-start-procedure]] in the [Demo Manual](https://www.analog.com/media/en/technical-documentation/user-guides/dc2736af.pdf) 

![](/assets/images/dc2736a.measure.EfficiencyVsLoad.Vout12vFsw500hz.png){max-width: 300px, display: block, margin: 0 auto}

# Set Up

![](/assets/images/exp.MesuresTestDCKEL.SetUpPicAll.png){max-width: 600px, display: block, margin: 0 auto}

# Measurement at $\;T_A = 33°C\;$ and $\;V_{in}=30V\;$

- We don't get the same efficiency curve.

- We did not go beyond $11A$ to avoid burning out the board due to the high ambiant temperature we were operating in.

- Moreover, the transition from $9A$ to $10A$ is characterized by a drastic change in behavior:
    - The card emits a hissing sound for $10A$ ;
    - The measurements do not stabilize (even after 1min waiting) ;
    - We obtain a loss of $10\%$ on the output.

Here are the measurements that we have taken : $\qquad\qquad\qquad$ ([Donwload PDF](https://github.com/TunnRKA/LaplaceCEM/blob/master/notes/assets/2022.07.20.LaplaceCEM.TestingDC2736A.pdf))

![](/assets/images/exp.MesuresTestDCKEL.ExcelPrintEN.png){max-width: 800px, display: block, margin: 0 auto}

# Devices Used

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

- The measurements were made with the following methods:
    - [[equipements.KEL103]] Front Plug (2-wire modes): the cables carry current (which induces a voltage drop)
    - [[equipements.KEL103]] Back Plug (4-wires modes): the cables do not carry current

![](/assets/images/exp.MesuresTestDCKEL.CircuitMesure4fils.png){max-width: 600px, display: block, margin: 0 auto}

Here are the connectics used on the [[equipements.KEL103]] :

![](/assets/images/exp.MesuresTestDCKEL.PicKelMesureFront.png){max-width: 300px, display: block, margin: 0 auto}

![](/assets/images/exp.MesuresTestDCKEL.PicKelMesureBack.png){max-width: 300px, display: block, margin: 0 auto}