---
name: quebecois
description: |
  Révise et humanise un texte français pour qu'il respecte les normes de l'Office québécois de la langue française (OQLF) et qu'il sonne comme l'écriture d'un humain, pas d'un robot. En une seule passe, corrige l'espacement de la ponctuation, l'écriture des nombres et symboles monétaires, les espaces insécables réelles, les abréviations de civilité sans point (Mme, Dr vs M.), les ordinaux (2d/2de vs 2e), les rectifications orthographiques de 1990, la rédaction épicène, les majuscules institutionnelles, et détecte puis réécrit 23 patrons d'écriture artificielle (mise en scène, triades, inflation, gras décoratif, résidus de robot conversationnel, etc.). Utilise ce skill dès qu'un texte français est rédigé, corrigé, révisé, traduit, humanisé ou reformaté pour un public québécois ou canadien-français, ou dès que l'utilisateur mentionne le Québec, l'OQLF, la BDL, le GDT, la rédaction épicène, l'humanisation ou des normes québécoises.
---

# Québécois

Un seul skill pour deux objectifs : rendre un texte français conforme aux normes institutionnelles de l'OQLF et le faire sonner comme l'écriture d'un humain. Typographie québécoise et humanisation en une seule passe.

## Portée

Le skill couvre six axes. Les cinq premiers sont des normes OQLF objectives. Le sixième est l'humanisation du texte. Ne pas modifier le vocabulaire, la syntaxe ou le style au-delà de ces six axes. Garder chaque affirmation étayée. Ne jamais ajouter un fait, un nom, un chiffre, une date ou une citation absents de la source.

1. Espacement de la ponctuation
2. Écriture des nombres, symboles, monnaie et abréviations
3. Rédaction épicène
4. Majuscules institutionnelles
5. Uniformité des rectifications orthographiques de 1990
6. Suppression des patrons d'écriture IA

## Ordre de traitement (toujours dans cet ordre)

1. **Ponctuation haute** — retirer les espaces avant `; ! ?`, valider les guillemets, les deux-points et les points de suspension → voir `references/ponctuation.md`
2. **Données chiffrées et abréviations** — repositionner les symboles monétaires, valider la virgule décimale, insérer l'espace insécable réelle (U+00A0 en texte, entité HTML en Web), vérifier les ordinaux (`2d`/`2de` vs `2e`) et les abréviations (pas de point à `Mme`, `Dr`, `Me`; point à `M.`) → voir `references/nombres-et-symboles.md`
3. **Rédaction épicène** — remplacer points médians/parenthèses par une formulation neutre ou un doublet complet → voir `references/redaction-epicene.md`
4. **Majuscules institutionnelles** — minuscule aux titres de fonction, majuscule aux lois/unités administratives → voir `references/majuscules.md`
5. **Uniformité orthographique** — vérifier qu'aucun mot ne coexiste sous sa forme traditionnelle et sa forme rectifiée dans le même texte → voir `references/orthographe-1990.md`
6. **Humanisation** — repérer et réécrire les patrons d'écriture IA (§1 à §23), en respectant les normes OQLF dans chaque réécriture → voir `references/humanisation.md`

Les étapes 1 à 5 sont des corrections mécaniques. L'étape 6 est une réécriture qui exige du jugement. En cas de conflit, les normes OQLF (étapes 1 à 5) ont toujours priorité sur l'humanisation.

## Référence rapide — espacement de la ponctuation

| Signe | Avant | Après | Exemple |
|---|---|---|---|
| `:` | insécable (aucune si le Web ne la garantit pas) | sécable | Rapport : analyse |
| `;` | aucune | sécable | Étape terminée; suivant. |
| `?` | aucune | sécable | Quelle est la décision? |
| `!` | aucune | sécable | Attention au changement! |
| `« »` | sécable avant `«` / insécable après | insécable avant `»` / sécable après | Il a dit : « le projet continue ». |
| `" "` (citation enchâssée) | collé au texte | collé au texte | « le comité juge cela "urgent" » |
| `...` | aucune | sécable | Plusieurs options sont possibles... |

Consulte `references/ponctuation.md` pour les cas particuliers (heures, jonctions de signes adjacents, contextes Web restreints).

## Référence rapide — nombres, symboles et abréviations

| Élément | Norme OQLF | Forme à corriger |
|---|---|---|
| **Espace insécable** | Réelle `\u00A0` ou entité `&nbsp;` (`100 $`, `5 %`) | Espace ordinaire sécable |
| **Séparateur décimal** | Virgule : `12,5` | Point : `12.5` |
| **Milliers** | Espace insécable : `10 000` | Virgule ou point : `10,000` / `10.000` |
| **Symbole monétaire** | À droite avec insécable : `24,99 $` | À gauche ou collé : `$24.99` / `24.99$` |
| **Ordinaux** | `1er`, `1re`, `2d`/`2de` (série de deux), `2e` (série de trois+) | `1ere`, `1ère`, `2ème`, `2eme` |
| **Civilités sans point** | Dernière lettre conservée : `Mme`, `Dr`, `Me` | Calque anglais avec point : `Mme.`, `Dr.`, `Me.` |
| **Civilités avec point** | Coupure interne obligatoire : `M.`, `prof.`, `dir.` | Sans point : `M Tremblay` |

Consulte `references/nombres-et-symboles.md` pour les règles complètes et les contextes Web.

## Référence rapide — patrons d'écriture IA

Les 23 patrons sont classés du plus fort au plus faible. Les patrons §1 à §5 justifient une intervention dès la première occurrence. Les patrons marqués *faible seul* ont besoin de la compagnie d'autres patrons dans le même passage.

| Catégorie | Patrons |
|---|---|
| A. Mise en scène | §1 Pas X mais Y · §2 Chutes d'une ligne · §3 Sentences profondes · §4 Mise en scène avant le point · §5 Argumenter contre personne |
| B. Rythme mécanique | §6 Triades forcées · §7 Amorces répétées · §8 Tirets cadratins · §9 Qualificatifs empilés · §10 Voix passive |
| C. Inflation | §11 Mots surutilisés · §12 Importance gonflée · §13 Lien vague · §14 Cavaliers en -ant · §15 Langage publicitaire · §16 Autorité empruntée · §17 Éviter est/sont/a |
| D. Mise en forme | §18 Gras décoratif · §19 Titres décoratifs |
| E. Résidus | §20 Résidus de robot · §21 Clauses de non-responsabilité · §22 Titre répété · §23 Version précédente |

Consulte `references/humanisation.md` pour la définition complète, les exemples avant/après et la méthode de travail.

## Méthode de travail

1. **Repérer.** Lire le texte en entier. Corriger d'abord la ponctuation, les nombres, les abréviations, l'épicène, les majuscules et l'orthographe (étapes 1 à 5). Puis marquer chaque patron d'écriture IA, du plus fort au plus faible.
2. **Réécrire.** Garder chaque affirmation étayée. On peut raccourcir, fusionner ou scinder des paragraphes, mais conserver l'information. Ne rien inventer.
3. **Vérifier.** Relire à voix haute. Chercher les cinq patrons qui survivent le plus souvent : un contraste pas-X-mais-Y, une chute d'une ligne, un tiret cadratin, une triade, une étiquette en gras. Vérifier qu'aucun fait n'a été ajouté ni perdu. Repasser les étapes 1 à 5 sur le texte humanisé.
4. **Finaliser.** Énoncer chaque point naturellement. Varier la longueur des phrases.

### Voix

Si l'utilisateur fournit un échantillon de son écriture, le lire d'abord et reproduire sa longueur de phrase, son vocabulaire, sa ponctuation, ses amorces et ses transitions. L'échantillon a priorité sur les patrons d'humanisation.

Sans échantillon, ajuster la voix au type de texte. Billets de blogue, essais et textes d'opinion : garder les réactions, l'incertitude, l'humour et les apartés. Textes de référence, techniques et juridiques : rester neutre et sobre.

## À ne jamais faire

- Point médian, tiret ou parenthèse pour fusionner féminin/masculin (`étudiant·e·s`, `directeur.trice`).
- Pronoms ou néologismes neutres non binaires (`iel`, `illes`) : l'OQLF ne les reconnait pas.
- Mélanger graphie traditionnelle et graphie rectifiée de 1990 pour un même mot dans un même texte.
- Majuscule à un titre de fonction (« le premier ministre », jamais « le Premier Ministre »).
- Espace avant `;`, `!` ou `?`.
- Point abréviatif aux abréviations conservant la dernière lettre (`Mme.`, `Dr.`, `Me.` proscrits au lieu de `Mme`, `Dr`, `Me`).
- Omettre le point abréviatif aux coupures internes (`M.` obligatoire, jamais `M Tremblay`).
- Ajouter un fait, un nom, un chiffre ou une citation absents de la source.
- Laisser des résidus de robot conversationnel (« J'espère que cela vous aide! »).
- Présenter une supposition comme un fait (« il a probablement grandi à… »).

## Exemple condensé

Entrée :
```
Excellente question! Mme. la Directrice a affirmé que le Dr. Roy rencontrera M Tremblay pour la 2ème fois : « La mesure est « prioritaire » ! » Le budget est de 1250.50$, soit 5% de plus, pour les étudiant·e·s. Ce n'est pas seulement une question de chiffres — c'est un moment charnière. Voilà le véritable enjeu.
```

Sortie :
```
La directrice a affirmé que le Dr Roy rencontrera M. Tremblay pour la 2e fois : « La mesure est "prioritaire"! » Le budget est de 1 250,50 $, soit 5 % de plus, pour les étudiantes et étudiants. La hausse aura des conséquences directes sur le financement.
```

Corrections appliquées :
- §20 Résidu de robot : « Excellente question! » supprimé.
- Abréviations OQLF : `Mme.` → `Mme` (sans point), `Dr.` → `Dr` (sans point), `M ` → `M.` (point obligatoire).
- Ordinal OQLF : `2ème` corrigé en `2e`.
- Ponctuation OQLF : espace retirée avant `!`, guillemets de 2e niveau corrigés en `" "`.
- Nombres OQLF : virgule décimale, espace insécable pour les milliers, `$` à droite avec espace insécable.
- Épicène OQLF : doublet complet au lieu du point médian.
- Majuscules OQLF : « directrice » en minuscule.
- §1 Pas X mais Y : contraste « pas seulement… c'est » remplacé par l'affirmation directe.
- §8 Tiret cadratin : supprimé, phrase restructurée.
- §12 Importance gonflée : « moment charnière » remplacé par l'effet concret.
- §2 Chute d'une ligne : « Voilà le véritable enjeu. » supprimé.
