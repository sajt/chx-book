Ésszel fejleszt az ember!
=========================
### írta Négyesi Károly ###
###### A The Definitive Guide to Drupal 7 c. könyvből

A könyv célja, hogy eszközöket adjon ahhoz, hogy jobban megértsd a Drupalt, amivel aztán nagyszerű dolgokat csinálj, és adj vissza valamit a közösségnek. Ez a fejezet nem csak abban segít, hogy hatékonyabb legyél, hanem élvezd is amit csinálsz.

Használj verziókezelőt
--------------------
Egyszerűen fogalmazva a verziókezelő mindig elmenti a fájljaidat, amikor megkéred erre. Így lehetővé válik, hogy a későbbiekben visszaállítsd. Természetesen annál többet tud, mint a állományok változatainak tárolása. Van egy halom másik funkciója, de most csak a „visszaállítás később” funkció lényeges.

A drupal.org-on már egy ideje a Gitet (http://git-scm.com) használjuk, és azt ajánlom, hogy ezt használd Te is! Munkád nyomon követése a Gittel olyan egyszerű, mint lefuttatni az alábbi kódot:

    git init .
    git add .
    git commit -m 'Initial commit.'

Mindig amikor mentesz, futtasd a `git commit -a -m "bármi"` parancsot. A „bármi” egy üzenet, egy mondat, mindegy, hogy mi, ezen ne aggódj. A legegyszerűbb, ha beírod az aktuális időpontot a megjegyzésbe egy rendszerparancs használatával (`git commit -a -m "`date`"`) vagy definiálsz egy  gyorsbillentyűt. Fontos, hogy a megerőltetés nélkül meglegyen a munkád összes verziója. (A megerőltetés-nélküliség fontossága később válik tisztává.)

Egy jobb világban az operációs rendszer megcsinálná ezt helyetted, de sajnos a valóságban általában ez nem történik meg. Amikor elérsz egy mérföldkőhöz, akkor írj egy hasznos commit üzenetet, arra az esetre, ha meg akarnád osztani a munkát valaki mással. A folyamatos commitolás rutinja nem a megosztásról szól. Arról szól, hogy bármikor vissza tudsz térni egy korábbi állapotra. Tanulmányozd a `git bisect`-et, hogy hogyan találhatod meg azt a változatot, ahol a hiba előjött. További információk a Gitről, a 2. fejezetben.

Biztonsági mentés
-----------------
Használhatod a mysqldumpot (dev.mysql.com/doc/refman/5.5/en/mysqldump.html) vagy a Backup and Migrate projektet SQL mentések készítésére. Ezek az SQL mentések szövegfájlok, így ezeket is lehet a Gitbe commitolni (drupal.org/project/backup_migrate). Lényegében mindegy, hogy milyen szövegfájlokon dolgozol, csak dobd be a verziókezelőbe!

A weboldalad esetleg tartalmaz állományokat, így ne felejtsd el azokat is elmenteni. Windows-hoz és Mac OS X-hez is van GUI eszköz (Windows Backup és a Time Machine), hogy elérd ezt. Linuxhoz pedig vannak parancssori eszközök (tar és rsync). Én az r1soft (r1soft.com) ingyenes és fizetős termékeit tudom ajánlani.

Kísérletezz szabadon
--------------------
Ha semmi mást nem tanulsz ebből a könyvből csak egyet, az legyen ez: Kísérletezz szabadon! Ez egy nagyon fontos része annak, hogy sikeres webfejlesztő legyél. Ne aggódj, nem tudod elrontani. Ez az amiért állandóan verziókezelőt használok és állandóan mentek. Soha ne dolgozz éles szerveren. Egy fejlesztői környezet beállítása nagyon fontos és nem is bonyolult (ráadásul erről szól a 12. fejezet).

Gyakran látok embereket az IRC-n és más fórumokon, akik azt kérdezik: „Mi történik, ha...” Nos van egy jó hírem: semmi végzetes! A legrosszabb ami történhet, egy hibaüzenet. Ha kapsz egyet, vedd ki belőle a rád vonatkozó részeket (például a Drupal helyi elérési útját) add meg a Google-nak, hogy kitaláld, ez miért is történhetett. A Szabadon kísérletezés stratégiája nem csak azt jelenti, hogy mindenfélét kipróbálsz, hanem azt is, hogy közben folyamatosan keresed a weben a megoldásokat.

Egy webes keresés nem tart túl sokáig és minél többet futtatsz, annál jobb. Keress valamire, nézd meg amit találtál, ez alapján írd át a keresőszavaidat és inkább előbb, mint később meg fogod találni, amit keresel.
Ez egy állandóan ismétlődő feladat és ez az egyetlen lehetőség arra, hogy jobb legyél.

Ez így igaz és nem csak a keresésre, hanem mindenre. A kifejezés „Élethosszig való tanulás” folyamatos tanulást jelent. Lehet, hogy amit most megtanulsz, nem tűnik hasznosnak, de hasznos lehet később. A mottóm: „A nap, amikor nem tanulok semmit, elpazarolt és felesleges.”

Másrészről ne tanulj meg tényeket. A Google jobban ismeri az összes tényt, mint amit valaha is megtanulhatunk és gyorsabban tanulja meg ezeket, mint bárki. Inkább tanulj módszereket! Sajátítsd el azt a szókincset, ami hasznos a keresésekhez! Korunkban, a mindenütt elérhető webkeresés még azt is megváltoztatja hogy mi a „tudás”. Ha tudod használni a keresőt, akkor elég csak a tudás csontváza a fejedben, a húst a gyors keresésekkel növesztheted hozzá.

A szabadon kísérletezés egy lépés a flow (áramlat) felé. A flow az elme egy furcsa állapota, Csíkszentmihályi Mihány szerint „tevékenység végzése magáért a tevékenységért. Az ego eltűnik. Az idő elrepül. Minden akció, mozgás és gondolat elkerülhetetlenül következik az előtte lévőből, ahogyan jazzt játszanak.Az egész lényed részt vesz benne, és az adottságaidat a lehető legjobban használod fel.” A flow elérése örömteli és elvezet a kiemelkedő teljesítmény eléréséig. Néhány kifejezés erre a mentális állapotra: „a pillanatban”, „zónában”, „mederben” és „a játékon tartani a szemet.” ???

Nem azt mondjuk, hogy állandóan a flow állapotában kell lenned, nem is célszerű a flowra törekedned (valószínűleg nem is lehet). Inkább csak szervezd úgy a dolgaidat hogy a flow megtörténhessen. Sajnos erre nincs egyszerű recept, de a következő dolgok valószínűleg segítenek:

*Legyenek világos céljaid.* Ezt a legegyszerűbben úgy érheted el, ha jól meghatározott projekteken dolgozol. (Íme ezért is létfontosságú egy jó specifikáció a sikerhez!) Ha a specifikációval problémák vannak, akkor szedd szét feladatokra, amelyek önmagukban tiszták.

*Koncentrálj!* Azt ajánlom hallgass zenét a koncentráláshoz. Jó hangulatba hoz, és elfedi a zavaró zajokat.

*Élvezd az közvetlen és azonnali visszajelzéseket.* Ez az oka, hogy egy web programozó miért éri el egyszerűbben a flowt. A közvetlen és azonnali visszajelzés adott a szakmánkban. Mentsd el a kódot, nyomj egy frissítést a böngészőben, és ta-da! Az azonnaliság fontos itt, arra várni, hogy a kód leforduljon vagy várni, hogy egy teszt végigfusson, nem felel meg ennek a módszernek.

*A tevékenységed ne legyen se túl könnyű, se túl nehéz*. Ezt elég trükkös elérni munkahelyi környezetben. Érezd magad szerencsésnek, amikor ez megtörténik.

*Egyfajta személyes ellenőrzés a különböző helyzetek és tevékenységek felett.* Emlékszel arra amit mondtam arról, hogy a problémákat bontsuk feladatokra? Ez megadja az ellenőrzés érzését. Egy nem rögzített (határidők nélküli) ütemterv szintén segít.

*Az aktivitás eredendően jó érzést kelt, ezért könnyebb cselekedni.* Érezted már magadat jól attól, mert a kódod működött?

Közreműködés
----------
A nyílt forrású projektben való közreműködés nem fizet kéthetente, de másképpen lehet vele jól járni.

Először is, ha pénzt akarsz, van egy befogadó közösség, így a szakmai ismeretséged is nő, ami több munkalehetőséghez vezet. Ez különlegesen igaz a Drupalra, ahol a minőségi munkavállalókra való kereslet messze meghaladja a kínálatot (legalábbis most éppen és bár ez elég kiszámíthatatlan de várhatóan egy ideig még így lesz.)

Másodszor, a szakértők visszajelzései lehetőséget adnak a tanulásra. Ez az egyik oka, hogy miért nagy lehetőség a nyílt forráskód - közösen tanulunk.

Harmadszor, mi emberek társas lények vagyunk. A közösséghez tartozás és dicséretet kapni azoktól, akiket tisztelünk mindenki számára fontos.

Negyedszer, vizsgáld meg a fenti listát a flowról! Amikor dolgozol a saját hibajegyeden (issue), vannak tiszta céljaid, így válassz olyat, ami megvalósítható (éppen hogy csak). Természetesen teljes felügyeleted van a helyzet felett.

Végül, bár nem kapsz készpénzt, mégis teljesen kifizetődő.

Nos, hogyan tudsz közreműködni? Közreműködni sok formában lehet (marketing, rendezvényszervezés, stb.) de van kettő amit ki szeretnék emelni. Ezek a dokumentáció és a kódolás.

Dokumentációt legjobban az tud írni, aki éppen azon a ponton van, hogy úgy érzi, megértette az adott témát. Ahhoz különleges tehetség kell, hogy amikor már gyakorlottak vagyunk egy témában, akkor megértsük a kezdők problémáit. Így amikor éppen azon küszködsz, hogy megérts valamit, írj jegyzeteket a problémákról, amiket találtál. Végül írd le a válaszokat,amiket találtál és van is egy kézikönyv oldalad. Lehet, hogy nem lesz egyszerű. Lehet,hogy kissé tört angolsággal, de emiatt ne aggódj. Egyszerűbb kijavítani egy kézikönyv oldalt, mint írni egyet újat.

Kódolásban való közreműködés a leggyakrabban patchek írásában és azok átnézésében van. Mind a kettő nagyon fontos. Elmehetsz bármelyik projekt oldalára, kattints az „open issues” hivatkozásra, és kijavíthatsz egy fontos hibát vagy átnézhetsz egy patchet. Kiváló kézikönyv oldalak vannak, amik segítenek ebben: `drupal.org/patch`, `drupal.org/patch/apply`, és `drupal.org/handbook/git`.

Még egyszer, ne próbálj a tökéletes megoldással előállni. Csinálj valamit, ami működik és dolgozz a közösséggel. Megjegyzem, hogy sok patch átnézés leírása rövid és nem túl hízelgő. Jegyezd meg, hogy a negatív kritika a kódodnak szól és nem neked! Mi mindenkit szeretünk, aki közreműködik. Időt tölteni a közreműködéssel önmagában is nagyra becsülendő, mivel az idő a legdrágább árucikk a nyílt forrású közösségekben.

Írhatsz egy hibajegyet, ha nem programozol. Nyithatsz egy hibajelentést és ellenőrizheted, hogy tartalmaz-e elég információt ahhoz, hogy meg lehessen ismételni. Ha nem, jelöld így: „több információ szükséges” (needs more information). Ha igen, próbáld megismételni. Ha többet nem lehet megismételni, zárd le „javított”-ként (fixed). Szükségünk van sok emberre, akik ezt csinálják, hogy azok, akik jobban ismerik a Drupalt – például Te, miután elolvastad ezt a könyvet, gyakorlatot szereznek és időt fordítanak rá – tudjanak valódi problémák megoldására koncentrálni.

Többet erről és más közreműködési lehetőségekről lásd a 38. fejezetet.
