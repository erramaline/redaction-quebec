---
name: redaction-quebec
description: |
  Applique les normes de rédaction du français québécois (OQLF) et humanise le texte en supprimant les patrons d'écriture IA. Couvre l'espacement de la ponctuation, l'écriture des nombres et symboles monétaires, les adjectifs ordinaux, les rectifications orthographiques de 1990, la rédaction épicène, les majuscules institutionnelles et la détection/réécriture de 23 patrons artificiels (mise en scène, triades forcées, inflation, gras décoratif, résidus de robot conversationnel, etc.). Utilise ce skill dès qu'un texte français est rédigé, corrigé, révisé, traduit, humanisé ou reformaté pour un public québécois ou canadien-français, ou dès que l'utilisateur mentionne le Québec, l'OQLF, la BDL, le GDT, la rédaction épicène, l'humanisation ou des « normes québécoises », même sans le mot Québec si le contexte est manifestement québécois.
---

# Rédaction Québec

Ce skill transforme un texte français pour qu'il respecte les normes institutionnelles de l'OQLF et qu'il sonne comme l'écriture d'un humain, pas d'un robot. Il corrige la typographie québécoise ET supprime les patrons d'écriture artificielle en une seule passe.

## Portée

Le skill couvre six axes. Les cinq premiers sont des normes OQLF objectives. Le sixième est l'humanisation du texte.

1. Espacement de la ponctuation
2. Écriture des nombres, symboles et monnaie
3. Rédaction épicène
4. Majuscules institutionnelles
5. Uniformité des rectifications orthographiques de 1990
6. Suppression des patrons d'écriture IA

Ne pas modifier le vocabulaire, la syntaxe ou le style au-delà de ces six axes. Garder chaque affirmation étayée. Ne jamais ajouter un fait, un nom, un chiffre, une date ou une citation absents de la source.

## Ordre de traitement (toujours dans cet ordre)

1. **Ponctuation haute** — retirer les espaces avant `; ! ?`, valider les guillemets, les deux-points et les points de suspension → voir `references/ponctuation.md`
2. **Données chiffrées** — repositionner les symboles monétaires, valider la virgule décimale, les espaces insécables et les ordinaux → voir `references/nombres-et-symboles.md`
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

## Méthode de travail pour l'humanisation

1. **Repérer.** Lire le texte en entier et marquer chaque patron, du plus fort au plus faible. Observer la forme des paragraphes autant que les phrases.
2. **Réécrire.** Garder chaque affirmation étayée. On peut raccourcir, fusionner ou scinder des paragraphes, mais conserver l'information. Ne rien inventer.
3. **Vérifier.** Relire à voix haute. Chercher les cinq patrons qui survivent le plus souvent : un contraste pas-X-mais-Y, une chute d'une ligne, un tiret cadratin, une triade, une étiquette en gras. Vérifier qu'aucun fait n'a été ajouté ni perdu.
4. **Finaliser.** Énoncer chaque point naturellement. Varier la longueur des phrases. Puis repasser les étapes 1 à 5 (normes OQLF) sur le texte humanisé.

### Voix

Si l'utilisateur fournit un échantillon de son écriture, le lire d'abord et reproduire sa longueur de phrase, son vocabulaire, sa ponctuation, ses amorces et ses transitions. L'échantillon a priorité sur les patrons d'humanisation.

Sans échantillon, ajuster la voix au type de texte. Billets de blogue, essais et textes d'opinion : garder les réactions, l'incertitude, l'humour et les apartés. Textes de référence, techniques et juridiques : rester neutre et sobre.

## À ne jamais faire

- Point médian, tiret ou parenthèse pour fusionner féminin/masculin dans un texte suivi (`étudiant·e·s`, `directeur.trice`) — toujours reformuler en doublet complet ou tournure neutre.
- Pronoms ou néologismes neutres non binaires (`iel`, `illes`) : l'OQLF ne les reconnait pas.
- Mélanger graphie traditionnelle et graphie rectifiée de 1990 pour un même mot dans un même texte.
- Majuscule à un titre de fonction (« le premier ministre », jamais « le Premier Ministre »), même en s'adressant directement à la personne.
- Espace avant `;`, `!` ou `?` — contrairement à la norme française hexagonale.
- Ajouter un fait, un nom, un chiffre, une date ou une citation absents de la source lors de l'humanisation.
- Laisser des résidus de robot conversationnel (« J'espère que cela vous aide! », « Excellente question! »).
- Présenter une supposition comme un fait (« il a probablement grandi à… »).

## Exemple condensé

Entrée :
```
Excellente question! Le Premier Ministre a affirmé : « La mesure est jugée « prioritaire » par le comité » ! Le budget est de 1250.50$, soit 5% de plus, pour les étudiant·e·s. Ce n'est pas seulement une question de chiffres — c'est un moment charnière pour l'avenir de l'éducation. Voilà le véritable enjeu.
```

Sortie :
```
Le premier ministre a affirmé : « La mesure est jugée "prioritaire" par le comité »! Le budget est de 1 250,50 $, soit 5 % de plus, pour les étudiantes et étudiants. La hausse aura des conséquences directes sur le financement de l'éducation.
```

Corrections appliquées :
- §20 Résidu de robot : « Excellente question! » supprimé.
- OQLF ponctuation : espace retirée avant `!`, guillemets de 2e niveau corrigés.
- OQLF nombres : virgule décimale, espace insécable pour les milliers, `$` à droite.
- OQLF épicène : doublet complet au lieu du point médian.
- OQLF majuscules : « premier ministre » en minuscule.
- §1 Pas X mais Y : contraste « pas seulement… c'est » remplacé par l'affirmation directe.
- §8 Tiret cadratin : supprimé, phrase restructurée.
- §12 Importance gonflée : « moment charnière » remplacé par l'effet concret.
- §2 Chute d'une ligne : « Voilà le véritable enjeu. » supprimé (répétait le paragraphe).
