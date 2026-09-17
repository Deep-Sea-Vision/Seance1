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