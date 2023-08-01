# Projekt életciklusok és gyakorlatok útmutatója

## Háttér

Számos nyílt forráskódú tárolóval rendelkezünk, és ezek száma valószínűleg nem
fog csökkeni az idő múlásával. A legtöbb tároló nem nagy, de összességükben sok
munkát jelenthetnek, csak hogy életben tartsuk őket. Néhány tároló csak kósza
ötletek kezdetleges vázai, míg mások nagyobb gondosságot igényelhetnek, hogy
idővel jó állapotban maradjanak.

Ennek a dokumentumnak az a célja, hogy megállapítsa, hogyan fogjuk kezelni
ezeknek a tárolóknak az életciklusát, és biztosítsa, hogy ez az
életciklus-kezelés egyértelmű legyen mindenki számára, aki kapcsolatba kerül
velük.

### Tartalom

- [A csapatok felelőssége](#busts_in_silhouette-a-csapatok-felelőssége)
- [Tárolók állapotai](#bar_chart-tárolók-állapotai)
- [Hogyan változik egy tároló állapota](#chart_with_upwards_trend-hogyan-változik-egy-tároló-állapota)
- [Az archiválás megszüntetésére irányuló kérelem](#recycle-az-archiválás-megszüntetésére-irányuló-kérelem)
- [Problémakezelés](#mag-problémakezelés)
- [A problémakezelés általános gyakorlata](#bug-a-problémakezelés-általános-gyakorlata)
- [Problémakezelési gyakorlatok a tároló állapota tekintetében](#white_check_mark-problémakezelési-gyakorlatok-a-tároló-állapota-tekintetében)
- [Fenntartjuk a jogot, hogy lezárjuk a kérdéseket](#negative_squared_cross_mark-fenntartjuk-a-jogot-hogy-lezárjuk-a-kérdéseket)
- [Hozzájárulások](#repeat-hozzájárulások)
- [Hozzájárulások általános kezelése](#twisted_rightwards_arrows-hozzájárulások-általános-kezelése)
- [Új funkciók és nagyobb pull requestek kezelése](#love_letter-új-funkciók-és-nagyobb-pull-requestek-kezelése)
- [Elfogadási feltételek](#ok-elfogadási-feltételek)
- [Elfogadási feltételek a pull request típusától függően](#capital_abcd-elfogadási-feltételek-a-pull-request-típusától-függően)
- [Hozzájárulások kezelése a tároló állapota tekintetében](#heavy_check_mark-hozzájárulások-kezelése-a-tároló-állapota-tekintetében)
- [Fenntartjuk a jogot, hogy nem fogadunk el egy hozzájárulást](#negative_squared_cross_mark-fenntartjuk-a-jogot-hogy-nem-fogadunk-el-egy hozzájárulást)
- [Kiadási gyakoriság](#date-kiadási-gyakoriság)
- [A nyelvek és keretrendszerek nem támogatott verzióinak szabályai](#put_litter_in_its_place-a-nyelvek-és-keretrendszerek-nem-támogatott-verzióinak-szabályai)
- [Közösségi fájlok](#beer-közösségi-fájlok)
- [Automatizálás](#robot-automatizálás)
- [Szerzők](#black_nib-szerzők)

## :busts_in_silhouette: A csapatok felelőssége

Mielőtt belemerülnénk a dokumentum további részébe, érdemes megjegyezni, hogy
egy adott tároló életciklusa és gyakorlatai végső soron az adott tárolót
birtokló csapat belátására vannak bízva. Előfordulhatnak olyan, az egyik csapat
tárolóhelyére jellemző körülmények, amelyek egy másik csapat tárolóhelyére nem
érvényesek. A jelen dokumentum tartalma nem olyan szigorúan betartandó szabály,
amelyet minden tárolónk esetén szigorúan betartunk.

Ennek ellenére a legtöbb tároló követi az ebben a dokumentumban szereplő
útmutatást.

## :bar_chart: Tárolók állapotai

A következő állapotokat határozzuk meg egy kódtárolóhoz:

1. **Kísérleti:** A tároló aktív fejlesztés alatt állhat, de az is lehet, hogy 
nem. A tárolóból fordított szoftverek valószínűleg csak korlátozottan 
használhatóak, de az is előfordulhat, hogy egyáltalán nem fordíthatóak le. Ezek 
jellemzően kezdeti fázisban lévő projektek vagy kódkezdemények, amelyeket 
bármikor félbehagyhatunk, vagy lezárhatunk, majd újra megnyithatunk, amikor azt 
jónak látjuk. Az ilyen tárolókhoz előfordulhat, hogy semmilyen támogatást, 
segítséget vagy dokumentációt nem tudunk nyújtani.

1. **Aktívan fejlesztett:** A tárolóban rendszeres fejlesztési tevékenység 
folyik, például új funkciók hozzáadása, vagy meglévő funkciók hibajavítása. Ez 
idő alatt előfordulhatnak olyan változások, amelyek hatással vannak a korábbi 
verziókkal való kompatibilitásra. Egyes tárolóknál előfordulhat, hogy hosszabb 
időre is aktív fejlesztés alatt állnak, másoknál lehetséges, hogy hosszabb 
időre magára hagyottnak tűnhetnek, de attól még később tervezett fejlesztések 
történhetnek benne és a tároló aktívan használatban van.

1. **Karbantartott:** A tároló stabilnak és teljesnek tekinthető, abba már új 
funkciók bevezetését nem tervezzük, azonban a meglévő funkciók hibajavítása és 
a függőségek karbantartása még mindig zajlik. Biztonsági javításokat és a 
függőségek frissítése miatt esetleg szükséges módosításokat szívesen fogadjuk 
ezekhez a tárolókhoz, de új funkciók bevezetéséhez a tároló forkolását szoktuk 
javasolni.

1. **Archivált:** Ebbe a tárolóba már nem lehet hozzájárulást küldeni, a GitHub 
archiválási eszközével archiváltuk. Nincs benne semmiféle aktivitás. Ebbe az 
állapotba juthat gyakorlatilag bármelyik korábbi állapotból egy tároló, tehát 
nem garantált, hogy egyáltalán használható kódot, vagy lefordítható kész 
terméket tartalmaz, ha mégis, az elkészült build valószínűleg elavult, 
biztonsági vagy egyéb szempontból nem javasolt a használata.

### :chart_with_upwards_trend: Hogyan változik egy tároló állapota

Ha egy tároló **kísérleti** akkor annak sorsa attól függ, hogy végül valami 
használható eredmény születik-e belőle vagy sem. Azt javasoljuk, hogy ne 
építsünk semmire, ami kísérleti tárolóban található.

Ha a tároló az **aktívan fejlesztett** stádiumba ér, akkor általában már van 
egy vagy több használható kiadása (ezek nem feltétlenül érik el az 1.0.0-s 
verziószámot) és van karbantartott és releváns dokumentációja. Ugyanakkor 
tudomásul kell venni, hogy bármikor a működést komolyan befolyásoló, vagy azt 
eltörő módosítást eszközölhetünk rajta.

Egy **karbantartott** tárolóban található kód és annak kiadásai már általában 
stabilak, ha nem is érik el egy késztermék állapotát, de a működésen, a főbb 
funkciókon és a kód felépítésében mélyreható változásokat már nem tervezünk 
benne. Egy ilyen tároló előfordulhat, hogy akár hosszú ideig sem kap új 
módosítást, vagy commitot, de általában amíg az adott kódbázis lefordítható 
naprakész operációs rendszerek, futtatókörnyezetek és fejlesztőeszközök 
segítségével, addig nem archiváljuk, és építhetünk a tároló tartalmára.

Ha egy kísérleti tároló végül nem vezet használható eredményre, vagy egy 
aktívan fejlesztett, illetve karbantartott projekt végül elavultá válik, vagy 
egyszerűen csak már semmilyen érdekünk vagy rendszerkövetelményünk nem követeli 
meg, hogy egy tárolót fenntartsunk, akkor **archiváljuk** azt. Egy archivált 
tároló jellemzően örökre archivált marad, nagyon ritka esetben fordulhat csak 
elő, hogy valamilyen követelményváltozás miatt egy tároló visszakerül a aktívan 
fejlesztett stádiumba.

### :recycle: Az archiválás megszüntetésére irányuló kérelem

Egy kódtároló archiválásának feloldására nincs meghatározott eljárás. Ha 
szükséged van egy archivált kódbázis által előállított szoftverre, akkor 
nyugodtan forkold el és használd úgy, ahogy jónak látod. Jellemzően az olyan 
kéréseket, amik arra vonatkoznak, hogy valamilyen munkát végezzünk el egy már 
archivált tárolónkon, vissza fogjuk utasítani.

## :mag: Problémakezelés

A problémák hatékony és következetes kezelésének céljából meghatározunk néhány 
általános és a tároló állapotára jellemző gyakorlatot, de ne feledjük, hogy 
egyes tárolóknak lehetnek olyan speciálisabb gyakorlatai, amelyek csak az 
adott projektre jellemzőek.

### :bug: A problémakezelés általános gyakorlata

Arra törekszünk, hogy minden új problémát a létrehozástól számított 1 hónapon 
belül megvizsgáljunk.

A tárolók rendelkeznek egy problémasablonnal, amely segít meghatározni a 
probléma bejelentésével kapcsolatos elvárásokat.

Ha egy kérdést megvizsgálunk, akkor azt:
* megfelelően felcímkézzük
* további információkat kérhetünk be, ha az szükséges a megértéshez
* opcionálisan átnevezhetjük a problémát a kereshetőség és a kiadási jegyzetek 
generálásának automatizálásának javítása érdekében

Igyekszünk minden tőlünk telhetőt megtenni annak érdekében, hogy a kérdéssel 
kapcsolatos megbeszéléseket időben lefolytassuk.

Ha további információkat kérünk, és 2 hónapon belül nem kapunk választ, 
lezárjuk a hibajegyet:

* Ezt egy üzenettel tesszük, amelyben elmagyarázzuk, hogy miért zárjuk le az 
ügyet.
* Megemlítjük, hogy szívesen megnyitjuk újra, ha további információk érkeznek.

Proaktívan törekszünk a problémalisták "tisztán tartására", különösen azért, 
mert adott esetben a problémákat más rendszereken keresztül is nyomon 
követhetjük (pl: privát projekttáblák, kanban, todo.md, stb.).

Általánosságban elmondható, hogy egy ügyet akkor tartunk nyitva, ha az megfelel 
az alábbi kritériumok közül egynek vagy többnek:

* A hiba önmagában reprodukálható, vagy nyilvánvalóan hibás viselkedés
* A problémaleírás egyértelmű
* A kérdés releváns a projekt és/vagy a kérdést benyújtó személy szempontjából
* A probléma egy produktív vita az tárolóról/projektről (a csapat döntése 
alapján GitHub Discussion-be is átalakítható).

Ha ezek a kritériumok nem teljesülnek, akkor a rendszeres problémakezelés 
részeként lezárhatjuk a problémát.

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

### :white_check_mark: Problémakezelési gyakorlatok a tároló állapota tekintetében

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

### :negative_squared_cross_mark: Fenntartjuk a jogot, hogy lezárjuk a kérdéseket

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

## :repeat: Hozzájárulások

Hasonlóan a problémák kezeléséhez, nehéz lehet egyetlen szabályrendszert vagy 
gyakorlatot alkalmazni arra vonatkozóan, hogy hogyan kezeljük a tárolóinkhoz 
való hozzájárulásokat. A problémakezeléshez hasonló gyakorlatok vonatkoznak a 
pull requestek kezelésére is.

### :twisted_rightwards_arrows: Hozzájárulások általános kezelése

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

### :love_letter: Új funkciók és nagyobb pull requestek kezelése

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

### :ok: Elfogadási feltételek

Ez a szakasz elég egyértelmű, általános elfogadási feltételeink a következőek:
* Minden teszt sikeres
* Minden kód a tárolóban található formázási konvencióknak megfelelően van 
formázva (ezt egy .editorconfig fájl automatizálhatja).
* A kód tulajdonosainak minden visszajelzését figyelembe vettük.

És ennyi! Van néhány további feltételünk a pull request típusától függően.

### :capital_abcd: Elfogadási feltételek a pull request típusától függően

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

### :heavy_check_mark: Hozzájárulások kezelése a tároló állapota tekintetében

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

### :negative_squared_cross_mark: Fenntartjuk a jogot, hogy nem fogadunk el egy hozzájárulást

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

## :date: Kiadási gyakoriság

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

## :put_litter_in_its_place: A nyelvek és keretrendszerek nem támogatott verzióinak szabályai

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

## :beer: Közösségi fájlok

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

## :robot: Automatizálás

Arra törekszünk, hogy a lehető legtöbb folyamatot automatizáljuk. Célunk, hogy 
a legfontosabb dolgokra koncentráljunk, és hagyjuk, hogy a dolgok a maguk 
módján áramoljanak, például a GitHub projektekbe. Ez magában foglalja a 
következőket:

* Dependabot engedélyezve a lehető legtöbb adattárban (automatikus címkézéssel).
* Különféle GitHub Actions, amelyek segítenek a kódtárolók ápolásában, ha 
szükséges, mint például a [Stale bot](https://github.com/actions/stale).
* Nyilvános projekt táblák esetében GitHub Actions, amelyek a témákat és 
PR-okat a megfelelő állapotokhoz társítják és mozgatják az adott táblában, de 
lehetnek privát táblák és tárolóhelyek is. 

## :black_nib: Szerzők

*Az ebben a dokumentumban szereplő kijelentések ötleteinek és kifejezéseinek 
nagy része a következő közösségek munkáján alapul, vagy azok inspirálták őket:*

* [Honeycomb OSS Lifecycle and Practices](https://github.com/honeycombio/home/blob/main/honeycomb-oss-lifecycle-and-practices.md)
