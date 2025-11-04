# RICHARD_PLAT_JV3
Student project, 3D platformer in UE5.

## Controls

| Input    | Action     |
|----------|------------|
| Z/Q/S/D  | Move       |
| Spacebar | Jump       |
| E        | Dash combo |


## How to play
Try to reach the cylinder at the end of each level and collect all the coins you can. When you finish, alt+f4 to quit.

## Retour pédagogique
### Expérience attendue
Le jeu présente plusieurs petites mécaniques de platforming telles que le saut, le dash et les pièges. Des checkpoints sont placés fréquemment pour donner un côté die and retry ainsi que pour pouvoir placer des situations assez difficiles qui nécessitent plusieurs essais.

### Mécanique de character
Triple dash : quand on appuie sur E en étatn au sol, le joueur dash en avant. S'il dash plusieurs fois d'affilé, les dashs sont plus longs (jusqu'à 3). Si le joueur dash sur un mur fragile de sa taille, il le détruit.

### Mécaniques d'environnement
Plateformes pouvant avoir plusieurs comportements : endommager ou soigner le joueur, faire sauter le joueur, agrandir ou rétrécir le joueur, empêcher le joueur de dash.

Plateforme mouvante pouvant suivre un parcours, déclenchable automatiquement ou bien au contact du joueur.

Piège tuant le joueur au contact.

### Difficultés rencontrés
J'ai eu du mal au début du projet à m'approprier la structure Unreal : comment bien séparer le controller du character, qu'est-ce qui mérite d'être un blueprint, comment orchestrer les interactions etc. Maintenant j'ai mieux compris et j'ai été capable de rajouter les dernières mécaniques très rapidement sans problème.

J'ai également eu des difficultés pour référencer des points dans l'espace au sein des BP (à la manière d'un empty transform dans Unity), et la solution m'a été apportée grâce aux **SceneComponents**.

Concernant le langage BP, j'ai encore un peu de mal à retrouver le confort et la structuration de la programmation classique (pas de short circuit, difficile d'avoir une vue d'ensemble du source code, impossible de review les commits) mais je dois admettre que c'est très efficace pour du prototypage et on trouve toujours un moyen de parvenir à ses fins.

Globalement la courbe d'apprentissage d'Unreal me semble beaucoup plus difficile que pour Unity, mais les possibilités qu'offre le moteur en terme de pipelines, d'intégration d'assets et de travail collaboratif compensent largement cette difficulté.

### Choses à améliorer
J'ai conçu un système modulaire d'effets de plateformes que je peux cumuler (ex: une plateforme peut faire des dégats ET bump le joueur ET ralentir...) et qui détermine l'aspect de la plateforme grâce à son shader, mais je ne l'ai pas exploité dans le level design. Tant pis au moins je me suis bien amusé à le faire.

Je n'ai pas pris le temps de faire un écran de fin pour relancer ou quitter le jeu quand on le termine.

Le dash pourrait être un peu plus polish.
