---
name: quebecois
description: |
  Révise et humanise un texte français pour qu'il respecte les normes de l'Office québécois de la langue française (OQLF) et qu'il sonne comme l'écriture d'un humain, pas d'un robot. En une seule passe, corrige l'espacement de la ponctuation, l'écriture des nombres et symboles monétaires, les espaces insécables réelles, les abréviations de civilité sans point (Mme, Dr vs M.), les ordinaux (2d/2de vs 2e), les rectifications orthographiques de 1990, la rédaction épicène, les majuscules institutionnelles, puis détecte 23 patrons d'écriture artificielle et applique 12 principes d'humanisation profonde (régularité structurelle, transitions scolaires, vocabulaire artificiellement soutenu, sur-explication, symétrie, dépolissage). Utilise ce skill dès qu'un texte français est rédigé, corrigé, révisé, traduit, humanisé ou reformaté pour un public québécois ou canadien-français, ou dès que l'utilisateur mentionne le Québec, l'OQLF, la BDL, le GDT, la rédaction épicène, l'humanisation ou des normes québécoises.
---

# Québécois

Un seul skill pour deux objectifs : rendre un texte français conforme aux normes institutionnelles de l'OQLF et le faire sonner comme l'écriture d'une personne réelle. Typographie québécoise et humanisation profonde en une seule passe.

## Portée

Le skill couvre six axes. Les cinq premiers sont des normes OQLF objectives. Le sixième est l'humanisation profonde du texte. Garder chaque affirmation étayée. Ne jamais ajouter un fait, un nom, un chiffre, une date ou une citation absents de la source.

L'humanisation autorise (et exige parfois) de modifier la structure des phrases, le vocabulaire, les transitions et l'architecture des paragraphes. Elle n'autorise jamais d'inventer du contenu, d'ajouter des opinions fictives ou d'introduire des fautes.

1. Espacement de la ponctuation
2. Écriture des nombres, symboles, monnaie et abréviations
3. Rédaction épicène
4. Majuscules institutionnelles
5. Uniformité des rectifications orthographiques de 1990
6. Humanisation profonde (23 patrons IA + 12 principes de voix humaine)

## Ordre de traitement (toujours dans cet ordre)

1. **Ponctuation haute** — retirer les espaces avant `; ! ?`, valider les guillemets, les deux-points et les points de suspension → voir `references/ponctuation.md`
2. **Données chiffrées et abréviations** — repositionner les symboles monétaires, valider la virgule décimale, insérer l'espace insécable réelle (U+00A0 en texte, entité HTML en Web), vérifier les ordinaux (`2d`/`2de` vs `2e`) et les abréviations (pas de point à `Mme`, `Dr`, `Me`; point à `M.`) → voir `references/nombres-et-symboles.md`
3. **Rédaction épicène** — remplacer points médians/parenthèses par une formulation neutre ou un doublet complet → voir `references/redaction-epicene.md`
4. **Majuscules institutionnelles** — minuscule aux titres de fonction, majuscule aux lois/unités administratives → voir `references/majuscules.md`
5. **Uniformité orthographique** — vérifier qu'aucun mot ne coexiste sous sa forme traditionnelle et sa forme rectifiée dans le même texte → voir `references/orthographe-1990.md`
6. **Humanisation mécanique** — repérer et réécrire les 23 patrons d'écriture IA (§1 à §23), en respectant les normes OQLF dans chaque réécriture → voir `references/humanisation.md`, partie A
7. **Humanisation profonde** — appliquer les 12 principes : casser la régularité, réduire les transitions, supprimer la sur-explication, ajuster le vocabulaire, vérifier la plausibilité humaine, dépolir le texte → voir `references/humanisation.md`, partie B

Les étapes 1 à 5 sont des corrections mécaniques. L'étape 6 est une réécriture mécanique de patrons. L'étape 7 est une réécriture profonde qui exige du jugement. En cas de conflit, les normes OQLF (étapes 1 à 5) ont toujours priorité.

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
| **Espace insécable** | Réelle U+00A0 ou entité HTML (`100 $`, `5 %`) | Espace ordinaire sécable |
| **Séparateur décimal** | Virgule : `12,5` | Point : `12.5` |
| **Milliers** | Espace insécable : `10 000` | Virgule ou point : `10,000` / `10.000` |
| **Symbole monétaire** | À droite avec insécable : `24,99 $` | À gauche ou collé : `$24.99` / `24.99$` |
| **Ordinaux** | `1er`, `1re`, `2d`/`2de` (série de deux), `2e` (série de trois+) | `1ere`, `1ère`, `2ème`, `2eme` |
| **Civilités sans point** | Dernière lettre conservée : `Mme`, `Dr`, `Me` | Calque anglais avec point : `Mme.`, `Dr.`, `Me.` |
| **Civilités avec point** | Coupure interne obligatoire : `M.`, `prof.`, `dir.` | Sans point : `M Tremblay` |

Consulte `references/nombres-et-symboles.md` pour les règles complètes et les contextes Web.

## Référence rapide — patrons d'écriture IA (couche mécanique)

Les 23 patrons sont classés du plus fort au plus faible. Les patrons §1 à §5 justifient une intervention dès la première occurrence. Les patrons marqués *faible seul* ont besoin de la compagnie d'autres patrons dans le même passage.

| Catégorie | Patrons |
|---|---|
| A. Mise en scène | §1 Pas X mais Y · §2 Chutes d'une ligne · §3 Sentences profondes · §4 Mise en scène avant le point · §5 Argumenter contre personne |
| B. Rythme mécanique | §6 Triades forcées · §7 Amorces répétées · §8 Tirets cadratins · §9 Qualificatifs empilés · §10 Voix passive |
| C. Inflation | §11 Mots surutilisés · §12 Importance gonflée · §13 Lien vague · §14 Cavaliers en -ant · §15 Langage publicitaire · §16 Autorité empruntée · §17 Éviter est/sont/a |
| D. Mise en forme | §18 Gras décoratif · §19 Titres décoratifs |
| E. Résidus | §20 Résidus de robot · §21 Clauses de non-responsabilité · §22 Titre répété · §23 Version précédente |

Consulte `references/humanisation.md`, partie A, pour la définition complète, les exemples avant/après et les exceptions.

## Référence rapide — humanisation profonde (12 principes)

Ces principes ciblent les causes de l'écriture artificielle plutôt que les symptômes. Un texte peut ne contenir aucun des 23 patrons ci-dessus et rester manifestement artificiel par sa régularité, ses transitions scolaires et son vocabulaire trop soutenu.

| # | Principe | En bref |
|---|---|---|
| 1 | Empreinte de voix | Analyser 10 dimensions (longueur des phrases, vocabulaire, connecteurs, etc.) avant de réécrire. Ne pas écrire en style académique générique par défaut. |
| 2 | Casser la régularité | Éviter que chaque paragraphe suive le même modèle (problème → explication → nuance → conclusion). L'irrégularité humaine n'est pas une alternance régulière. |
| 3 | Transitions génériques | Réduire « Cela dit… », « En effet… », « En ce sens… ». Supprimer les transitions qui n'ajoutent rien. |
| 4 | Conclusions mécaniques | Ne pas reformuler la thèse à la fin de chaque paragraphe. Ne pas élargir automatiquement l'enjeu. |
| 5 | Oppositions artificielles | Réduire les oppositions binaires systématiques (court terme/long terme, technologie/réglementation). |
| 6 | Triades artificielles | Ne pas regrouper les idées par trois uniquement pour la structure. |
| 7 | Vocabulaire soutenu | Préférer le mot spontané. Éviter l'accumulation de « enjeu », « dynamique », « levier », « incontournable ». |
| 8 | Voix personnelle fictive | Ne jamais ajouter « je pense », « à mon avis » artificiellement. |
| 9 | Répétitions naturelles | Conserver les répétitions cohérentes avec la voix de l'auteur. Ne pas varier le vocabulaire uniquement pour éviter une répétition. |
| 10 | Précision avant élégance | Préférer la formulation spontanée et précise à la formulation élégante. Ne pas embellir sans raison. |
| 11 | Sur-explication | Faire confiance au lecteur. Ne pas définir chaque concept avant de l'utiliser. Réduire le ton scolaire. |
| 12 | Plausibilité humaine | Relire : cette formulation est-elle naturelle? cette transition est-elle nécessaire? le raisonnement est-il trop parfaitement organisé? |

Consulte `references/humanisation.md`, partie B, pour la définition complète et les exemples.

## Méthode de travail (5 étapes)

1. **Corriger.** Lire le texte en entier. Appliquer les normes OQLF (étapes 1 à 5) sur le texte brut.
2. **Éliminer les patrons IA.** Marquer chaque patron (§1 à §23) du plus fort au plus faible. Réécrire les passages marqués.
3. **Humaniser en profondeur.** Appliquer les 12 principes. Casser la régularité, réduire les transitions, supprimer la sur-explication, ajuster le vocabulaire.
4. **Lecture critique.** Relire comme si le texte avait été écrit par son auteur sans assistance. Poser deux questions par paragraphe : « Est-ce qu'une personne réelle formulerait cette idée de cette manière? » et « Est-ce que cette phrase existe parce qu'elle apporte quelque chose, ou uniquement parce qu'elle permet une belle transition? »
5. **Dépolissage contrôlé.** Supprimer ce qui semble ajouté pour rendre le texte plus élégant ou plus complet. Le résultat doit être naturel et crédible plutôt que parfaitement lisse. Ne jamais introduire de fautes pour simuler une écriture humaine. Repasser les normes OQLF (étapes 1 à 5) sur le texte final.

### Voix

Si l'utilisateur fournit un échantillon de son écriture, l'analyser d'abord selon 10 dimensions : longueur de phrase, vocabulaire, formalité, utilisation du « je », connecteurs, amorces de paragraphe, degré de nuance, répétitions naturelles, densité des idées, manière de conclure. L'échantillon a priorité sur les 12 principes d'humanisation.

Sans échantillon, choisir une voix plausible pour le contexte. Billets de blogue, essais et textes d'opinion : garder les réactions, l'incertitude, l'humour et les apartés. Textes de référence, techniques et juridiques : rester neutre et sobre. Dans tous les cas, éviter le style académique excessivement poli, uniforme et démonstratif.

### Niveaux d'humanisation

- **Standard.** Correction des patrons IA et principes de base. Pas d'échantillon. Voix adaptée au type de texte.
- **Académique.** Travaux universitaires, rapports professionnels. Humain, rigoureux, personnel et crédible, mais jamais conversationnel. Ne pas écrire « je trouve ça intéressant » ou « en fait » pour faire humain.
- **Personnelle.** L'utilisateur fournit un ou plusieurs échantillons. Construire un profil de voix complet. Réécrire en conservant la formulation originale autant que possible.

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
- Ajouter « je pense », « à mon avis », « pour ma part » artificiellement pour faire humain.
- Introduire des fautes, des erreurs grammaticales ou de la mauvaise ponctuation pour simuler une écriture humaine.
- Promettre un résultat « 100 % humain » ou « indétectable par les détecteurs d'IA ».

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

## Exemple d'humanisation profonde

Entrée (texte sans patron IA flagrant, mais artificiellement régulier) :
```
La fidélisation des clients constitue un enjeu majeur pour les entreprises modernes. En effet, le concept de valeur client actualisée, ou CLV, rappelle que conserver un client existant coute généralement moins cher que d'en acquérir un nouveau. Cela dit, il ne suffit pas d'offrir un bon produit. Il faut également bâtir une relation de confiance durable.

De plus, la transparence joue un rôle fondamental dans cette dynamique. Les consommateurs d'aujourd'hui s'attendent à une communication honnête et à des pratiques éthiques. En ce sens, les entreprises qui investissent dans la transparence récoltent souvent les bénéfices d'une fidélité accrue.

En conclusion, la fidélisation repose sur trois piliers : la qualité du produit, la transparence et la confiance. Les organisations qui intègrent ces dimensions dans leur stratégie sont mieux positionnées pour prospérer à long terme.
```

Sortie :
```
Fidéliser coute moins cher qu'acquérir. La CLV le confirme, mais la plupart des entreprises le savent déjà sans nécessairement agir en conséquence.

Un bon produit ne suffit pas. Les clients veulent savoir comment l'entreprise fonctionne, pas seulement ce qu'elle vend. Ceux qui ont l'impression d'être traités honnêtement reviennent.

La fidélité se construit sur la durée. Elle dépend moins d'une stratégie formelle que d'habitudes cohérentes.
```

Principes appliqués :
- Principe 2 : architecture des paragraphes variée (le 1er est court et direct, le 2e développe, le 3e conclut différemment).
- Principe 3 : transitions « En effet », « Cela dit », « De plus », « En ce sens », « En conclusion » supprimées.
- Principe 4 : conclusion mécanique (« repose sur trois piliers ») remplacée par une affirmation simple.
- Principe 6 : triade « qualité, transparence, confiance » cassée.
- Principe 7 : « enjeu majeur », « dynamique », « fondamental », « dimensions » remplacés par des mots simples.
- Principe 10 : formulations plus directes et moins académiques.
- Principe 11 : définition scolaire de la CLV condensée (le lecteur connait le concept).
