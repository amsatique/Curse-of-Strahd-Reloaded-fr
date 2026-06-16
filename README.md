# Brief : traduction de la campagne (EN → FR)

Ce repo contient le guide d'une campagne D&D 5e (édition 2024), *Curse of Strahd Reloaded*, structuré pour Obsidian. La version originale anglaise est dans `/en`, et l'objectif est de produire une traduction française complète dans `/fr`, fichier par fichier, en conservant exactement la même arborescence et les mêmes noms de fichiers.

## Consignes de traduction

- **Traduction intégrale, jamais de résumé.** Chaque ligne, paragraphe, encadré (callout), tableau et bloc de statistiques doit être traduit en entier. Ne saute aucune section, même longue ou répétitive.
- **Les noms propres restent tels quels** : noms de personnages (Strahd, Ireena, Arabelle, Van Richten...), de lieux (Vallaki, Barovia, Krezk, Argynvostholt, Wachterhaus...), de groupes (Vistani...), titres d'objets/œuvres en italique (*Sunsword* → *Épée du Soleil* seulement si une trad. officielle existe — sinon garder l'anglais), etc. En cas de doute, garder l'anglais.
- **Terminologie D&D 5e (2024) officielle en français** : utiliser le vocabulaire des manuels officiels (voir liste de référence ci-dessous), pas une traduction libre.
- **Conversion impérial → métrique** : convertir les unités de distance (pieds, miles) en mètres/km comme le font les manuels français (voir table ci-dessous).
- **Liens wiki `[[...]]`** :
  - Lien vers un fichier non encore traduit → garder la cible anglaise originale (`[[Arc J - The Stolen Gem]]`).
  - Lien interne vers un titre (heading) **du même fichier** → traduire la cible pour qu'elle corresponde au nouveau titre français (`[[#E8b. Following Rictavio]]` → `[[#E8b. Suivre Rictavio]]`).
- **Conserver toute la structure HTML/Markdown Obsidian** : `![[embeds d'images]]`, frontmatter, `<div class="description">`, `<table class="ability-table">`, `<span class="citation">`, `<span class="credit">`, callouts (`> [!info]+`, `> [!warning]+`, `> [!lore]+`, `> [!profile]+`, `> [!abstract]+`, `> [!combat]-`, `> [!item]+`, `> [!design]-`, etc.). Ne pas en ajouter, ni en retirer (attention au tag fantôme `</content>` parfois généré par erreur en fin de fichier — toujours vérifier et le supprimer si présent).

## Méthode de travail (validée, à respecter)

Pour les fichiers longs (500+ lignes), traduire **par sections** afin d'éviter de dépasser la limite de tokens en sortie :
1. Lire le fichier source anglais en entier (par chunks de lecture si nécessaire).
2. Écrire le fichier français avec l'outil Write pour le premier morceau.
3. Poursuivre avec des appels Edit successifs, chacun ancré sur la fin du texte déjà traduit (`old_string` = dernière ligne traduite), pour ajouter la suite section par section.
4. Une fois le fichier terminé, vérifier : nombre de lignes cohérent avec l'original, absence de tag `</content>` parasite, cohérence des liens internes traduits.

## Terminologie de référence (déjà utilisée, à réutiliser pour la cohérence)

Classe d'armure, Points de vie, Vitesse, Facteur de puissance (FP), Bonus de maîtrise, Jets de sauvegarde, Compétences, Sens, Langues, Attaques multiples, Actions bonus, Réactions, Résistances/Vulnérabilités/Immunités aux dégâts, Immunités aux états, FOR/DEX/CON/INT/SAG/CHA, DD (Difficulté de Test), Jalon (Milestone), PX (points d'expérience).

## Conversions impérial → métrique

- 5 ft → 1,50 m
- 15 ft → 4,50 m
- 30 ft → 9 m
- 60 ft → 18 m
- 80 ft → 24 m
- 100 ft → 30 m
- 320 ft → 96 m
- one mile → un mile (généralement conservé tel quel dans le texte narratif, plutôt que converti en km, car cela sonne plus naturel en français)

## Priorités

1. **Acte II complet** (Arcs D à I, ainsi que le Résumé de l'Acte II) : terminé.
2. Le reste de la campagne, dans l'ordre suivant : Chapitres 1-3 restants → Acte I → Acte III → Acte IV → Annexes → `_other/templates/combat.md`.

## État d'avancement

Fichiers déjà traduits dans `/fr` :
- `Introduction/A DM's Guide to Curse of Strahd.md`
- `Introduction/Changelog.md`
- `Introduction/Using This Guide.md`
- `Chapter 1 - Beginning the Campaign/Character Creation.md`
- `Chapter 1 - Beginning the Campaign/Session Zero.md`
- `Act II - The Shadowed Town/Arc D - St. Andral's Feast.md`
- `Act II - The Shadowed Town/Arc E - The Missing Vistana.md`
- `Act II - The Shadowed Town/Arc F - Lady Wachter's Wish.md`
- `Act II - The Shadowed Town/Act II Summary.md`
- `Act II - The Shadowed Town/Arc G - The Strazni Siblings.md`
- `Act II - The Shadowed Town/Arc H - The Lost Soul.md`
- `Act II - The Shadowed Town/Arc I - The Walls of Krezk.md`
- `Chapter 2 - The Land of Barovia/History of Barovia.md`
- `Chapter 2 - The Land of Barovia/Lore of Barovia.md`
- `Chapter 2 - The Land of Barovia/Strahd von Zarovich.md`
- `Chapter 3 - Running the Game/Adventure Summary.md`
- `Chapter 3 - Running the Game/Running the Adventure.md`
- `Act I - Into the Mists/Act I Summary.md`
- `Act I - Into the Mists/Act I Plot Map.canvas`
- `Act I - Into the Mists/Arc A - Escape From Death House.md`
- `Act I - Into the Mists/Arc B - Welcome to Barovia.md`
- `Act I - Into the Mists/Arc C - Into the Valley.md`
- `Act III - The Broken Land/Act III Summary.md`
- `Act III - The Broken Land/Arc J - The Stolen Gem.md`
- `Act III - The Broken Land/Arc K - The Fallen Abbey.md`
- `Act III - The Broken Land/Arc L - The Den of Wolves.md`
- `Act III - The Broken Land/Arc M - The Dragon's Manor.md`
- `Act III - The Broken Land/Arc O - Dinner with the Devil.md`

Prochaine étape : comparer les arborescences `/en` et `/fr` pour identifier les fichiers restants (Chapitres 1-3 restants, Acte I, etc.) et continuer la traduction dans cet ordre.

Pour repérer rapidement ce qui reste à faire, comparer les arborescences `/en` et `/fr` (les fichiers absents de `/fr` restent à traduire).
