# redaction-quebec

**Skill Claude pour le français québécois** — normes OQLF et humanisation du texte en une seule passe.

---

## Ce que fait ce skill

`redaction-quebec` prend un texte français et le transforme pour qu'il respecte les normes institutionnelles de l'Office québécois de la langue française (OQLF) **et** qu'il sonne comme l'écriture d'un humain, pas d'un modèle de langue. Il corrige la typographie québécoise et supprime les patrons d'écriture artificielle dans un ordre précis.

### Les six axes de traitement

| # | Axe | Ce qu'il fait | Référence |
|---|---|---|---|
| 1 | **Ponctuation** | Retire les espaces avant `;` `!` `?`, valide les guillemets et les deux-points | [`ponctuation.md`](references/ponctuation.md) |
| 2 | **Nombres et symboles** | Virgule décimale, `$` à droite, espace insécable pour les milliers et les unités | [`nombres-et-symboles.md`](references/nombres-et-symboles.md) |
| 3 | **Rédaction épicène** | Doublets complets ou tournures neutres au lieu du point médian | [`redaction-epicene.md`](references/redaction-epicene.md) |
| 4 | **Majuscules** | Minuscule aux titres de fonction, majuscule aux lois et unités administratives | [`majuscules.md`](references/majuscules.md) |
| 5 | **Orthographe 1990** | Uniformité des rectifications pour chaque mot dans un même texte | [`orthographe-1990.md`](references/orthographe-1990.md) |
| 6 | **Humanisation** | 23 patrons d'écriture IA repérés et réécrits, de la mise en scène aux résidus de robot | [`humanisation.md`](references/humanisation.md) |

Les axes 1 à 5 sont des corrections mécaniques fondées sur des normes objectives. L'axe 6 est une réécriture qui exige du jugement. En cas de conflit, les normes OQLF ont toujours priorité.

---

## Exemple rapide

**Entrée :**
> Excellente question! Le Premier Ministre a affirmé : « La mesure est jugée « prioritaire » par le comité » ! Le budget est de 1250.50$, soit 5% de plus, pour les étudiant·e·s. Ce n'est pas seulement une question de chiffres — c'est un moment charnière. Voilà le véritable enjeu.

**Sortie :**
> Le premier ministre a affirmé : « La mesure est jugée "prioritaire" par le comité »! Le budget est de 1 250,50 $, soit 5 % de plus, pour les étudiantes et étudiants. La hausse aura des conséquences directes sur le financement de l'éducation.

**Corrections appliquées :** résidu de robot supprimé, ponctuation corrigée (espace avant `!`, guillemets de 2e niveau), virgule décimale, `$` repositionné, doublet épicène, majuscule du titre de fonction corrigée, contraste pas-X-mais-Y supprimé, tiret cadratin retiré, « moment charnière » remplacé par l'effet concret, chute d'une ligne supprimée.

---

## Différences clés avec la norme française hexagonale

| Règle | Québec (OQLF) | France |
|---|---|---|
| Espace avant `;` `!` `?` | **Aucune** | Espace fine insécable |
| Symbole monétaire `$` | Après le nombre (`100 $`) | Avant le nombre dans certaines conventions |
| Citations enchâssées | Guillemets anglais `" "` | Guillemets français emboîtés `« « » »` |
| Écriture inclusive | Doublets complets uniquement | Point médian toléré |
| Titres de fonction | **Toujours minuscule** | Majuscule de courtoisie parfois admise |

---

## Structure du dépôt

```
redaction-quebec/
├── SKILL.md                           Déclenchement, algorithme et référence rapide
├── references/
│   ├── ponctuation.md                 Espacement de la ponctuation (norme OQLF)
│   ├── nombres-et-symboles.md         Nombres, monnaie, ordinaux (norme OQLF)
│   ├── redaction-epicene.md           Rédaction épicène (norme OQLF)
│   ├── majuscules.md                  Majuscules institutionnelles (norme OQLF)
│   ├── orthographe-1990.md            Rectifications orthographiques (norme OQLF)
│   └── humanisation.md               23 patrons d'écriture IA (adapté au français QC)
├── evals/
│   └── evals.json                     13 cas de test (6 OQLF + 7 humanisation)
└── README.md
```

---

## Sources

- **Normes typographiques et linguistiques :** Office québécois de la langue française (OQLF), Banque de dépannage linguistique (BDL), Grand dictionnaire terminologique (GDT).
- **Patrons d'écriture IA :** Adaptés de la page Wikipédia [Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing), maintenue par le WikiProject AI Cleanup.

---

## Licence

MIT
