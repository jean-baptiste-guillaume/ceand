# Complément de visuels pour le visual novel

17 nouvelles images — 16 octobre 2026. Ce complément s’ajoute au premier pack. Il ne contient ni remplacement d’image ni nouvelle version du jeu.

## Dépôt dans GitHub

1. Décompresser le ZIP sur l’ordinateur.
2. Dans GitHub, ouvrir `ceand/visual-novel`, puis **Add file → Upload files**.
3. Glisser le dossier `assets` et les quatre fichiers placés à côté dans le ZIP. Le dossier `assets` se fusionnera avec celui du dépôt grâce à ses sous-dossiers `backgrounds` et `characters`.
4. Faire **Commit changes**, par exemple avec le message « Ajout des poses de dialogue et des transitions du visual novel ».

Déposer le contenu extrait directement dans `visual-novel`, sans créer un dossier `visual_novel_ajouts_v2` supplémentaire. Ne pas renommer les PNG. Ne pas déposer le ZIP fermé : les images doivent exister individuellement dans le dépôt.

Les nouveaux noms sont tous distincts des fichiers V1. Les anciens `index.html`, `manifest.json`, `ui/visual-novel.css` et les 19 images du premier pack restent en place. Le catalogue de ce complément s’appelle `apercu-ajouts-v2.html`.

## Nouveaux décors

| Fichier dans assets/backgrounds | Fonction |
|---|---|
| bg_corridor_porte.png | Arrivée devant la porte de la salle, pour la décision d’installation |
| bg_consultation_seuil.png | Vue depuis la porte ouverte, pour matérialiser l’entrée dans la salle |
| bg_corridor_sortie.png | Vue du couloir vers la sortie, pour la conclusion et le départ |

## Nouvelles poses des personnages

Chaque ligne est disponible pour Khloé et Élise. Les fichiers se trouvent dans `assets/characters` et commencent par `khloe_` ou `elise_`.

| Suffixe après le prénom | Usage prévu |
|---|---|
| assise_ecoute_face.png | Écoute en couleur, regard vers Camille, pendant le choix d’une réplique |
| assise_parle_face.png | Prise de parole adressée à Camille, bouche entrouverte et geste explicatif |
| assise_parle_autre.png | Échange mère-fille, orientation vers l’autre personnage |
| assise_hesite_face.png | Réflexion ou difficulté exprimée, en couleur, sans coder une rupture d’alliance |
| debout_ecoute_face.png | Écoute dans le couloir, regard vers Camille |
| debout_parle_face.png | Réponse dans le couloir, bouche entrouverte et geste explicatif |
| debout_marche.png | Pose de déplacement vers la droite, pour les transitions |

Il s’agit de poses fixes séparées, et non de cycles de marche animés. Le futur code pourra accompagner les déplacements par un changement de décor et un mouvement discret du calque.

## Articulation avec le premier pack

Les poses V2 en couleur complètent les états V1 : `ouverte`, `enthousiaste`, `reservee` et `fermee`. Les réactions négatives immédiates continueront à utiliser les personnages V1 en noir et blanc. Le retour à une zone de choix pourra employer les nouveaux regards de face en couleur. La mémoire de l’alliance restera gérée séparément dans le moteur.

Les bulles de dialogue ne sont pas incrustées dans les images. Elles seront ajoutées en HTML lors de la reprise du code, pour rester lisibles, adaptables et accessibles.

## Préparation de la prochaine version du jeu

| Moment du scénario | Ressources à privilégier |
|---|---|
| Accueil et choix de répliques | Décor V1 salle d’attente et poses assises `ecoute_face` |
| Réponses de Khloé ou d’Élise | `parle_face` pour la personne qui s’exprime, écoute pour l’autre |
| Marche vers la salle | Couloir V1 et poses `debout_marche` |
| Arrivée devant la porte | `bg_corridor_porte` et poses debout d’écoute |
| Ouverture et entrée | `bg_consultation_seuil`, puis décor V1 salle d’entretien |
| Échange sur vélo et lacets | Poses assises de parole, orientation vers l’autre et hésitation |
| Réaction au choix du professionnel | Expressions V1, dont les réactions en noir et blanc |
| Nouvelle zone de choix | Poses d’écoute en couleur, regard vers Camille |
| Conclusion et départ | `bg_corridor_sortie`, poses debout puis marche |

## Fichiers techniques du complément

- `apercu-ajouts-v2.html` : catalogue local, à ouvrir après extraction du ZIP. Il fonctionne avec les seules images du complément.
- `manifest-ajouts-v2.json` : inventaire des 17 nouvelles images, dimensions et transparence.
- `generation-prompts-v2.json` : consignes de création des visuels.
- Ce mode d’emploi.

Les personnages mesurent 1024 × 1536 px, les décors 1672 × 941 px. Les PNG conservent leur transparence et leurs marges. Ne pas recadrer automatiquement les fichiers : les marges aident à stabiliser les ancrages.

Les poses générées présentent de légères variations de contour et de cadrage, à régler lors de la mise en scène du jeu. L’aperçu permet de les examiner, mais ne constitue pas une intégration dans Rise. Le code du jeu et le scénario n’ont pas été modifiés dans cette livraison.
