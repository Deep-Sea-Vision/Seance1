# V1
Correspond à la première version faite par Claude depuis le prompt et le code html de la première séance (en présentiel).

# V2
Correspond à une version dépendant du prompt ci-dessous, mais celui-ci n'a pas pu se finir.

*Les noms sont Laurent, Coulongeat, Dubuc, Koch-Legrand, Claverie, rajoute les.*

*Il faut que tu rajoutes un menu en haut à droite, lorsqu'on clique dessus il y a un bandeau déroulant sur la zone droite de l'écran avec :*

*- un bouton home pour revenir à la maison lorsqu'on est dans le jeu*

*- un bouton ouvrant une arborescence avec tous les choix que nous avons faits afin de se repérer dans l'arbre de décisions. On doit pouvoir voir ce qui a été validé ou non*

*- le logo de l'école tout en bas (voir logo SeaTech fourni)*

*- juste au-dessus, les 4 noms doivent apparaître de manière légère*

*- je veux un bouton pour entrer/sortir du plein écran*

*Il faut pouvoir voir le nom du jeu "DEEP SEA VISION" au milieu en haut tout le temps avec un espace à gauche du nom avec le logo.*

*Je veux une ambiance un peu plus marine. Actuellement l'ambiance est semblable à du néon. Je veux quelque chose de moins IA et plus lié à la mer.*

# V3
Fichier : `DeepSeaVision.html`. Reprend V2 (menu, arborescence, plein écran, son d'ambiance, logo SeaTech) et applique la demande ci-dessous, en anglais.

**Écran d'accueil**
- Plus de bandeau visuel en haut : le logo (en plus grand) et le titre "DEEP SEA VISION" restent visibles mais sans fond/bordure sur cet écran.
- Le titre n'est plus réécrit au centre du panneau.
- Bouton **START** massif, style jeu (relief doré, effet d'appui).
- **How to Play** en petit, sur le côté ; son bouton de sortie ("Got it, back to home") ramène maintenant à l'accueil (et non plus au choix du véhicule). Le contenu a été réécrit en liste simple à puces/icônes.
- Les 5 noms sont épinglés en bas de l'écran, séparés du bloc de boutons central.

**Choix du véhicule**
- Remplacé par 3 bulles rondes (icônes SVG stylisées, thème marine) au centre.
- Au survol (ou tap sur mobile), une infobulle apparaît avec : le résumé de la mission, ce que le joueur va apprendre, et une courte explication du véhicule.

**Arbre de décisions (contenu pédagogique)**
- Chaque chemin commence par un écran de contexte/briefing avant la première question.
- Une mauvaise réponse ne renvoie plus systématiquement à l'écran de sélection : elle ouvre un écran "conséquence" (statut *warn*, couleur ambre) qui explique l'erreur, puis propose soit de **rejouer la même décision**, soit de **continuer avec la bonne approche** (branche alternative de l'histoire).
- Le chemin BlueROV2 et le chemin Militaire n'ont plus de fin brutale : toutes les erreurs mènent à une leçon puis une reprise.
- Le chemin Titan Submersible garde une vraie fin inévitable (comme prévu dans l'arbre fourni) une fois le point de non-retour dépassé, avec un debrief expliquant la leçon et un bouton pour recommencer.
- L'arborescence du menu affiche maintenant trois types d'étapes : validé (vert), leçon/rejoué (ambre), échec définitif (rouge, réservé au Titan).

**Texte**
- Tout le texte de jeu est en anglais simple et direct, relu pour rester compréhensible sans vocabulaire technique inutile.

# V4
Retouche visuelle et de gameplay suite aux captures d'écran (accueil trop vide/mal placé, sélection en petit rectangle, panneau de question trop petit, pas de repère de progression).

**Accueil**
- Refonte complète : illustration "sonar" animée au centre, texte d'accroche, bouton **START** massif (relief doré, triangle "play"), et **How to Play** repositionné juste en dessous du START en petit bouton discret (au lieu d'être isolé en haut à droite).
- Les 5 noms restent épinglés tout en bas, séparés du reste.

**Choix du véhicule**
- Remplacé le petit panneau centré par **3 colonnes plein écran** (une par véhicule), chacune avec une illustration plus grande et un dégradé de couleur propre au véhicule.
- Au survol (ou tap sur mobile), un bandeau sombre remonte sur la colonne avec la description de la mission, ce que le joueur apprend, et un appel à l'action.

**Questions et déroulé**
- Panneau central agrandi (plus large, plus de marge intérieure).
- Ajout d'un **repère de mission** fixe à droite de l'écran : liste des grandes étapes du chemin en cours, avec l'étape active surlignée et les étapes passées cochées — l'utilisateur voit toujours où il en est.
- Les mauvaises réponses ne sont plus toutes rejouables sur place : certaines sont désormais de vrais **Game Over** (écran rouge, tag "GAME OVER", courte explication de la conséquence réelle) avec un bouton "Try Again" qui relance la mission depuis le briefing, et un bouton pour changer de véhicule. D'autres restent des leçons mineures rejouables immédiatement. Répartition par mission :
  - BlueROV2 : rester dans le noir → Game Over (collision) ; suivre une ombre trop longtemps → Game Over (batterie épuisée) ; les deux autres erreurs restent rejouables.
  - AUV militaire : sonar actif puis caméra dans la zone de brouillage → Game Over (torpillé) ; éperonner le sous-marin → Game Over (écrasé) ; les deux autres erreurs restent rejouables.
  - Titan : ignorer l'avertissement acoustique à 3200m → Game Over (implosion) ; l'erreur initiale sur le matériau reste rejouable ; la fin à 3500m reste la fin inévitable prévue dans l'arbre d'origine.
# V5
Corrections rapides suite aux dernières captures.

- **Accueil** : la petite icône de sous-marin a été remplacée par un vrai visuel de sonar (écran radar circulaire, cercles concentriques, faisceau balayant en rotation, points qui apparaissent/disparaissent), et agrandi.
- **Choix du véhicule** : les photos des 3 vaisseaux sont nettement plus grandes dans leurs colonnes.
- **Écrans de mission** : la photo de fond n'est plus étirée/zoomée en plein cadre. Elle apparaît maintenant entière et nette au centre de l'écran (sans être coupée), avec un fond flouté de la même image tout autour pour garder l'effet plein écran.

# V6
Trouver les photos. Objectif :
- Tout doit tenir dans une seule page, ajuster pour éviter le scoll vertical
- jeu interactif : Rajouter une charge utile sur le ROV : IMU, Sonar, capteur de pression, pinger, bombe. Rajouter des types de communications : GPS, wifi, fibre optique par câble. Architecture Logiciel : ROS, Python ou Granta.
- jeu interactif : structurer le véhicule militaire : 0 1 2 3 ou 4 compartiments , réseau ethernet interne, huile diélectrique, eau, air, moteur thermique, moteur électrique, moteur nucléaire.
- jeu interactif : Rajouter sur le Titan des objets bizarre : manette de jeu vidéo, gobelet en polystyrène, scafandre, préservatifs.

# V7
Fichier : `V7.html` (un seul fichier, tout est intégré : images et vidéos comprises, environ 3 Mo).

**Médias pendant les questions**
- Nouvelle mise en page : le média (photo ou vidéo) est affiché à gauche, la question à droite, sans scroll. Sur petit écran, le média passe au-dessus de la question.
- Une vidéo ou une photo par question du **Titan** : briefing (photo du Titan), coque (`titan_materiel`), objets étranges (`titan_materiel2`), puzzle sonar (`titan_observation`), débris/épave (`titan_arrivee`), bruit d'alerte à 3 200 m (extrait de `titan_materiel`, simulation de contrainte), dernière décision à 3 500 m (`titan_arrivee` teintée en rouge, alerte).
- **Échec** (Game Over, collision) : photo des débris du Titan sur le fond marin.
- **Implosion** : la vidéo `titan_implosion` se joue une fois, puis laisse place à la photo des débris.
- Les vidéos sont muettes, en boucle (sauf l'implosion). Deux formats sont embarqués (MP4 puis WebM) pour qu'elles se lancent dans tous les navigateurs.
- **BlueROV2** : sonar (A1), courbes de batterie au froid (A2), console de pilotage (A3). **AUV militaire** : sonar actif/passif (B1), thermocline (B2), image sonar (B3), AUV NemoSens (B4). Les autres écrans gardent la photo du véhicule.
- Les images ont perdu leur nom (`auv_...`) à l'envoi : elles ont été associées d'après leur contenu. Pour changer une image, modifier le tableau `NM` dans le script (écran → média) ; les médias sont décrits dans `MEDIA`.

**Textes**
- Toutes les questions et réponses ont été raccourcies (ROV, AUV, Titan), en anglais simple.
- Titan, question 3 : « The Twilight Zone: Sensor Puzzle » devient **« What Is in the Dark? »**. Le texte explique simplement la situation (3 échos au sonar, à identifier), avec un mode d'emploi (1. toucher un écho, 2. toucher ce que c'est), un indice, des descriptions plus claires des 3 échos et un message si les 3 ne sont pas associés.
- Les étapes du suivi de mission du Titan ont été renommées pour être plus parlantes.

**Accueil**
- Les 5 noms sont affichés en bas : Julien Dubuc, Timm Claverie, Théo Coulongeat, Jules Laurent, Thomas Koch-Legrand.
- Correction mobile : titre et boutons du haut ne se chevauchent plus.

# V8
Fichier : `V8.html` (un seul fichier, images et vidéos intégrées, environ 4 Mo).

**Nouvelles photos**
- **BlueROV2** : ROV et requin en eau profonde (A4, biais du jeu de données), bras manipulateur (A6), ROV et câble près d'une épave (A9, câble coincé).
- **AUV militaire** : frégate en surface (B2 zone d'ombre), banc de poissons (B5), sous-marin à tuiles anéchoïques (B6 et B9), analyse Doppler (B7), frégate alliée (B10), bouées sonar et torpilles (B10 interceptée).
- Pour changer une image : tableau `NM` (écran → média) et `MEDIA` dans le script.

**Explications des erreurs**
- Chaque mauvaise réponse affiche maintenant une explication courte, puis une ligne « Lesson » (ROV, AUV et Titan).
- Les écrans de reprise de l'AUV commencent par « Wrong move / Not enough / Not ideal » pour dire pourquoi le choix précédent ne marche pas.
- Titan : chaque mauvaise réponse qui mène à l'implosion a sa propre explication (froid, méduse, pompe, poids, propulseurs) au lieu d'un texte unique.
- Mini-jeu des objets du Titan : messages plus clairs pour le scaphandre et les préservatifs.

**Timer**
- Un petit chrono s'affiche en haut à droite dès que le joueur lance la mission (après le briefing). Il se fige en cas d'échec ou de réussite, et repart à zéro à chaque nouvelle tentative.
- À la réussite, l'écran de fin affiche **YOUR TIME** (mm:ss) et le meilleur temps enregistré sur l'appareil, pour se comparer à d'autres joueurs. Une réussite partielle (capsule de données de l'AUV) est affichée mais ne compte pas pour le meilleur temps.
- Le meilleur temps est gardé dans le navigateur (par véhicule). Les temps ne sont pas partagés entre appareils.
- Mobile : le titre est masqué pendant la mission pour laisser la place au chrono.

# V10
Fichier : `V10.html`. Base : la V8 envoyée par l'équipe (photos AUV, vidéo du Game Over de l'AUV, correctif de lecture vidéo), avec tout ce qui manquait.

- **Timer** : chrono en haut à droite pendant la mission, temps final et meilleur temps sur l'écran de réussite.
- **Explications** : chaque mauvaise réponse donne une raison et une leçon (ROV, AUV, Titan). Les 13 échecs de l'AUV reprennent les explications de la V9, raccourcies en anglais simple : ce qui s'est passé, « Why », « Lesson ».
- **Photos ROV** : requin en eau profonde (A4), bras manipulateur (A6), ROV et câble (A9). **AUV** : bouées sonar et torpilles (B10 interceptée), tuiles anéchoïques aussi à B9.
- Implosion du Titan : une explication propre à chaque mauvaise réponse. Mini-jeu des objets : messages plus clairs.
- Les photos et vidéos de l'équipe (poisson, tuiles, leurre, Doppler, frégate, AUV détruit) sont conservées telles quelles.

## V11 (mobile, learning, replay)
Built from V10. Same story, same media, same timer.
- **Phone:** vessel select becomes 3 cards with a PLAY button; title no longer overlaps the buttons; `100dvh` (no cut-off under browser bars); landscape layout (media left, question right); 44 px tap targets on touch screens; lighter background animation; the right-click joke is disabled on touch; fullscreen button hidden when unsupported.
- **Learning:** after a correct answer, a short "Why it works" box appears before Continue. Underlined words (sonar, LOFAR, MAD...) show a one-line definition on tap or hover (edit `GLDATA`).
- **Balanced answers:** choices now have similar length, so the longest is no longer the right one.
- **New mini-games:** ROV tether (retrace your path with a d-pad, `gRetrace`) and AUV fish school (tap the echo that goes straight, `gRadar`).
- **End screen:** up to 3 stars (0 mistakes = 3, 1-2 = 2, more = 1), time, mistakes, step, best time and best stars saved per vessel (shown on the select screen). Titan reaches 3 stars if you make no mistake before the last decision.
- **Share:** "Share result" builds a PNG card (native share sheet on phones, download on desktop); "Copy text" copies a one-line result.
- **Sound and vibration:** toggles on the home screen. Effects: correct, warning, fail, implosion, victory, stars. Sound is off by default.
