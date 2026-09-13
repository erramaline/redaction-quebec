---
name: redaction-quebec
description: Applique les normes de rédaction du français québécois définies par l'Office québécois de la langue française (OQLF) — espacement de la ponctuation, écriture des nombres et symboles monétaires, adjectifs ordinaux, rectifications orthographiques de 1990, rédaction épicène et majuscules institutionnelles. Utilise ce skill dès qu'un texte français est rédigé, corrigé, révisé, traduit ou reformaté pour un public québécois ou canadien-français, ou dès que l'utilisateur mentionne le Québec, l'OQLF, la BDL, le GDT, la rédaction épicène ou des « normes québécoises », même sans le mot Québec si le contexte (organisme, adresse, client) est manifestement québécois.
---

# Rédaction Québec

Ce skill transforme un texte français pour qu'il respecte les normes institutionnelles de l'OQLF, distinctes par endroits de la norme typographique française hexagonale.

## Portée
Le français québécois partage sa grammaire et son lexique avec le français international. Il ne s'en distingue que sur cinq points précis : l'espacement de la ponctuation, l'écriture des nombres/symboles, l'uniformité des rectifications orthographiques de 1990, la rédaction épicène, et la majusculation institutionnelle. Ne touche à rien d'autre — ne pas modifier le vocabulaire, la syntaxe ou le style au-delà de ces cinq axes.

## Ordre de traitement (toujours dans cet ordre)
1. **Ponctuation haute** — retirer les espaces avant `; ! ?` → voir `references/ponctuation.md`
2. **Données chiffrées** — repositionner les symboles monétaires, valider la virgule décimale et les espaces insécables → voir `references/nombres-et-symboles.md`
3. **Rédaction épicène** — remplacer points médians/parenthèses par une formulation neutre ou un doublet complet → voir `references/redaction-epicene.md`
4. **Majuscules institutionnelles** — minuscule aux titres de fonction, majuscule aux lois/unités administratives → voir `references/majuscules.md`
5. **Uniformité orthographique** — vérifier qu'aucun mot ne coexiste sous sa forme traditionnelle et sa forme rectifiée de 1990 dans le même texte → voir `references/orthographe-1990.md`

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

## À ne jamais faire
- Point médian, tiret ou parenthèse pour fusionner féminin/masculin dans un texte suivi (`étudiant·e·s`, `directeur.trice`) — toujours reformuler en doublet complet ou tournure neutre.
- Pronoms ou néologismes neutres non binaires (`iel`, `illes`) : l'OQLF ne les reconnaît pas.
- Mélanger graphie traditionnelle et graphie rectifiée de 1990 pour un même mot dans un même texte.
- Majuscule à un titre de fonction (« le premier ministre », jamais « le Premier Ministre »), même en s'adressant directement à la personne.

## Exemple condensé
Entrée : `Le Premier Ministre a affirmé : « La mesure est jugée « prioritaire » par le comité » ! Le budget est de 1250.50$, soit 5% de plus, pour les étudiant·e·s.`

Sortie : `Le premier ministre a affirmé : « La mesure est jugée "prioritaire" par le comité »! Le budget est de 1 250,50 $, soit 5 % de plus, pour les étudiantes et étudiants.`
