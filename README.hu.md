🇬🇧 [en](README.md) | 🇭🇺 [hu](README.hu.md)

# Github közösségi irányelvek

*Alapértelmezett [közösségi irányelvek](https://help.github.com/en/github/building-a-strong-community/creating-a-default-community-health-file) 
minden nyílt forráskodú projektemhez.*

Ez a repó határozza meg az **alapértelmezett közösségi irányelveket**, 
**hibajegy- és PR-sablonokat**, amelyeket a saját projektjeim összes kódtárolója 
automatikusan örököl, kivéve ha egy projekt saját irányelveket használ.

Célja, hogy minden projekt egységes szabványokkal és hozzájárulási folyamattal 
működjön.

## Milyen útmutatásokat tartalmaz?

- **[Közreműködők Magatartási Kódexe](CODE_OF_CONDUCT.hu.md)**: meghatározza a hozzájárulók elvárt 
viselkedését. 
- **[Közreműködési útmutató](CONTRIBUTION.hu.md)**: útmutató a hozzájárulók számára, hogy tudnak részt 
venni a projektben. 
- **[Projektirányítási modell](GOVERNANCE.hu.md)**: a projekt irányítási modellje (szerepkörök, 
felelősségek, döntéshozatal). 
- **[Biztonsági házirend](SECURITY.hu.md)**: útmutató a sebezhetőségek bejelentéséhez, valamint a 
támogatott verziók kezeléséhez. 
- **[Támogatás és Segítség](SUPPORT.hu.md)**: leírja, hol és hogyan kérhetsz segítséget és mit nem vállal a projekt.

## Milyen további sablonokat tárol?

- **Hibajegyek sablonjai**: megkülönböztetjük az alábbi hibalehetőségeket, a projekt 
[nem fogad el](.github/ISSUE_TEMPLATE/config.yml) más típusú hibajegyeket.
    - [hibák](.github/ISSUE_TEMPLATE/bug.yml)
    - [karbantartási javaslatok vagy hibák](.github/ISSUE_TEMPLATE/chore.yml)
    - [dokumentációs javaslatok vagy hibák](.github/ISSUE_TEMPLATE/documentation.yml)
    - [funkciókérések](.github/ISSUE_TEMPLATE/feature.yml)
    - [lokalizációs javaslatok vagy hibák](.github/ISSUE_TEMPLATE/localisation.yml)
    - [a projekt használatával kapcsolatos kérdések](.github/ISSUE_TEMPLATE/question.yml)
    - [refaktorálással kapcsolatos javaslatok](.github/ISSUE_TEMPLATE/refactoring.yml)
    
- **[Pull Request sablon](/.github/PULL_REQUEST_TEMPLATE.md)**: megadja a beolvasztási kérelmek 
elfogadott formáját.
- **[CODEOWNERS](.github/CODEOWNERS)**: ez a fájl határozza meg, hogy mely fájlokért vagy könyvtárakért 
kik a felelősök a szervezet repóiban. A GitHub ezt a fájlt az alábbiakhoz 
használja:
    - Automatikusan bekéri a kijelölt kódtulajdonosok review-ját
    - Kényszeríthető, hogy a kódtulajdonos jóváhagyása nélkül ne lehessen 
merge-elni
    - Meghatározza, ki a felelős bizonyos komponensek vagy útvonalak 
karbantartásáért
- **[FUNDING.yml](.github/FUNDING.yml)**: ez fájl teszi lehetővé, hogy a GitHub felületén megjelenjenek a 
támogatási / szponzorációs linkek.
