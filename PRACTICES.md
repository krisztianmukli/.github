# Project Lifecycle and Practices

## Background

We have several open source repositories, and that number likely won’t be
getting smaller with time. Currently, most of these repositories aren’t large,
but the sum total of them can amount to a lot of work just to “keep the lights
on”. Some repository are just a rudimentary skeleton of an idea, while others
may require more care to to remain in good condition over time.

The goal of this document is to establish how we will manage the lifecycle of
these repositories and ensure that this lifecycle management is made clear to
anyone who interacts with them.

### Contents

- [Responsibility of the teams](#busts_in_silhouette-responsibility-of-the-teams)
- [Repository states](#bar_chart-repository-states)
    - [How repositories move from state to state](#chart_with_upwards_trend-how-repositories-move-from-state-to-state)
    - [Petitioning to unarchive a repository](#recycle-petitioning-to-unarchive-a-repository)
- [Issue triage](#mag-issue-triage)
    - [Issue triage general practices](#bug-issue-triage-general-practices)
    - [Issue triage practices with respect to repository states](#white_check_mark-issue-triage-practices-with-respect-to repository-states)
    - [We reserve the right to close issues](#negative_squared_cross_mark-we-reserve-the-right-to-close-issues)
- [Pull request triage](#repeat-pull-request-triage)
    - [Pull request triage general practices](#twisted_rightwards_arrows-pull-request-triage-general-practices)
    - [Handling new features and larger pull requests](#love_letter-handling-new-features-and-larger-pull requests)
    - [Acceptance criteria](#ok-acceptance-criteria)
    - [Acceptance criteria based on the kind of pull request](#capital_abcd-acceptance-criteria-based-on-the-kind-of-pull-request)
    - [Pull request triage practices with respect to repository states](#heavy_check_mark-pull-request-triage-practices-with-respect-to-repository-states)
    - [We reserve the right to deny a contribution](#negative_squared_cross_mark-we-reserve-the-right-to-deny-a-contribution)
- [Release cadence](#date-release-cadence)
- [Support policy for unsupported versions of languages and frameworks](#put_litter_in_its_place-support-policy-for-unsupported-versions-of-languages-and-frameworks)
- [Community health files](#beer-community-health-files)
- [Automation](#robot-automation)
- [Credits](#black_nib-credits)

## :busts_in_silhouette: Responsibility of the teams

Before diving into the rest of this document, it’s worth noting that the
lifecycle and practices of a given repository are ultimately at the discretion
of the team who owns that repository. There may be circumstances unique to one
teams’ repository that do not hold for another team’s repository. The contents
of this document are not hard and fast rules that every team strictly adheres to
for every single repository.

That being said, most repositories will follow the guidance in this document.

## :bar_chart: Repository states

We define a few states for a repository:

1. **Experimental:** The repository may or may not be under active development.
Software compiled from the repository is likely to be of limited use, but may
not be compiled at all. These are typically early-stage projects or code starts,
which can be suspended or closed at any time and reopened when we see fit. For
such repositories, there may be no support at all, assistance or documentation.

1. **Actively developed:** Regular development activity in the repository is
ongoing, such as adding new features or bugfixing existing features. During this
time, changes may occur that affect compatibility with previous versions. Some
repositories may be under active development for a longer period of time, others
may appear to be abandoned for a longer period of time, but still have planned
improvements later on and be in active use.

1. **Maintained:** The repository is considered stable and complete, no new
features are planned, but bug fixes and dependencies are still being maintained.
Security patches and changes that may be necessary to update dependencies are
welcome for these repositories, but to introduce new features we recommend you
can fork the repository.

1. **Archived:**  It is no longer possible to interact with this repository. It
is archived with GitHub’s archival tool. There is zero activity of any sort.
This state can be reached from virtually any previous state of a repository, so
there is no guarantee that it contains any usable code or compilable finished
product, and if it does, the build is likely to be out of date, security or
otherwise not recommended for use.

### :chart_with_upwards_trend: How repositories move from state to state

If a repository is **Experimental**, then the state it ultimately moves into
will be determined by the result of the experiment being done. As such, it is
highly recommended that nobody depend on anything marked as Experimental.

When a repository reaches the **actively developed** stage, it usually already
has one or more usable releases (not necessarily up to version 1.0.0) and
maintained and relevant documentation. However, it should be acknowledged that
at any time there may be a significant impact on or break the operation of the
system.

The code and its releases in a **maintained** repository are generally stable,
if not ready for a finished product, but no major changes to the functionality,
no new major features and no code structure changes are planned. Such a
repository may not receive any new changes or commits for a long time, but
usually as long as the code base is compilable with up-to-date operating
systems, runtimes and development tools, we do not archive and build on the
contents of the repository.

If an experimental repository eventually fails to produce a usable result, or an
actively developed and maintained project eventually becomes obsolete, or simply
no longer has any interest or system requirements to maintain a repository, then
**archive** it. Typically, an archived repository will remain archived forever;
it is very rare that a repository will revert back to the actively developed
stage due to a change in requirements.

### :recycle: Petitioning to unarchive a repository

There is no official process to petition to unarchive a repository. If you
depend on an artifact that the codebase produces, and need to change it, please
feel free to fork it and use as you see fit. Typically, requests to do some work
on a project that has already been already archived, will be rejected.

## :mag: Issue triage

In order to deal with problems effectively and consistently, we will define some
general practices that are specific to the state of the repository, but remember
that some repositories may have more specific practices that are only specific
to a particular project.

### :bug: Issue triage general practices

We will strive to have any new issue looked at by someone within *1 month* of
creation.

Repositories will have an issue template that helps set expectations for filing
an issue.

When an issue is looked at, it will:

* be appropriately labeled 
* request further information if it is necessary for understanding
* optionally rename the issue to improve searchability and automate the
  generation of release notes

We will try our best to be timely with any discussions on an issue.

If we ask for additional information, and don’t hear back within *2 months*, we
will close the issue:

* This will be done with a message explaining why we’re closing it
* We will mention that we are happy to re-open it if more information is
  provided

We are proactive in keeping our issue lists “clean”, especially since we may
track issues in a more central location (such as a public or private project
boards, kanban, todo.md, etc).

In general, for us to keep an issue open, it needs to meet one or more of the
following criteria:

* Has a minimal, self-contained reproduction OR be obviously incorrect behavior
* The problem described is unambiguous
* The issue is still relevant to the project and/or person who filed the issue
* The issue is a productive discussion about the repository/project (it may also
  be converted into a GitHub Discussion at the discretion of the team)

If these criteria are not met, we may close the issue as a part of regular issue
grooming.

Előfordulhat az is, hogy nagyon régi hibajegyeket zárunk le. Gyakran előfordul, 
hogy a régi hibák súlyossága és relevanciája idővel csökken, különösen, ha a 
szoftver érintett területe idővel jelentősen fejlődött. Ez nagy valószínűséggel 
egybeesik azzal a döntésünkkel, hogy leállítjuk egy adott funkció vagy 
funkcióterület támogatását. Kétféle régebbi lezárandó problémát különböztetünk 
meg:

* Olyan kérdések, amelyek egyszerűen csak régiek, és valószínűleg már nem 
relevánsak. Ha úgy érzed, hogy ez még fontos számodra, értesíts minket, és 
valószínűleg újra megnyitjuk. Mindenképpen együtt fogunk dolgozni veled egy 
olyan pull request beadásán, amely megoldja a problémát, amennyiben az 
technikailag lehetséges.
* Olyan problémák, amelyeket életkor, relevancia és fejlesztési döntés miatt 
zárunk be. Ebben az esetben WONTFIX címkét alkalmazunk, és nem nyitjuk meg újra 
a problémát, illetve nem fogadunk el olyan pull requestet, amely kijavítja azt. 
Ezt a lezárást a döntést magyarázó üzenet fogja kísérni.

### :white_check_mark: Issue triage practices with respect to repository states

A következő gyakorlatokat alkalmazzuk a tároló állapotával összefüggésben:

**Kísérleti**
* Semmilyen garancia nincs rá, hogy bármilyen beküldött problémát megvizsgálunk.

**Aktívan fejlesztett**
* Az általános gyakorlatot követjük minden benyújtott kérdésben.
* Néhány kérdést lezárhatunk, mert van olyan folyamatban lévő munka, amely 
elkerülhetővé teszi a felvetett problémát.

**Karbantartott**
* Az általános gyakorlatot követjük minden benyújtott kérdésben.
* Lezárhatunk egyes hibajegyeket, ha azokat nem gondoljuk kellőképpen fontosnak. 
Elsősorban a biztonsági hibák és komolyabb működési hibák javítása élvez 
elsőbbséget.

**Archivált**
* Nem lehetséges probléma beküldése.

### :negative_squared_cross_mark: We reserve the right to close issues

Nem minden kérdést van értelme nyitva tartani. Következzen néhány (de nem 
kizárólagos) ok, amiért lezárhatjuk a hibajegyet:

* A kérdéses hiba javítása eleve el van tervezve, még ha nem is nyilvánvaló 
azonnal, hogy ez miért van így.
* A kérdés egy másik kérdés duplikációja, még akkor is, ha ez nem nyilvánvaló 
azonnal, hogy miért van így.
* A beadott probléma jogos probléma, de stratégiai okokból nem fogjuk 
megoldani, és nem fogadunk el hozzájárulást a megoldásához.

Ha lezárunk egy problémát, akkor ezt tisztelettel és magyarázattal tesszük, 
hogy miért zártuk le, feltéve, hogy a probléma nem sérti az tároló magatartási 
kódexét, és egyértelműen volt benne némi erőfeszítés. Ha hajlandó vagy időt 
szánni arra, hogy átgondoltan küldj be egy problémát, akkor magyarázatot 
érdemelsz arra, hogy miért zártuk be.

## :repeat: Pull request triage

Hasonlóan a problémák kezeléséhez, nehéz lehet egyetlen szabályrendszert vagy 
gyakorlatot alkalmazni arra vonatkozóan, hogy hogyan kezeljük a tárolóinkhoz 
való hozzájárulásokat. A problémakezeléshez hasonló gyakorlatok vonatkoznak a 
pull requestek kezelésére is.

### :twisted_rightwards_arrows: Pull request triage general practices

Arra törekszünk, hogy minden új pull requestet a létrehozástól számított 1 
héten belül megvizsgáljon valaki az adott projektnél.

A tárolóknak van egy Pull Request sablonja, amely segít meghatározni a probléma 
benyújtásával kapcsolatos elvárásokat.

Amikor egy pull requestet megvizsgálunk, akkor:

* Megfelelően felcímkézzük (javítás, új funkció)
* Egyben vagy részlegesen átnézzük, esetleg felcímkézzük, hogy át fogjuk nézni
* Beolvasztjuk, ha átnéztük, átment a teszteken és mi is egyetértünk a 
beolvasztással
* Lehetséges, hogy módosítjuk, hogy kezeljük a beolvasztás során keletkező 
kódütközéseket
* Lehetséges, hogy további megjegyzésekkel és címkékkel látjuk el, hogy a 
beküldő értesüljön arról, ha konfliktusok miatt esetleg módosítania kell
* Hozzászólásokat tehetünk a pull request elfogadásához szükséges esetleges 
utómunkálatokhoz

Elkötelezzük magunkat amellett, hogy barátságosak és professzionálisak leszünk 
veled, amikor pull requestet nyújtasz be. Nagyra értékeljük, hogy jelentős 
személyes időt fordítottál arra, hogy elküldhesd nekünk, és mindent megteszünk, 
hogy ezt elismerjük a veled való interakciók során.

Ha további közreműködést kérünk (több információ, kódváltoztatás, teszt 
hozzáadásának szükségessége, stb.), és nem kapunk választ 1 hónapon belül, 
akkor:

* Ha elég értékes a munka, mi magunk is elvégezhetjük a módosítást
* Lezárhatjuk a pull requestet, ezt egy üzenettel fogjuk megtenni, amiben 
elmagyarázzuk, hogy miért zárjuk be. Szívesen megnyitjuk újra, amikor készen 
állsz a további közreműködésre.

A problémák kezeléséhez hasonlóan itt is proaktívan proaktívan törekszünk a 
pull request listák "tisztán tartására".

Előfordulhat, hogy kivételt teszünk az 1 hónapos irányelv alól, amennyiben 
folyamatban lévő más elfoglaltságaink éppen nem teszik lehetővé a 
közreműködésünket az adott projekten. Ez azért fordulhat elő, mert projektjeink 
jellemzően non-profit keretek között készülnek, és nem biztos, hogy minden 
időben rendelkezésre áll megfelelő emberi, technikai vagy egyéb feltétel.

### :love_letter: Handling new features and larger pull requests

Arra kérünk, hogy ne küldj be azonnal új funkciókat és/vagy nagyobb 
pull-requesteket anélkül, hogy a munkádhoz kapcsolódó elfogadott probléma lenne.

Új funkciók esetén, ha még nincs a funkció kérelemhez kapcsolódó probléma, 
először azt küldd be. A hibakezelés során rátérünk erre, és jóváhagyjuk vagy 
elutasítjuk a funkció kérelmet. Ha jóváhagytuk, nyugodtan folytasd a pull 
request benyújtásával.

Általában azt részesítjük előnyben, ha a hozzájárulások kis méretűek és 
inkrementális jellegűek. Ez megkönnyíti a dolgok átnézését, és így gyorsabban 
tudjuk a kód beolvasztását biztosítani.

Azonban felismertük, hogy nem minden hozzájárulás lehet kicsi, vagy nem lehet 
észszerűen feldarabolni. Nagyobb változtatások (pl. architektúrális 
változtatások) esetén arra kérünk, hogy nyiss egy hibajegyet amiben megbeszéled, 
hogy mit szeretnél csinálni és miért. Ez lehet egy már létező kérdés (például 
egy funkció kérés kérdése). A problémakezelésénél leírtak szerint fogunk veled 
foglalkozni.

Ha mindannyian egyetértünk abban, hogy a javaslatodnak van értelme, nyugodtan 
nyújtsd be a nagyobb pull requestet. Ha nem értünk egyet, arra kérünk, ne 
nyújtsd be pull requestet, mert azt le fogjuk zárni.

### :ok: Acceptance criteria

Ez a szakasz elég egyértelmű, általános elfogadási feltételeink a következőek:
* Minden teszt sikeres
* Minden kód a tárolóban található formázási konvencióknak megfelelően van 
formázva (ezt egy .editorconfig fájl automatizálhatja).
* A kód tulajdonosainak minden visszajelzését figyelembe vettük.

És ennyi! Van néhány további feltételünk a pull request típusától függően.

### :capital_abcd: Acceptance criteria based on the kind of pull request

**Hibajavítások**:
Kell legyen egy regressziós teszteset, amely bizonyítja, hogy a javítás 
kijavította a hibát, VAGY a javításnak kicsinek és nyilvánvalónak kell lennie. 
Ennek eldöntése ránk van bízva.

**Új funkciók vagy fejlesztések:**
A kódodnak rendelkeznie kell egy tesztesettel (vagy esetekkel), amely 
bizonyítja, hogy a kódod megoldja az esetlegesen felmerülő szélsőséges eseteket.
Ennek eldöntése belátásunk szerint történik.

**Teljesítményjavítás**:

Ha valami nyilvánvaló, például egy O(n^2) rutin O(n)-re való módosítása, akkor 
nincs szükség semmi másra. Általában ez már a kódodból is egyértelmű lesz.

Ha valami nem nyilvánvaló, akkor bizonyítani kell, hogy a pull request javítja a 
teljesítményt a teljesítmény bármely dimenziójában (CPU-idő, memóriaterhelés, 
falióra-idő stb.). A legtöbb nyelv rendelkezik valamilyen statisztikai 
benchmarking eszközzel, profilerrel vagy mással, ami segíthet ennek a 
bizonyítéknak a biztosításában.

Ha nem vagy biztos benne, hogyan tudod bizonyítani, hogy a változtatásod javítja 
a dolgokat, ne légy szégyenlős! Nyugodtan küldd el a PR-det, és kérdezd meg, 
hogy milyen bizonyítékot keresünk. Mindent megteszünk, hogy a legegyszerűbb 
módját javasoljuk annak, hogy megszerezzük, amire szükségünk van, és bizonyos 
körülmények között együtt dolgozunk veled, hogy a változtatásodat egyesítsük, ha 
nagyon nehéz bizonyítékot gyűjteni.

**Általános javítások (pl. README frissítése, CI furcsaságok, stb.)**:

Semmi különös, eltekintve a visszajelzések figyelembevételének biztosításától.

### :heavy_check_mark: Pull request triage practices with respect to repository states

Ezeken túlmenően meghatározunk néhány konkrét gyakorlatot az adott tároló 
állapotával összefüggésben.

**Kísérleti**

* Semmilyen garanciát nem vállalunk arra, hogy figyelembe vesszük a beküldött 
hozzájárulásokat.

**Aktívan fejlesztett**

* Megpróbáljuk követni az általános gyakorlatot a benyújtott hozzájárulások 
esetében.
* Egyes hozzájárulások lezárásra kerülhetnek, mert a csapat folyamatban lévő 
munkája szükségtelenné teszi vagy megismételné azt.

**Karbantartott**

* Az általános gyakorlatot követjük a benyújtott hozzájárulások esetében
* Valószínűleg nem fogadunk el nagyobb funkcióigényeket. A kisebb 
funkciókérések, különösen, ha a megvalósítás nem sok kódot tartalmaz, 
elfogadásra kerülhetnek. 

**Archivált**

* Hozzájárulás nem lehetséges.

### :negative_squared_cross_mark: We reserve the right to deny a contribution

Nem minden hozzájárulásnak van értelme a szóban forgó kódtároló számára. Ennek 
okai lehetnek többek között (de nem kizárólagosan):

* A kódtároló már csak karbantartott állapotban van.
* A változás túl nagy/bonyolult ahhoz, hogy hosszú távon fenntartsuk.
* A változtatás ellentmondana a tárolóból felépített könyvtár/eszköz/stb. 
céljainak.
* Nem tervezzük tovább fenntartani az tárolót, és szeretnénk a lehető 
legkisebbre csökkenteni a változást.

Általánosságban úgy gondoljuk, hogy a hozzájárulás elutasításának elkerülése 
érdekében a legjobb módja az, ha az elvárások egyértelműek. Különösen a (2) és 
(3) ponthoz hasonló okok miatt a mi feladatunk, hogy közöljük ezeket az 
árnyalatokat, hogy a hozzájárulók ne legyenek félrevezetve a tároló állapotát 
vagy az abból előállított szoftvereket illetően.

Amikor lezárunk egy pull requestet, ezt tisztelettel és magyarázattal tesszük, 
hogy miért zártuk le, feltéve, hogy a pull request nem sérti a kódtároló 
magatartási kódexét, és egyértelműen volt benne némi erőfeszítés. Ha hajlandó 
vagy időt szánni egy hozzájárulás átgondolt benyújtására, akkor magyarázatot 
érdemelsz arra, hogy miért zártuk le.

## :date: Release cadence

Az előző szakaszokhoz hasonlóan a kiadási gyakoriság az adott kódtároló 
állapotára és az azt kezelő csapat belátására van bízva. Egy nagy, 
folyamatosan fejlesztett kódtároló esetében a kiadásokat a többi nyílt forrású
komponenstől eltérő módon is ütemezhetjük.

Általánosságban elmondható, hogy rendszeres időközönként áttekintjük a 
beolvasztott pull-kérelmek listáját, amelyeket "to release" címkével láttunk el.
Ha vannak olyan figyelemre méltó fejlesztések, amelyek túlmutatnak a kisebb 
kódváltoztatásokon, akkor igyekszünk kiadni egy új verziót. 

A kiadásra vonatkozó durva kritériumaink a következők:

* A legutóbbi kiadás óta volt biztonsági javítás.
* A legutóbbi kiadás óta egy vagy több hibajavításra került sor.
* Az utolsó kiadás óta új funkciót adtunk hozzá.
* Az utolsó kiadás óta történt néhány jelentős frissítés a függőségekben (pl. ha
a frissítés teljesítménynöveléssel járt).
* Egy alapvető komponens függősége frissült, és ez fontos a komponens 
felhasználói számára.

Általánosságban elmondható, hogy nem adunk ki új verziót csak azért, mert van 
néhány kisebb függőségi frissítés. Semmi bajunk azzal, ha néhány hónapig nem 
adunk ki új verziót valamiből, ha semmi kritikus változás nem történt.

Továbbá, ha úgy érzed, hogy egy könyvtár új verzióját kellene kiadni, csak írj 
nekünk egy új GitHub hibajegyet. A kiadások néha megszakításokkal történhetnek, 
és ez rendben is van.

## :put_litter_in_its_place: Support policy for unsupported versions of languages and frameworks

Mivel több nyelvet és keretrendszert kell támogatnunk, nem szeretnénk, ha a 
régebbi verziók támogatására mennének el az erőforrásaink, ezért a következő 
szabályokat hoztuk:

* Ha egy nyelv vagy keretrendszer azon verziója, amelyre építünk, még mindig 
támogatott, akkor teljes mértékben támogatjuk a tárolóból előállított szoftvert.
* Ha egy nyelv vagy keretrendszer azon verziója, melyre építünk elavul, akkor 
azt a verziót már nem támogatjuk és a kódtároló is automatikusan elavultnak 
tekinthető, akkor is, ha **Aktívan fejlesztett** vagy **Karbantartott** 
állapotban van.
* Előfordulhat olyan időszak, amikor még mindig egy nem támogatott verzióra 
építünk. Kell lennie egy olyan hibajegynek, amely nyomon követi a támogatott 
verzióra való frissítést.

## :beer: Community health files

Minden **Aktívan fejlesztett**, valamint **Karbantartott** tárolónknak 
rendelkeznie kell a következő [közösségi fájlokkal](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file#supported-file-types)

* CODE_OF_CONDUCT.md
* CONTRIBUTING.md
* Issue és pull request sablonok
* SECURITY.md
* SUPPORT.md
* README.md
* LICENSE
* Egy `.editorconfig` fájl, ha alkalmazható, a kód formázásának szabványosítása 
érdekében.

Ezek szabványosítva lettek a tárolóinkban, de az egyes tárolókban ezek tartalma 
eltérhet egymástól.

Azoknak a tárolóknak, amelyek **Kísérleti** vagy **Archivált** állapotban 
vannak, nem biztos, hogy vannak ilyen fájljaik.

## :robot: Automation

Arra törekszünk, hogy a lehető legtöbb folyamatot automatizáljuk. Célunk, hogy a
legfontosabb dolgokra koncentráljunk, és hagyjuk, hogy a dolgok a maguk módján
áramoljanak, például a GitHub projektekbe. Ez magában foglalja a következőket:

* Dependabot engedélyezve a lehető legtöbb adattárban (automatikus címkézéssel).
* Különféle GitHub Actions, amelyek segítenek a kódtárolók ápolásában, ha 
szükséges, mint például a [Stale bot](https://github.com/actions/stale).
* Nyilvános projekt táblák esetében GitHub Actions, amelyek a témákat és 
PR-okat a megfelelő állapotokhoz társítják és mozgatják az adott táblában, de 
lehetnek privát táblák és tárolóhelyek is. 

## :black_nib: Credits

*Az ebben a dokumentumban szereplő kijelentések ötleteinek és kifejezéseinek 
nagy része a következő közösségek munkáján alapul, vagy azok inspirálták őket:*

* [Honeycomb OSS Lifecycle and Practices](https://github.com/honeycombio/home/blob/main/honeycomb-oss-lifecycle-and-practices.md)
