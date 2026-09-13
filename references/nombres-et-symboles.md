# Nombres, symboles, monnaie, ordinaux et abréviations (norme OQLF)

## Séparateur décimal
Virgule uniquement (`12,5`). Le point décimal est un anglicisme typographique à toujours corriger.

## Séparateur de milliers
Espace insécable (U+00A0) par tranches de trois chiffres, pour les entiers comme pour les décimaux : `12 535,75`. Jamais de point ni de virgule comme séparateur de milliers.

## Symbole monétaire ($)
Toujours à droite du nombre, précédé d'une espace insécable : `100 $`, `24,99 $`. Jamais `$100` ni `100$`.

## Unités de mesure, pourcentage, température
Espace insécable entre le chiffre et le symbole : `25 kg`, `8,5 %`, `25 °C`.

## Espaces insécables réelles en sortie (Web / Code / Texte)
Dans certains environnements de saisie ou lors de la publication Web, une espace classique risque de rejeter un symbole monétaire (`$`), un pourcentage (`%`) ou une abréviation en début de ligne suivante :
- **Texte enrichi / Markdown / Prose :** Utiliser le véritable caractère Unicode d'espace insécable `\u00A0` (NBSP).
- **Web / HTML / CMS :** Employer l'entité HTML `&nbsp;` (`100&nbsp;$`, `5&nbsp;%`, `1&nbsp;250&nbsp;000&nbsp;$`, `M.&nbsp;Tremblay`).

## Adjectifs numéraux ordinaux
Abréviation en exposant préférée ; ligne de base tolérée si l'exposant est techniquement impossible.

| Terme | Conforme | Formes proscrites |
|---|---|---|
| Premier / Première | 1er / 1re | 1ere, 1ère, 1er. |
| Premiers / Premières | 1ers / 1res | 1eres, 1ères |
| Second / Seconde | 2d / 2de | 2ème, 2eme |
| Deuxième | 2e | 2ème, 2eme, 2è |
| Troisième | 3e | 3ème, 3ieme, 3è |
| Vingtième / siècle | 20e / XXe | 20ème, XXème |

### Nuance entre 2d / 2de (second / seconde) et 2e (deuxième)
- **`2d` / `2de` (second / seconde) :** S'emploie rigoureusement lorsqu'il n'y a que deux éléments dans un ensemble ou une série fermée (ex. : *la Seconde Guerre mondiale*, *le second tour du scrutin*, *la seconde période*).
- **`2e` (deuxième) :** S'emploie lorsqu'il y a un troisième élément ou lorsque la série est ouverte (ex. : *le deuxième tome d'une trilogie*, *la 2e édition d'un festival*).
- **Recommandation OQLF :** Bien que l'usage moderne admette `2e` dans tous les cas, maintenir `2d` / `2de` lorsqu'il n'y a que deux éléments enrichit la précision et l'élégance du texte.

Note : les dates s'écrivent toujours au masculin (`le 1er mai`, jamais `la 1re mai`).

## Abréviations de civilité et règle du point abréviatif

L'OQLF applique une règle stricte et logique concernant le point abréviatif :

1. **Pas de point abréviatif si la dernière lettre est conservée :**
   Si la dernière lettre de l'abréviation est la même que la dernière lettre du mot complet, on ne met **aucun point abréviatif** :
   - `Mme` (Madame — se termine par *e*)
   - `Mlle` / `Mlles` (Mademoiselle — se termine par *e*)
   - `Dr` / `Drs` (Docteur — se termine par *r*)
   - `Me` / `Mes` (Maître, juriste — se termine par *e*)
   - `Bd` (Boulevard — se termine par *d*)
   *Formes proscrites fréquentes générées par les IA (calques de l'anglais Mrs., Dr.) :* `Mme.`, `Dr.`, `Me.`, `Bd.`.

2. **Point abréviatif obligatoire si la coupure est interne :**
   Si l'abréviation est coupée avant la dernière lettre du mot, le point abréviatif est **obligatoire** :
   - `M.` (Monsieur — coupé à *M*, ne se termine pas par le *r* final)
   - `MM.` (Messieurs)
   - `prof.` (professeur)
   - `dir.` (directeur)
   - `av.` (avenue)
   - `vol.` (volume)
   - `p.` (page)
