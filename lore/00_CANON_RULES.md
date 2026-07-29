---
id: doc_canon_rules
type: rules
status: canon
version: 1
reliability: objective
tags:
- meta
- canon
- rules
---

# Règles de canon

## Objet
Ce fichier gouverne l'ensemble du corpus narratif de TrisProject. Tout agent (humain ou IA) travaillant sur le lore doit le lire avant toute production. En cas de doute, ce fichier prime.

## Hiérarchie des sources
1. Règles de canon (ce fichier).
2. Informations explicitement imposées par le créateur du projet.
3. Fiches canoniques validées (`status: canon`).
4. Chronologie validée (`04_TIMELINE.md`).
5. Textes narratifs validés.
6. Rumeurs et documents subjectifs (`truth_status` autre que `objective`).
7. Brouillons (`status: draft`).
8. Suggestions générées par IA non intégrées aux fichiers.

## Statuts documentaires
- `canon` : information imposée par le créateur ou explicitement validée par lui.
- `draft` : proposition non validée. Utilisable comme hypothèse de travail, jamais comme vérité définitive.
- `hypothesis` : interprétation ou déduction non explicitement établie par une source.
- `contradiction` : versions incompatibles nécessitant un arbitrage.
- `unresolved` : question ouverte ou information incomplète nécessitant une décision.
- `resolved` : question ou contradiction ayant reçu une décision explicite.
- `deprecated` : ancien élément abandonné.

Convention interne : `> Statut : canon` ou `> Statut : draft` en tête de chaque section importante.

## Portée des statuts

Le **statut du fichier** indique le niveau de validation de sa fonction générale ou de l'existence documentaire de la fiche.

Le **statut de section** indique le niveau de validation du contenu précis d'une section.

Le **statut d'entité** indique le niveau de validation d'un personnage, lieu, événement, ordre, symbole ou autre élément décrit.

Un fichier globalement `canon` peut donc contenir des fondations canoniques, des développements `draft`, des `hypothesis`, des `contradiction` et des `unresolved`. Le statut global du fichier ne canonise jamais automatiquement tout son contenu.

## Fait objectif et texte subjectif
Le statut documentaire décrit le niveau de validation d’un document, d’une section ou d’un élément. Le champ truth_status décrit le rapport du contenu à la vérité objective du monde. Ces deux notions sont indépendantes.

Les valeurs autorisées de `truth_status` sont :
- `objective` : le contenu est présenté par le corpus comme une réalité objective du monde.
- `subjective` : le contenu exprime un point de vue, une perception ou un jugement interne au monde.
- `propaganda` : le contenu est produit pour influencer une population ou défendre les intérêts d’une faction, d’une institution ou d’un personnage.
- `rumor` : le contenu circule comme une rumeur et sa véracité n’est pas établie.
- `partially_true` : le contenu associe des faits exacts à des omissions, déformations ou conclusions trompeuses.
- `false` : le contenu est objectivement faux dans le monde, même si certains personnages le croient.
- `unknown` : le corpus ne permet pas encore de déterminer la vérité objective.
- `disputed` : plusieurs sources internes donnent des versions incompatibles sans qu’une vérité objective soit établie.

Principes :
- un document `canon` peut contenir une rumeur, de la propagande, une croyance subjective ou une affirmation fausse ;
- une proposition non validée reste `draft`, quel que soit son `truth_status` ;
- une rumeur reconnue comme existant dans le monde utilise par exemple `status: canon` et `truth_status: rumor` ;
- `rumor` n’est pas un statut documentaire.

## Procédure de validation
1. Toute nouvelle proposition naît en `draft`.
2. Seul le créateur du projet peut promouvoir un `draft` en `canon`, par validation explicite.
3. Lors d'une promotion, incrémenter `version` et reporter le terme au glossaire.

## Traitement des contradictions
1. Ne pas trancher arbitrairement.
2. Conserver l'information canonique en l'état.
3. Signaler la contradiction dans le rapport de travail.
4. Consigner dans `31_OPEN_QUESTIONS.md`.

## Règles anti-prolifération
- Exactement 3 divinités humaines majeures (Mahra, Mitra, Mola). Aucune quatrième.
- Exactement 3 dieux noirs (Azura, Atara, Mazda). Aucun quatrième.
- Exactement 13 grandes villes humaines, chacune gouvernée par un duc.
- Un seul roi nain reconnu par tous les nains.
- Avant de créer une faction, un lieu, un ordre ou une guilde : vérifier dans `06_FACTIONS_INDEX.md`. La réutilisation prime sur la création.

## Règles de nommage
- Identifiants techniques : anglais, minuscules, `snake_case`, uniques, stables.
- Noms narratifs : français, prononçables, sans apostrophes internes. Voir `28_NAMING_CONVENTIONS.md`.

## Interdits permanents
- Ne jamais remplacer la dynastie impériale par une autre.
- Le nom propre officiel de la capitale est **Tris**. « la cité impériale » reste une désignation fonctionnelle ou descriptive.
- Ne jamais remplacer la balance comme symbole principal de la famille impériale.
- Ne jamais modifier la succession du mythe de Mitra : argile, puis pierre, puis lumière.
- Ne jamais prononcer couramment le nom de Mazda dans les textes fictifs.
- Ne jamais reprendre d'élément protégé de Warhammer, D&D, HeroQuest ou Baldur's Gate.

## Rappel du canon imposé (résumé de référence)

> Statut : canon

- Année actuelle : 2609. La même famille règne depuis 2 609 ans.
- Empereur actuel : Alexandre III. Sa divinité privilégiée est Mitra.
- Blason impérial : une balance parfaitement équilibrée.
- Capitale : **Tris**, la cité impériale — ville concentrique : basse-cour extérieure, douves, un grand pont, six quartiers, château central à haute tour en spirale.
- Treize grandes villes humaines, chacune gouvernée par un duc.
- Guerres en cours : **orques et gobelins au sud**, au-delà des Monts-Ferrés ; **morts-vivants et nécromanciens à l'est** ; **renégats au nord** ; escarmouches d'elfes marginaux depuis les forêts.
- L'Empire est officiellement neutre envers elfes et nains.
- Les elfes et les nains se détestent (haine ancienne et sérieuse). Les deux peuples combattent les mêmes ennemis que l'Empire.
- Les nains vivent dans les montagnes du sud, entre l'Empire et les orques ; ils reconnaissent un roi unique au tempérament explosif et vénèrent des statues.
- Dieux humains : Mahra (amour, eau), Mitra (lumière, connaissances, sagesse), Mola (guerre, feu).
- Dieux noirs : Azura (tromperies), Atara (plaisirs), Mazda (nom imprononcé).
- La majorité des renégats a abandonné les dieux humains ; seule une minorité adore les dieux noirs.
- L'armée impériale est très organisée et hiérarchisée ; Alexandre III dispose d'escadrons d'élite ; certains soldats d'élite sont de terrifiants fanatiques de Mola.
- Des ordres de mages liés à Mitra. La magie est rare, difficile, dangereuse et surveillée.
- Les guildes de mercenaires sont rattachées à l'Empire ; les guildes de voleurs aux renégats.
- Jeux d'arène et banquets organisés par les ducs et à Tris, la cité impériale.
- Les villages sont actifs, importants pour l'économie, et régulièrement attaqués en zone frontière.
