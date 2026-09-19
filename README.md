# All zone PMDO project

Cartes ground pour **PMDO 0.8.12** (Guilde Treehouse PMD), livrées en calques PNG séparés, jour + nuit,
avec spécification écrite avant génération, scripts de build/audit et aperçus HTML autonomes.

| Lot | Contenu | État |
|---|---|---|
| `col_eboulis_v1/` | « Le col des Éboulis » — chemin sud → nord vers l'entrée canonique de Mont Horn, 640×640, 10 calques × jour/nuit, audit 16/16 PASS | livré |
| `beachsky_v1/` | Zone Beach/Sky étendue en calques avec eau animée (palette cycling) | références réunies, à produire |

Règles : générateur = guide de composition et textures inventées en DA PMD pour les zones indépendantes ; jamais de tuiles
générées présentées comme canoniques ; dimensions divisibles par 8, alpha propre, noms de fichiers uniques ; nuit = filtre Abyss
exact ; aucun test moteur revendiqué (voir `col_eboulis_v1/README.md`).

Rebuild d'un lot : `python3 build.py && python3 verify.py && python3 package.py` (Pillow, numpy, scipy).
