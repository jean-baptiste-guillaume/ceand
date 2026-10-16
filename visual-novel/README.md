# Visuels du visual novel Khloé et Élise

Pack V1 — 16 octobre 2026. Direction graphique validée : décors matte painting chaleureux, personnages de bande dessinée européenne et retrait relationnel représenté en noir et blanc dessiné.

## Contenu

- 3 décors PNG sans personnages : salle d’attente, salle d’entretien et couloir.
- 16 personnages PNG sur fond transparent : Khloé et Élise, assises ou debout, dans quatre états chacune.
- `index.html` : catalogue et aperçu interactif des combinaisons de visuels. Ouvrir ce fichier après extraction complète du ZIP, en conservant l’arborescence.
- `ui/visual-novel.css` : styles de la scène, du bandeau ivoire et des boutons bleus. Le texte et les contrôles restent en HTML pour la lisibilité, le clavier et l’adaptation au mobile.
- `manifest.json` : inventaire, dimensions et correspondance des états.
- `generation-prompts.json` : consignes de génération et de déclinaison.

## Correspondance avec le scénario

| État du scénario | Suffixe du fichier | Traitement |
|---|---|---|
| Pensive plus | `ouverte` | Couleur, attention posée |
| Enthousiaste | `enthousiaste` | Couleur, sourire plus marqué |
| Pensive moins | `reservee` | Noir et blanc, réserve |
| Boude ou colère | `fermee` | Noir et blanc, fermeture |

Les réactions restent des conventions de la simulation. L’expression d’un visage ne prouve pas à elle seule un accord réel.

## Dépôt Git

Copier tout le dossier `visual_novel_assets_v1` dans le dépôt en conservant les noms. Les noms de ressources sont sans espace ni accent. Les liens de contenu doivent viser les fichiers bruts ou les fichiers servis par le site, pas les pages GitHub contenant `/blob/`.

Le jeu pourra utiliser une seule racine d’URL : `BASE_URL + "assets/characters/khloe_assise_fermee.png"`. Ne pas renommer les fichiers après intégration sans modifier les références.

Les PNG sont les originaux générés, sans compression destructive, avec leur transparence conservée. Les personnages font 1024 × 1536 px ; les décors font 1672 × 941 px. Le pack d’images représente environ 35 Mio. Charger les images au fil des scènes et précharger les états de la scène suivante plutôt que les 19 images à chaque lancement.

## Composition

Le décor est le premier calque ; les personnages sont superposés séparément. Les poses assises n’intègrent pas de fauteuil : les sièges figurent dans les décors. Le couloir utilise les poses debout. Les cinq fins se composent avec les mêmes ressources, selon les états des deux personnages.

Les positions CSS fournies sont une première mise en scène, à ajuster avec le moteur définitif et son cadrage. Les variantes générées comportent de petites différences de contour et de placement : utiliser un fondu court entre les états plutôt qu’un morphing. Ne pas rogner automatiquement les marges transparentes, qui participent à l’ancrage.

Le catalogue n’est pas le jeu final : aucun score, embranchement ni achèvement Rise n’y est implémenté. Les boutons de démonstration montrent uniquement les réactions visuelles. Aucun son, logo, police distante ou service externe n’est nécessaire pour consulter le pack.
