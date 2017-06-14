**Optimisation d’échangeurs de chaleur à film ruisselant**\
**\
**Nicolas CELLIER**\
Laboratoire LOCIE\
Campus Universitaire Savoie Technolac\
73376 Le Bourget du Lac\
`contact@nicolas-cellier.net` — +336 71 37 74 67\

![image](logo-arc-72dpi){height="4cm"} ![image](logo_ra){height="4cm"}
![image](locie-logo){height="4cm"}

[2]{}

Introduction {#introduction .unnumbered}
============

Phénomène observable dans les rues durant une averse particulièrement
intense, le film ruisselant est un écoulement complexe qui trouve des
applications au sein du génie des procédés industriels.

Échangeurs de chaleur, évaporateurs sont des équipements technologiques
pouvant tirer profit des caractéristiques particulières de ce phénomène.

En s’écoulant sur une surface plane et sous certaines conditions
hydrodynamiques, un fluide pourra commencer à se déstabiliser et
présenter des séries d’ondelettes à sa surface. Ce phénomène
s’accompagne d’une forte intensification des transferts (thermiques et
matière).

[2]{}

![image](thinfilm){height="4cm"}
![image](thinfilm_unstable){height="4cm"}

Problématique {#problématique .unnumbered}
=============

-   Couplage entre l’hydrodynamique et les phénomènes de transfert
    relativement peu étudié.

-   Sa maîtrise peut mener à une intensification des phénomènes au cœur
    d’équipements technologiques et à la réduction de leur encombrement.

-   Nécessité de modéliser correctement l’hydrodynamique du film, et le
    couplage avec les transferts de chaleurs / de masse.

Les modèles {#les-modèles .unnumbered}
-----------

-   Modèles industriels nombreux, mais imparfaits \[[@Killion2001]\].

    -   Beaucoup de corrélations basés sur films plats.

    -   Les films ruisselants verticaux sont instables quelque soit le
        Reynolds \[@Miller1998a\].

    -   Incompréhension des interactions hydro / thermique menant à
        l’intensification de transfert

-   Simulation numérique direct, couteuse

    -   Basé sur la résolution directe des équations de Navier et Stokes
        et de Fourrier.

    -   Le coût calcul interdit un travail d’optimisation en des temps
        raisonnables.

(1,0)[1500]{}

[2]{}

Travaux engagés {#travaux-engagés .unnumbered}
===============

Modélisation hydrodynamique {#modélisation-hydrodynamique .unnumbered}
---------------------------

Modèle asymptotique intégré sur la hauteur du film a été développé, basé
sur les travaux de @Ruyer-Quil2000.

[2]{} $$\begin{aligned}
            \partial_t h =& -\partial_x q\\
            3 \mathrm{Re} \partial_t q =& \frac{5}{6} h
                \left(
                    1 - Ct \partial_x h + We \partial_{x,x,x} h
                \right)\\
            & - \frac{5}{2}\frac{q}{h^2}
            - \frac{5}{4} M \partial_x \theta \\
            & + 3 \mathrm{Re}
                \left(
                    \frac{9}{7}\frac{q}{h}^2 \partial_x h - \frac{17}{7}\frac{q}{h} \partial_x q
                \right)
        \end{aligned}$$

![image](01-established_wave_streamlines){width="0.95\columnwidth"}
\[fig:streamlines\]

On observe nettement les effets de recirculation au sein de l’onde
décrits par @Brauner1989, @Yoshimura1996 ou @Miyara1999.

Couplage thermique {#couplage-thermique .unnumbered}
------------------

Suivant un développement analogue, un modèle asymptotique a été écrit
basé sur les équations de Fourrier (publication en cours d’écriture).

[2]{}

![image](01-established_wave_T){width="0.98\columnwidth"}
\[fig:thermal\]

![image](01-established_wave_Tmag_streamlines){width="0.98\columnwidth"}
\[fig:streamlines\_thermal\]

On observe nettement un front thermique situé proche du point de
stagnation du fluide au sein de la vague. A noter que le modèle n’est
pas assez complexe pour représenter correctement ce phénomènes.

Impact de la fréquence de forçage {#impact-de-la-fréquence-de-forçage .unnumbered}
---------------------------------

[2]{}

### Sur l’hydrodynamique {#sur-lhydrodynamique .unnumbered}

Les simulations ont été faite avec un bruit blanc en entrée additionné
d’un forçage sinusoidale.

![image](01-frequency_effect){width="0.98\columnwidth"} \[fig:thermal\]

Pour de haute et de basses fréquences, les ondes naturelles dominent.

### Sur l’intensification de transfert {#sur-lintensification-de-transfert .unnumbered}

Suite des travaux {#suite-des-travaux .unnumbered}
=================

[2]{}

Prise en compte de la turbulence {#prise-en-compte-de-la-turbulence .unnumbered}
--------------------------------

Les Reynolds présentés sont un Reynolds moyen, basé sur le film plat
équivalent. Il peut être bien plus élevé, en particulier à la crête des
ondes.

L’objectif est de réécrire le modèle en incluant une viscosité
turbulente via des lois de comportements usuelles. Les tourbillons de
petites échelles sont pris en compte via leurs dissipations d’énergie au
sein de l’écoulement.

Effet Marangoni et *dry patchs* {#effet-marangoni-et-dry-patchs .unnumbered}
-------------------------------

L’effet Marangoni est lié à la dépendance entre les caractéristique du
fluide et la tempéraature (ou la concentration d’un solvant), en
particulier sur la tension de surface.

Cet effet mène à une instabilité supplémentaire, souvent dans le sens
transverse de l’écoulement et mène à la formation de rivulets, et à un
assèchement local de l’écoulement dans les cas extrèmes.

(1,0)[1500]{}

[2]{}

   $\rho$       masse volumique
  -------- -------------------------
    $u$        champs de vitesse
    $p$            pression
   $\tau$   tenseur des contraintes
    $h$     hauteur de l’interface

    $q$        débit local
  -------- --------------------
    $f$      force volumique
    $Ct$     Facteur de pente
    $Re$    Nombre de Reynolds
   $W\!e$    Nombre de Weber

Encadrement de thèse :

-   C. Ruyer - Quil (LOCIE)

-   N. Caney (LEGI)

-   P. Bandelier (CEA - Liten)

Partenaire industriel : CIAT

Mis en place et soutenu par la région Rhône-Alpes

(1,0)[1500]{}

Données et contenu additionnel {#données-et-contenu-additionnel .unnumbered}
==============================

Source

:   <https://github.com/celliern/arc_2017>

Élément de reproductibilités

:   <https://nbviewer.jupyter.org/github/celliern/arc_2017/blob/master/contenu_additionnel.ipynb>

Solveur utilisé

:   <https://locie.github.io/triflow/>


