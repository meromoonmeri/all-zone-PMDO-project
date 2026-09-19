## Col des Éboulis — entrée « Mont Horn » en calques, chemin sud → nord (19 septembre 2026)

Demande initiale : nouvelle entrée de donjon indépendante, biome montagne/pic, jour + nuit. Deux corrections
successives : (1) « ne pas changer les textures, seulement le layout : chemin sud → nord, montagnes de chaque côté »
— les essais C/D/E ont dérivé vers la texture de Steam Cave (cônes bruns) : **écartés** ; (2) consigne finale :
« **reprends Mont Horn**, fais en plusieurs layers le chemin vers l’entrée canonique de Mont Horn, **de face**, chemin
sud vers nord, avec l’altitude : **en contrebas, des chaînes de montagne au loin**, élabore plusieurs layers ».

Livraison : `renders/col_eboulis_v1/` (bruts, 20 calques `COLEBOULIS_V1_<JOUR|NUIT>_NN_*.png` 640×640, scènes),
`source/col_eboulis_v1/` (spec écrite avant génération, build/verify/package), aperçu racine `apercu_col_eboulis_v1.html`.
Méthode : composition H générée avec Mont Horn comme seule référence image → éléments régénérés à l’identique sur
magenta (massif+bords+rebords, chaîne proche, chaîne lointaine, feuille de rochers) + plaque de sol plein cadre →
détourage → 10 calques (ciel/nuages natifs, deux chaînes, sol masqué au plateau, ombres calculées, massif, vide de la
bouche, rochers instanciés hors corridor, rebords Top) → nuit par le filtre Abyss exact. 16 contrôles PASS.

Règles confirmées : le générateur s’ancre sur la référence de layout **texture comprise** — pour changer le layout en
gardant une texture, ne donner **que** la référence de texture en image et décrire le layout en texte. La méthode
« même scène avec sol/ciel en magenta » reproduit fidèlement les textures et donne des calques propres. Réduction
*nearest* 1024 → 640 admise pour les générations, jamais pour des tuiles natives. Pas de test moteur (code 139) ;
aucune collision ni destination fournie. La sandbox a été réinitialisée en cours de session (dépôt tronqué à ~126 Mo) :
le lot est autonome et léger ; ne pas garder le clone complet du dépôt dans `/home/user`.
