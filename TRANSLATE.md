Ésszel fejleszt az ember! írta Négyesi Károly
=================================================
A könyv célja, hogy jobban megértsd a Drupal-t, használd nagy dolgokra, és adj vissza a valamit a közösségnek. Ez a fejezet nem csak abban segít, hogy hatékonyabb legyél, hanem abban is,hogy élvezd amit csinálsz.

Használj verziókezelőt
--------------------
Egyszerűen fogalmazva a verziókezelő elmenti a fájl-jaidat, amikor szólsz neki, hogy ezt tegye, ami lehetővé teszi, hogy a későbbiekben visszaállítsd. Természetesen annál többet tud, mint a file-ok változásainak tárolása. Van egy halom másik funkciója de most csak a "visszaállítás később" funkció fontos.

A kód a Drupal.org-on már egy ideje a Git-et (http://git-scm.com), és azt ajánlom, hogy használd! Munkád nyomonkövetés a Git-el olyan egyszerű, mint lefuttatni az alábbi kódot:
    git init .
    git add .
    git commit -m 'Initial commit.'
Úgy szintén, mindig amikor mentesz futtasd a git commit -a -m "valami". A "valami" egy üzenet egy mondat, nem érdekes, hogy mi, ezen ne izgulj. A legegyszerűbb, ha beírod az aktuális időpontot a megjegyzésbe egy rendszerparancs használatával (git commit -a -m "'date'") vagy definiálsz egy  gyorsbillentyűt. Fontos, hogy megerőltetés nélkül meglegyen a munkád összes változata. (A megerőltetés nélküliség fontossága később tisztává válik.)

Egy jobb világban az operációs rendszer megcsinálná ezt helyetted, de sajnos a valóságban általában ez nem történik meg. Amikor elérsz egy mérföldkőhöz,
írj egy hasznos commit üzenetet, arra az esetre, ha meg akarnád osztani a munkát valaki mással. De a percenkénti
commit-olás rutinja nem a megosztásról szól. Arról szól, hogy bármikor vissza tudsz térni egy korábbi állapotra.
Tanulmányozd a `git bisect`-et, hogy hogyan találhatod meg azt a változatot, ahol a hiba előjött. További információk a Git-ről, a 2 fejezetben.

Mentés
------
Használhatod a mysqldump-ot (dev.mysql.com/doc/refman/5.5/en/mysqldump.html) vagy a Backup and Migrate projektet SQL
dump-ok készítésére. Az SQL dumpok szövegfile-ok, így ezeket is lehet a git-be commitolni.
(drupal.org/project/backup_migrate) Lényegében mindegy, hogy milyen szövegfile-okon dolgozol, dobd be a verziókezelőbe!
A weboldalad valószínűleg tartalmaz file-okat, így ne felejtsd el azokat is elmenteni. Windows-hoz és Mac OS X-hez van
 GUI eszköz (Windows Backup és a Time Machine), hogy elérd ezt. Linuxhoz pedig vannak parancssori eszközök (tar és
 rsync). Én az r1soft (r1soft.com) ingyenes és fizetős termékeit tudom ajánlani.

Kísérletezz szabadon
-----------------
Ha semmi mást nem tanulsz ebből a könyvből csak egyet, az legyen ez: Kísérletezz szabadon! Ez egy nagyon fontos része
 annak, hogy sikeres webfejlesztő legyél. Ne izgulj azon, hogy hibázol. Ez az,
 amiért állandóan verziókezelőt használok és állandóan mentek. Soha ne dolgozz egy éles szerveren. Egy fejlesztői
 környezet beállítása nagyon fontos és annyira nem is bonyolult.

Gyakran látok embereket az IRC-n és más fórumokon, akik azt kérdezik: "Mi történik,
ha..." Nos van egy jó hírem: semmi végzetes! A legrosszabb, ami történhet egy hibaüzenet. Ha kapsz egyet,
vedd ki belőle az egyedi részeket (mint a Drupal helyi elérési útját) add meg a Google-nak,
hogy ez miért történhetett. A Szabadon kísérletezés stratégiája nem csak azt jelenti, hogy mindenfélét kipróbálsz,
hanem azt is, hogy közben folyamatosan keresed a weben a megoldásokat.

Egy webes keresés nem tart túl sokáig és nem sokat kell belőle megtenni. keres valamire, nézd meg amit találtál,
ez alapján írd át a keresőszavaidat és inkább előbb, mint később meg fogod találni, amit keresel.
ezek alapján írd újra. Ez egy ismétlődő feladat és az egyetlen lehetőség arra, hogy jobb legyél.

Ez így igaz és nem csak a keresésre, hanem mindenre. A kifejezés "Élethosszig való tanulás" folyamatos tanulást
jelent. Lehet, hogy amit most tanulsz, az nem tűnik hasznosnak, de hasznos lesz később. A mottóm: "Az a nap,
amikor nem tanulok semmit az a nap elpazarolt, felesleges."

Másrészről ne tanulj meg beidegződéseket. A Google egyszerűen jobban ismeri az összes beidegződést,
mint ahogy te bármikor is megtanulhatsz. és a folyamatos tanulásával megelőz minden embert ezen a téren. Tanulj
módszereket inkább! Sajátítsd el azt a szókincset, ami hasznos a keresésekhez! Korunkban, a mindenütt jelenlévő keresés igazi jelentése a "tudás" folyamatosan változik.
Ha tudod használni a keresőt, akkor elég csak a tudás csontváza a fejedben, a húst a gyors keresésekkel növesztheted
hozzá.

A szabadon kísérletezés egy lépés a flow (áramlat) felé. A flow az elme egy furcsa állapota,
Csikszentmihályi Miihány szerint "tevékenység végzése magáért a tevékenységért. Az ego eltűnik. Az idő elrepül.
Minden akció, mozgás és gondolat elkerülhetetlenül következik az előtte lévőből, ahogyan jazz-t játszanak.Az egész
lényed részt vesz benne, és az adottságaidat a lehető legjobban használod fel." A flow elérése örömteli és elvezet a
kiemelkedő teljesítmény eléréséig. Néhány kifejezés erre a mentális állapotra: "a pillanatban", "zónában",
"sínen" és "a játékon tartani a szemet." ???

Nem azt mondjuk, hogy mindig a flow állapotában kell lenned, nem is célszerű a flow-ra törekedned (valószínűleg
lehetetlen is így elérni). Inkább csak szervezd úgy a dolgaidat hogy a flow megtörténhessen. Ó, jaj,
erre nincs egyszerű recept, de a következő dolgok valószínűleg segítenek:

*Legyenek világos céljaid.* Ez a legegyszerűbben úgy érhető el, ha jól meghatározott projceteken dolgozol. (Íme egy
újabb ok, hogy egy jó specifikáció létfontosságú a sikerhez!) Ha a specifikációval problémák vannak,
akkor szedd szét jól definiálható feladatokra.

*Koncentrálj!* Azt ajánlom hallgass zenét, hogy jobban koncentrálj. Jó hangulatba hoz,
és elfedi a zavaró zajokat.  (A fordító megjegyzése: különböző családtagokat tegyük minél messzebbre.)

*Élvezd az közvetlen és azonnali visszajelzéseket.* Ez az oka, hogy egy web programozó miért éri el egyszerűbben a
flow-t. A közvetlen és azonnali visszajelzés adott a szakmánkban. Mentsd el a kódot,
nyomj egy frissítést a böngészőben, és ta-da! Az azonnaliság fontos itt, arra várni,
hogy a kód leforduljon vagy várni, hogy egy teszt végigfusson, nem felel meg ennek a módszernek.

*A tevékenységed ne legyen se túl könnyű, se túl nehéz*. Ezt elég trükkös elérni munkahelyi környezetben. Érezd magad
 szerencsésnek, amikor ez megtörténik.

*Egyfajta személyes ellenőrzés a különböző helyzetek és tevékenységek felett.* Emlékszel arra amit mondtam arról,
hogy a problémákat bontsuk feladatokra? Ez megadja az ellenőrzés érzését. Egy nem rögzített ütemterv szintén segít.

*Az aktivitás eredendően jutalmazó, ezért könnyebb cselekedni.* Érezted már magadat jól attól, mert a kódod működött?

Közreműködés
----------
A nyílt forrású projectekben való közreműködés nem fizet két-hetente, de másképpen lehet vele jól járni. Először is,
ha pénzt akarsz, van egy közösség amely befogad, így a szakmai hálózatod nő, ami több munkalehetőséghez vezet. Ez
különlegesen igaz a Drupal-ra, ahol a mínőségi munkavállalókra való kereslet messze meghaladja a kínálatot (jelenleg,
de ez elég kiszámíthatatlan és várhatóan egy ideig még így lesz.)

Másodszor, a szakértői visszajelzések esélyt adnak a tanulásra. Ez az egyik oka, hogy miért nagy lehetőség a nyílt
forráskód - közösen tanulunk.

Harmadszor, mi emberek szociálisan fejlett állatok vagyunk. A közösséghez tartozás és dicséretet kapni azoktól,
akiket tisztelünk mindenki számára fontos.

Negyedszer, nézzük meg a fenti listát a flow-ról! Amikor a dolgozol a saját issue-don, vannak tiszta céljaid,
így válassz olyat, ami megvalósítható (de ne csak olyat). Természetesen, teljes  felügyeleted van a teljes szituáció
felett.

Végűl, bár nem kapsz készpénzt mégis lényegében kifizetődő.

Nos, hogyan tudsz közreműködni? Közreműködni sok formában lehet (marketing, rendezvényszervezés,
stb.) de van kettő amit ki szeretnék emelni a dokumentáció és a kódolás.

Dokumentációt legjobban az tud írni, aki elért arra a pontra, hogy úgy érzi, megértette az adott témát. ez létrehoz
egy rendkívüli tehetséget, hogy visszajelezze mi volt az, amit nehéz volt megérteni az elején. Így amikor éppen azon
harcolsz, hogy megérts valamit, írj jegyzeteket a problémákról, amiket találtál. Végül írd le a válaszokat,
amiket találtál és van is egy kézikönyv oldalad. Lehet, hogy nem lesz egyszerű. Lehet,
hogy kissé tört angolsággal. Ne aggódj. Egyszerűbb kijavítani egy kézikönyv oldalt, mint írni egyet.

Kódolásban való közreműködés a leggyakrabban patch-ek írásában és azok vizsgálatában van. Mind a kettő nagyon fontos.
 Elmehetsz bármelyik project oldalára, kattints az "open issues" hivatkozásra, és kijavíthatsz egy kiemelkedő hibát
 vagy felülvizsgálhatsz egy patch-et. Kiváló kézikönyv oldalak vannak amik segítenek ebben a folyamatban: drupal
 .org/patch, drupal.org/patch/apply, és drupal.org/handbook/git.

Még egyszer, ne próbálj a tökéletes megoldással előállni. Csinálj valamit, ami működik és dolgozz a közösséggel.
Megjegyzem, hogy sok patch vizsgálat rövid és nem túl hízelgő. Jegyezd meg, hogy a negatív kritika a kódodnak szól és
 nem neked! Mi mindenkit szeretünk, aki közreműködik. Időt tölteni a közreműködéssel önmagában is nagyrabecsülendő,
 mivel az idő a legdrágább árucikk a nyílt forrású közösségekben.

Csinálhatsz egy értékes közreműködést az issue queue-hoz, ha nem programozol. Nyithatsz egy hibajelentést és
ellenőrizheted, hogy tartalmaz-e elég információt ahhoz, hogy meg lehessen ismételni. Ha nem. jelöld így: "több
információ szükséges". Ha igen, próbáld, megismételni. Ha többet nem lehet megismételni,
zárd le "javított"-ként (fixed). Szükségünk van egy csomó emberre, akik ezt csinálják, hogy azok,
akik jobban ismerik a Drupal-t - például Te, miután elolvastad ezt a könyvet,
gyakorlatot szereznek és időt fordítanak rá - tudjanak valódi problémákra javítására koncentrálni

Többet erről és más közreműködési lehetőségekről lásd a 38. fejezetet.
