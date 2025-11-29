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

- Közreműködők Magatartási Kódexe: meghatározza a hozzájárulók elvárt 
viselkedését. - Közreműködési útmutató: útmutató a hozzájárulók számára, hogy 
tudnak részt venni a projektben. - Projektirányítási modell: a projekt 
irányítási modellje (szerepkörök, felelősségek, döntéshozatal). - Biztonsági 
házirend: útmutató a sebezhetőségek bejelentéséhez, valamint a támogatott 
verziók kezeléséhez. - Támogatás és Segítség: leírja, hol és hogyan kérhetsz 
segítséget és mit nem vállal a projekt.

## Milyen további sablonokat tárol?

- Hibajegyek sablonjai: megkülönböztetjük az alábbi hibalehetőségeket, a projekt 
nem fogad el más típusú hibajegyeket.
    - hibák
    - karbantartási javaslatok vagy hibák
    - dokumentációs javaslatok vagy hibák
    - funkciókérések
    - lokalizációs javaslatok vagy hibák
    - a projekt használatával kapcsolatos kérdések
    - refaktorálással kapcsolatos javaslatok
    
- Beolvasztási kérelem (Pull Request) sablon: megadja a beolvasztási kérelmek 
elfogadott formáját.
- `CODEOWNERS`: ez a fájl határozza meg, hogy mely fájlokért vagy könyvtárakért 
kik a felelősök a szervezet repóiban. A GitHub ezt a fájlt az alábbiakhoz 
használja:
    - Automatikusan bekéri a kijelölt kódtulajdonosok review-ját
    - Kényszeríthető, hogy a kódtulajdonos jóváhagyása nélkül ne lehessen 
merge-elni
    - Meghatározza, ki a felelős bizonyos komponensek vagy útvonalak 
karbantartásáért
- `FUNDING.yml`: ez fájl teszi lehetővé, hogy a GitHub felületén megjelenjenek a 
támogatási / szponzorációs linkek.
