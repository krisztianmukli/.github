🇬🇧 [en](GOVERNANCE.md) | 🇭🇺 [hu](GOVERNANCE.hu.md)

# Projektirányítási modell

Ez a dokumentum határozza meg a projekt irányítási struktúráját és a 
döntéshozatal folyamatát. Célja, hogy átlátható módon rögzítse, kik jogosultak 
fenntartani, irányítani és végső döntést hozni a kódtároló és az ahhoz 
kapcsolódó projekt működéséről.

## 🎩 Vezetési modell: BDFL + Code Owners

A projekt vezetési modellje a **[BDFL (Benevolent Dictator For 
Life)](https://en.wikipedia.org/wiki/Benevolent_dictator_for_life)** szemléleten 
alapul. Ez azt jelenti, hogy a projekt végső irányítása és a végső 
döntéshozatali jog:

1. **a kódtároló tulajdonosánál**, és  
2. **a CODEOWNERS fájlban meghatározott kódtulajdonosoknál**

van.

Ezek együtt alkotják a projekt "mindenkori BDFL-jeit".

A BDFL-ek jogosultak:

- a projekt stratégiai irányát meghatározni,
- pull requesteket jóváhagyni vagy elutasítani,
- kiadásokat ütemezni,
- a projekt állapotát (kísérleti, aktív, karbantartott, archivált) meghatározni,
- a hozzájárulási és működési irányelveket felülbírálni,
- vitás kérdésekben végleges döntést hozni.

Ha a CODEOWNERS fájl csak a tároló tulajdonosát tartalmazza, akkor ő az egyetlen 
BDFL.

## 👥 Fenntartók és közreműködők

A projektbe történő hozzájárulás mindenki számára nyitott a **[Közreműködési 
útmutatóban](CONTRIBUTING.hu.md)**leírt feltételek szerint.

A fenntartók (maintainerek):

- áttekintik és címkézik a hibajegyeket,
- átnézik a pull requesteket,
- javaslatokat tesznek technikai megoldásokra,
- biztosítják a kódminőséget,
- betartják a **[Közreműködők Magatartási Kódexének](CODE_OF_CONDUCT.hu.md)** előírásait.

Döntéseik a projekt BDFL-jeinek felügyelete alá tartoznak.  Ha vita merül fel, a 
BDFL döntése **végleges**.

## 🧭 Döntéshozatali folyamat

A projekt döntéshozatala a **szelíd konszenzus** és a **best-effort** 
együttműködés elvén működik.

1. **Nyilvános egyeztetés**  – Hibajegyekben, Pull Requestekben vagy Discussions 
témákban.

2. **Fenntartói javaslat**  – A maintainer(ek) javaslatot tesznek a megoldásra.

3. **Döntés**  
   – Konszenzus esetén: a maintainer beolvasztja vagy lezárja.  
   – Nézeteltérés esetén: a BDFL-ek döntenek.

4. **Felelős kommunikáció**  
   – A döntést mindig tiszteletteljes és egyértelmű magyarázattal közöljük.

## 🗂 A projekt állapota és életciklusa

A projekt életciklusára a **[Projekt életciklusok és gyakorlatok 
útmutatója](PRACTICES.hu.md)** dokumentumban meghatározott állapotok és 
szabályok vonatkoznak:

- Kísérleti  
- Aktívan fejlesztett  
- Karbantartott  
- Archivált  

A projekt aktuális állapotát a BDFL-ek határozzák meg.

## 🔄 A Projektirányítási struktúra módosítása

A dokumentum módosítása:

- pull request formájában kezdeményezhető,
- a CODEOWNERS által jelölt kódtulajdonosok felülvizsgálatát igényli,
- **csak a BDFL-ek jóváhagyásával** lép hatályba.
