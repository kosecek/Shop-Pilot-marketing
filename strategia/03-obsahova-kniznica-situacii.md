# Obsahová knižnica: situácie expertného systému ako príbehy (v1.1)

Zdroj: *Shop Pilot — Expert System Semantic Contract v0.51 & L1 Situation Matrix v0.34* (interný dokument, 24 aktívnych situácií MVP). Tento dokument je marketingová derivácia: každá situácia = jeden príbeh pre príspevok, e-mail, slide v ukážke a neskôr reklamu.

**Stav implementácie (18. 9. 2026).** Podľa *V2 Inventory/DR4 Vertical Slice Plan v0.4* sa práve dokončuje prvý slice nového systému (V2): reťazec skladových situácií (rastúci dopyt → dochádzajú zásoby → nedostupný produkt), platená návštevnosť na nedostupný produkt, ich spojená karta (bývalé DR4) a pripomienka zviditeľnenia po naskladnení. Tento slice nahrádza pôvodné pravidlá R2, R3, R4 a DR4 a musí prejsť prehrávkou incidentu PMAG/VEL (24. až 30. 6. 2026), inak nejde do produkcie. Zvyšok produktu beží na pôvodných pravidlách V1 (DR1, DR2, DR3, DR5, DR6, DR7, DR8, DR10, DR12); ich mapovanie na nové situácie je v prílohe 9 zmluvy označené ako neoverené.

Preto má každá karta pole **Dnes v produkte** s tromi hodnotami: **V2 slice** (prvý nasadený kus nového systému, publikovať po nasadení do produkcie), **V1** (pôvodné pravidlo, publikovať s reálnym pozorovaním z histórie odporúčaní), **návrh** (čaká na ďalšie fázy, nepublikovať ako funkciu). Platí: **publikujeme len príbehy o tom, čo produkt reálne robí.** Toto je hodnota „spoľahlivosť“ prenesená do marketingu.

**Názvy situácií** sú v zmluve kanonické a budú pred zobrazením zákazníkom lokalizované (rozhodnutie zakladateľa). Pri štyroch situáciách zo slice-u už existujú texty kariet pre majiteľa a tie používame prednostne; pri ostatných používame kanonický názov a po lokalizácii karty aktualizujeme.

---

## 1. Kostra obsahu: štyri otázky majiteľa

Expertný systém triedi každú situáciu podľa toho, aké rozhodnutie má majiteľ urobiť. Tie isté štyri otázky sú kostrou ranného briefingu, ukážky, landing page aj obsahu:

| Otázka majiteľa | Čo sa deje s peniazmi | Typické slovesá akcie | Aktívnych situácií |
|---|---|---|---|
| **Kde strácam?** | Peniaze aktívne odtekajú: reklama, marža, viazaný kapitál, zbytočné náklady | zrezať, pozastaviť, obmedziť, prepočítať, prestať robiť | 9 |
| **Kde uniká hodnota?** | Peniaze neprichádzajú, hoci dopyt alebo hodnota už existuje | opraviť, doskladniť, spriechodniť, presmerovať, doplniť | 11 |
| **Kde pritlačiť?** | Peniaze by mohli prísť s väčšou alokáciou, pozornosťou, zásobou | pritlačiť, navýšiť, podporiť, promovať, škálovať | 4 |
| **Môžem veriť dátam?** | Poistka, nie kategória: chráni dôveryhodnosť všetkého vyššie | preveriť, opraviť meranie | poistka |

Mriežka situácií v jazyku majiteľa (názvy sú kanonické, tak sa zobrazia aj v produkte):

| Oblasť | Kde strácam? | Kde uniká hodnota? | Kde pritlačiť? |
|---|---|---|---|
| Reklama a návštevnosť | Kampaň míňa rozpočet bez primeraného zisku · Akvizícia privádza zákazníkov, ktorí sa neoplácajú · Platený traffic smeruje na nepredajný produkt | Z dôležitého zdroja návštevnosti chodí menej ľudí | Výkonná kampaň má priestor na kontrolované škálovanie |
| Sklad | Produkt viaže cash a predáva sa príliš pomaly | Dôležitý produkt je nedostupný pri existujúcom dopyte · Hot seller má nízke skladové pokrytie a hrozí preventívny únik predaja | Emerging bestseller má rastúci dopyt a zaslúži si podporu |
| Web a nákupný proces | – | Dôležitá produktová alebo landing stránka má návštevnosť, ale nepredáva · Košík alebo checkout prepúšťa zákazníkov, ktorí už chceli kúpiť · Dôležitá skupina návštevníkov prestala nakupovať | Dôležitá stránka má návštevnosť, ktorú vieš lepšie premeniť na predaj |
| Zákazníci | Noví zákazníci prinášajú slabšiu maržu než zvyčajne | Noví zákazníci sa nevracajú na druhý nákup · Zákazníci po očakávanom čase neobjednávajú znova | Hodnotný zákaznícky segment vieš znovu aktivovať |
| Ceny a košík | Zľavy alebo kupóny zvyšujú obrat, ale ničia maržu · Predajný mix sa presúva do nízkomaržových produktov | Objednávky končia tesne pod hranicou dopravy zdarma | – |
| Prevádzka | Produkt má nadpriemerne veľa vratiek, refundov alebo reklamácií | Objednávky pripravené na vybavenie čakajú príliš dlho · Objednávky blokuje platba alebo doručenie | – |
| Zdravie e-shopu | Dlhodobo klesá prevádzkový zisk alebo prevádzková marža e-shopu | – | – |

Prázdne bunky sú zámerné (zmluva: „vymýšľať umelé situácie kvôli symetrii je horšie ako poctivá medzera“). Aj to je príbeh.

---

## 2. Formát karty a pravidlá použitia

Každá karta má rovnakú štruktúru:

- **Otázka majiteľa** a oblasť.
- **Dnes v produkte:** V2 slice / V1 (ktoré pôvodné pravidlo; mapovanie podľa prílohy 9 zmluvy, neoverené) / návrh.
- **Hook:** prvá veta príspevku alebo predmet e-mailu.
- **Príbeh:** situácia → v číslach → čo to stojí → čo urobiť dnes → ako to Shop Pilot stráži. Hranaté zátvorky sú miesta na reálne čísla z Kifra.sk alebo pilotov; bez reálneho čísla sa príbeh nepublikuje.
- **Pozor:** hranica zo zmluvy, ktorú text nesmie prekročiť (čo systém netvrdí).
- **Kanál a priorita:** 1 = publikovať v prvom mesiaci, 2 = do troch mesiacov, 3 = zásobník.

Pravidlá formulácie:

1. Názov situácie používať doslovne (je to jazyk majiteľa, prešiel testom zmluvy a takto sa zobrazí v produkte).
2. Žiadne metriky v titulku („PNO“, „CVR“, „sessions“). Metrika je dôkaz v tele textu, nie nadpis.
3. Dopad vždy „za deň“. Produkt počíta dopad na deň; 7- a 30-dňové projekcie sú len kontext.
4. Akcia vždy prvá a v slovesnom tvare, presne podľa prvej akcie zo zmluvy.
5. Produkt sa spomína až na konci karty. Príspevok je o majiteľovi, nie o nás.

---

## 3. Karty situácií (24 aktívnych)

### Kde strácam?

#### K1. Kampaň míňa rozpočet bez primeraného zisku
- **Otázka:** Kde strácam? Reklama, jedna kampaň.
- **Dnes v produkte:** V1 (DR1 Neefektívna kampaň, DR5 Zhoršujúca sa kampaň); reálny prípad z Kifra.sk existuje.
- **Hook:** „Moja najlepšia kampaň podľa ROAS bola stratová. Asi 1 000 €.“
- **Príbeh:** Kampaň má vysoký ROAS, report vyzerá skvele. Po odpočítaní tovaru, dopravy, poplatkov za platbu a podielu fixných nákladov prináša každá objednávka stratu. V číslach: [ROAS X, marža po nákladoch Y %, break-even ROAS Z]. Čo to stojí: [N € za deň]. Čo urobiť dnes: znížiť rozpočet, pozastaviť, alebo upraviť bidding, cielenie a kreatívu. Ako to Shop Pilot stráži: každú noc prepočíta zisk kampane po všetkých nákladoch, nie ROAS.
- **Pozor:** nehovoriť „nízky ROAS“; ide o zisk po nákladoch. Nesľubovať, že systém vie, ktorý produkt kampaň predáva (mapovanie kampaň → produkt nie je k dispozícii).
- **Kanál a priorita:** LinkedIn, skupiny, cold e-mail, hero webu. Priorita 1, jediný príbeh s reálnym číslom.

#### K2. Akvizícia privádza zákazníkov, ktorí sa neoplácajú
- **Otázka:** Kde strácam? Reklama, konkrétny zdroj zákazníkov.
- **Dnes v produkte:** návrh (vyžaduje atribučnú vrstvu).
- **Hook:** „Zdroj, ktorý privádza najviac nových zákazníkov, privádza tých najmenej ziskových.“
- **Príbeh:** Noví zákazníci z jedného zdroja nakupujú so zľavou, vracajú tovar a nevracajú sa. V číslach: [marža na nového zákazníka zo zdroja vs. priemer e-shopu]. Čo to stojí: [rozdiel × noví zákazníci za deň]. Čo urobiť dnes: prehodnotiť cielenie, optimalizačný cieľ, kreatívu, promo alebo produktový mix pre tento zdroj. Ako to Shop Pilot stráži: porovnáva skutočnú maržu nových zákazníkov podľa zdroja, a to len vtedy, keď je priradenie zdroja spoľahlivé.
- **Pozor:** nie generický „nízky ROAS“. Ak priradenie zdroja nie je spoľahlivé, systém zdroj neobviní; to je samo o sebe príbeh o spoľahlivosti.
- **Kanál a priorita:** LinkedIn. Priorita 3 (po nasadení).

#### K3. Platený traffic smeruje na nepredajný produkt
- **Text karty v produkte (slice):** „Produkt je nedostupný a stále naň chodí platený traffic.“ V spojení s U2 vzniká spojená karta „Dôležitý produkt je nedostupný a stále naň chodí platený traffic“ s prvou akciou: „Dočasne nastav produkt/variant na hidden, aby sa odstránil z reklamného katalógu alebo feedu. Po naskladnení ho znovu zviditeľni. Skontroluj, či máš dostupnú alternatívu alebo skladové riešenie.“
- **Otázka:** Kde strácam? Reklama, produktová stránka.
- **Dnes v produkte:** V2 slice (nahrádza DR4 Reklama trpí kvôli supply); publikovať po nasadení do produkcie.
- **Hook:** „Platíte za návštevy produktu, ktorý sa nedá kúpiť.“
- **Príbeh:** Produkt je vypredaný alebo nedostupný a platená návštevnosť naň ďalej chodí. V číslach: [platené návštevy stránky za deň, odhad minutých peňazí]. Čo to stojí: [ušlá marža z nedostupnosti € za deň + platená návštevnosť ako odhad plytvania]. Čo urobiť dnes: dočasne skryť produkt alebo variant, aby vypadol z reklamného katalógu a feedu; po naskladnení ho znovu zviditeľniť; skontrolovať alternatívu. Nerušiť celú kampaň. Ako to Shop Pilot stráži: z GA4 vidí platenú návštevnosť na stránke produktu, ktorý sa nedá kúpiť, spojí ju s vypredaným produktom do jednej karty a po naskladnení pripomenie zviditeľnenie (D1).
- **Pozor:** netvrdiť „kampaň X beží na produkt Y“. Systém vidí platenú návštevnosť na stránke produktu, nie mapovanie kampane na produkt. Straty z nedostupnosti a z platenej návštevnosti sa nesčítavajú naslepo; plytvanie reklamou je odhad, ak sa náklady nedajú spoľahlivo priradiť.
- **Kanál a priorita:** skupiny, cold e-mail (otvárač z Meta Ad Library je ručná kontrola zakladateľa, nie funkcia produktu), ukážka. Priorita 1. Reálne čísla: z prehrávky PMAG/VEL, ak fixture obsahuje platenú návštevnosť.

#### K4. Produkt viaže cash a predáva sa príliš pomaly
- **Otázka:** Kde strácam? Sklad, jeden produkt.
- **Dnes v produkte:** návrh (R5 Sortiment vypadáva je iná téma; pomalý sklad nemá živé pravidlo).
- **Hook:** „Koľko peňazí vám leží na sklade v produktoch, ktoré sa nehýbu?“
- **Príbeh:** Zásoba produktu vydrží pri aktuálnej rýchlosti predaja [X mesiacov]. V číslach: [hodnota zásoby, predaj za deň]. Čo to stojí: [viazaný kapitál × náklad kapitálu alebo riziko zľavy = € za deň]. Čo urobiť dnes: vypredať, znížiť cenu, prestať objednávať, upraviť merchandising; ak už produkt nemá byť v predaji, skryť ho. Ako to Shop Pilot stráži: rýchlosť predaja proti zásobe pre každý produkt, relatívne k veľkosti e-shopu.
- **Pozor:** dopad je cena viazaného kapitálu za deň, nie hodnota zásob. Nehovoriť o „starom produkte“ (vek v katalógu nie je vek zásoby) ani o sezónnosti.
- **Kanál a priorita:** skupiny (téma cash-flow rezonuje na Upterdame). Priorita 2.

#### K5. Noví zákazníci prinášajú slabšiu maržu než zvyčajne
- **Otázka:** Kde strácam? Zákazníci, celý e-shop.
- **Dnes v produkte:** návrh (kohortová vrstva ešte neexistuje).
- **Hook:** „Nových zákazníkov pribúda. Zisk z nich nie.“
- **Príbeh:** Nedávne skupiny nových zákazníkov majú po vyzretí slabšiu maržu: viac zliav, lacnejší mix, viac vratiek. V číslach: [marža na nového zákazníka vs. história]. Čo to stojí: [€ za deň]. Čo urobiť dnes: skontrolovať vstupnú ponuku, zľavy, produktový mix, vratky, náklady na doručenie a akvizičný mix. Ako to Shop Pilot stráži: porovnáva vyzreté skupiny nových zákazníkov na úrovni celého e-shopu; ak vie zdroj spoľahlivo určiť, ukáže ho.
- **Pozor:** neobviňovať zdroj bez spoľahlivého priradenia. Nezamieňať s „chýba druhý nákup“.
- **Kanál a priorita:** LinkedIn. Priorita 3.

#### K6. Zľavy alebo kupóny zvyšujú obrat, ale ničia maržu
- **Otázka:** Kde strácam? Ceny, konkrétna promo akcia.
- **Dnes v produkte:** V1 (DR10 Erózia cez zľavy).
- **Hook:** „Rekordný mesiac v tržbách. Najhorší v zisku. Kupóny.“
- **Príbeh:** Promo zvyšuje počet objednávok, ale realizovaná marža po zľave padá. V číslach: [podiel objednávok so zľavou, marža po zľave vs. bez]. Čo to stojí: [€ za deň]. Čo urobiť dnes: obmedziť zľavy, upraviť promo pravidlá, zmeniť politiku zliav. Ako to Shop Pilot stráži: sleduje realizovanú maržu po zľave v konkrétnej promo akcii.
- **Pozor:** samotná existencia zliav nestačí; musí ísť o materiálnu stratu marže. Nehovoriť „zľavy sú zlé“.
- **Kanál a priorita:** skupiny, LinkedIn (pred Black Friday). Priorita 1.

#### K7. Predajný mix sa presúva do nízkomaržových produktov
- **Otázka:** Kde strácam? Ceny, jeden produkt ako ťahač.
- **Dnes v produkte:** návrh.
- **Hook:** „Predávate viac a zarábate menej. Presunul sa mix.“
- **Príbeh:** Rastie podiel nízkomaržových produktov na predaji. V číslach: [podiel, priemerná marža predtým a teraz]. Čo to stojí: [€ za deň]. Čo urobiť dnes: upraviť merchandising, promo, cenu alebo nákupnú stratégiu. Ako to Shop Pilot stráži: hľadá konkrétny produkt, ktorý ťahá mix nadol, relatívne k e-shopu.
- **Pozor:** nízka marža sama o sebe nestačí.
- **Kanál a priorita:** LinkedIn. Priorita 3.

#### K8. Produkt má nadpriemerne veľa vratiek, refundov alebo reklamácií
- **Otázka:** Kde strácam? Prevádzka, jeden produkt.
- **Dnes v produkte:** návrh.
- **Hook:** „Produkt, ktorý sa vracia každý piaty raz, nie je bestseller.“
- **Príbeh:** Vyzreté objednávky produktu majú výrazne vyššiu vratkovosť než zvyšok e-shopu. V číslach: [vratkovosť produktu vs. e-shop]. Čo to stojí: [náklady na vratky × aktuálny predaj za deň]. Čo urobiť dnes: skontrolovať popis, kvalitu, veľkostnú tabuľku, dopravcu a očakávania; pri vážnom probléme obmedziť promo alebo dočasne skryť. Ako to Shop Pilot stráži: hodnotí vyzreté objednávky (vratky meškajú) a kým nie je vyriešené, brzdí odporúčania „pritlačiť“ na ten istý produkt.
- **Pozor:** nie „vratky za posledných 30 dní“.
- **Kanál a priorita:** skupiny (móda, obuv). Priorita 2.

#### K9. Dlhodobo klesá prevádzkový zisk alebo prevádzková marža e-shopu
- **Otázka:** Kde strácam? Zdravie e-shopu, celok.
- **Dnes v produkte:** návrh.
- **Hook:** „Žiadny jeden problém. A predsa zisk rok po roku klesá.“
- **Príbeh:** Pomalá erózia rozložená medzi marketing, zľavy, mix, vratky, dopravu a fixné náklady; žiadna jedna vec nespustí alarm. V číslach: [prevádzkový zisk vs. minulý rok, rozklad podľa príčin]. Čo to stojí: [rozdiel € za deň]. Čo urobiť dnes: prehľad ziskovosti s rozkladom podľa príčin; nie automatická akcia. Ako to Shop Pilot stráži: porovnáva uzavreté obdobia medziročne vrátane fixných nákladov; týždenný alebo mesačný signál, nie denný alarm; nehlási, ak pokles vysvetľujú už otvorené situácie.
- **Pozor:** nikdy „hneď“; systém netvrdí príčinu, ak ju rozklad nepodloží.
- **Kanál a priorita:** LinkedIn, webinár s účtovníkmi. Priorita 2.

### Kde uniká hodnota?

#### U1. Z dôležitého zdroja návštevnosti chodí menej ľudí
- **Otázka:** Kde uniká hodnota? Reklama a návštevnosť, jeden zdroj.
- **Dnes v produkte:** V1 (DR2 Pokles tržieb kvôli návštevnosti, DR7 Zhoršenie kanála).
- **Hook:** „Tržby klesli. Skôr než niečo meníte, zistite, ktorý zdroj ľudí vypadol.“
- **Príbeh:** Historicky hodnotný zdroj (organické vyhľadávanie, konkrétna kampaň, porovnávač) privádza menej ľudí než v porovnateľné dni. V číslach: [očakávané vs. skutočné návštevy, hodnota na návštevu]. Čo to stojí: [€ za deň]. Čo urobiť dnes: overiť meranie, potom kampane, organiku, feed, indexáciu, presmerovania a obsah. Ako to Shop Pilot stráži: porovnáva s rovnakými dňami v týždni a overí, či objednávky sedia s návštevnosťou; ak nie, hlási problém merania, nie biznisu.
- **Pozor:** nie „klesli sessions“; iba historicky hodnotné zdroje.
- **Kanál a priorita:** skupiny, LinkedIn. Priorita 1.

#### U2. Dôležitý produkt je nedostupný pri existujúcom dopyte
- **Text karty v produkte (slice):** „Dôležitý produkt je nedostupný pri existujúcom dopyte.“ Stav „hneď“ (kríza), ak prejde prahom dôležitosti.
- **Otázka:** Kde uniká hodnota? Sklad, jeden produkt.
- **Dnes v produkte:** V2 slice (nahrádza R2 Vypredaný TOP produkt); publikovať po nasadení. Reálny prípad: PMAG/VEL, jún 2026.
- **Hook:** „Najhorší deň e-shopu: ľudia chcú kúpiť a nemôžu.“
- **Príbeh:** Dôležitý produkt je vypredaný, dopyt trvá (ľudia chodia na jeho stránku). V číslach: [predaje za deň pred vypredaním, marža]. Čo to stojí: [ušlá marža € za deň]. Čo urobiť dnes: doskladniť, ponúknuť alternatívu, upraviť dostupnosť. Ako to Shop Pilot stráži: keď dôležitý produkt s dopytom nie je dostupný, ide na vrch zoznamu bez ohľadu na iné čísla; dôležitosť meria podielom na tržbách.
- **Pozor:** nie pre produkty, ktoré majiteľ zámerne stiahol (skryté). Systém nevidí otvorené objednávky u dodávateľa, povedať to úprimne. Ak import dát zlyhá, situácia sa nezavrie sama (S9).
- **Kanál a priorita:** skupiny, LinkedIn (príbeh PMAG/VEL), ukážka (spolu s K3 ako spojená karta). Priorita 1.

#### U3. Hot seller má nízke skladové pokrytie a hrozí preventívny únik predaja
- **Text karty v produkte (slice):** „Žiadanému produktu dochádzajú zásoby.“ Stavy „tento týždeň“ alebo „dnes“, nikdy „hneď“ (to patrí nedostupnosti).
- **Otázka:** Kde uniká hodnota? Sklad, jeden produkt.
- **Dnes v produkte:** V2 slice (nahrádza R3 Hrozí vypredanie); publikovať po nasadení.
- **Hook:** „Bestseller vám dôjde o 9 dní. Dodávateľ dodáva za 14.“
- **Príbeh:** Pri aktuálnej rýchlosti predaja vydrží zásoba kratšie než dodacia lehota. V číslach: [zásoba, predaj za deň, dodacia lehota, rezerva]. Čo to stojí: [ušlá marža za dni výpadku]. Čo urobiť dnes: objednať skôr, zrýchliť dodávku, pripraviť náhrady, obmedziť promo. Ako to Shop Pilot stráži: porovnáva pokrytie zásoby s dodacou lehotou dodávateľa a vašou rezervou; hlási „dnes“, kým sa dá objednať včas.
- **Pozor:** systém nevidí otvorené objednávky u dodávateľa, preto sa karta priamo pýta, či je doplnenie už na ceste. Toto je príbeh o poctivosti: nástroj priznáva, čo nevidí, a spýta sa.
- **Kanál a priorita:** skupiny, cold e-mail. Priorita 1.

#### U4. Dôležitá produktová alebo landing stránka má návštevnosť, ale nepredáva
- **Otázka:** Kde uniká hodnota? Web, jedna stránka.
- **Dnes v produkte:** V1 čiastočne (DR3 Pokles tržieb kvôli konverzii, overiť).
- **Hook:** „Stránka, ktorá predávala, prestala. Ľudia na ňu chodia ďalej.“
- **Príbeh:** Dôležitá stránka mala zdravý výkon, návštevnosť zostala, predaj padol. V číslach: [hodnota na návštevu predtým a teraz]. Čo to stojí: [€ za deň]. Čo urobiť dnes: skontrolovať cenu, popis, fotky, dostupnosť, dôveryhodnosť, výzvu k akcii, varianty a dopravu. Ako to Shop Pilot stráži: sleduje stránky s vlastnou zdravou históriou a vylúči zmenu zloženia návštevnosti, sklad, checkout a chyby merania.
- **Pozor:** nie chronicky slabé stránky (to je príležitosť, nie únik). Nehovoriť „konverzia stránky klesla“.
- **Kanál a priorita:** skupiny. Priorita 2.

#### U5. Košík alebo checkout prepúšťa zákazníkov, ktorí už chceli kúpiť
- **Otázka:** Kde uniká hodnota? Web, nákupný proces.
- **Dnes v produkte:** V1 (DR6 Problémy vo funneli).
- **Hook:** „Zákazník mal tovar v košíku a odišiel. Kde presne?“
- **Príbeh:** Ľudia dôjdu do košíka a checkoutu, dokončených objednávok ubudlo. V číslach: [košík → checkout → objednávka vs. porovnateľné dni]. Čo to stojí: [ušlá marža € za deň]. Čo urobiť dnes: skontrolovať dopravu, platby, chyby, mobilný checkout, kupóny a technické zmeny. Ako to Shop Pilot stráži: porovnáva kroky košíka a checkoutu s objednávkami v Shoptete a s rovnakými dňami v týždni; ak čísla nesedia, hlási meranie.
- **Pozor:** zlyhanie platobnej brány po odoslaní objednávky patrí do „objednávky blokuje platba“ (v Shoptete vzniká objednávka pred platbou). Nie generický pokles konverzie.
- **Kanál a priorita:** skupiny používateľov Shoptetu. Priorita 1.

#### U6. Dôležitá skupina návštevníkov prestala nakupovať
- **Otázka:** Kde uniká hodnota? Web, skupina návštevníkov.
- **Dnes v produkte:** V1 (DR3, DR8 Mobile UX problém).
- **Hook:** „Na mobile ste prestali predávať. Na počítači nie.“
- **Príbeh:** Konkrétna skupina (zariadenie, prehliadač, zdroj) chodí ďalej, ale nekupuje. V číslach: [hodnota na návštevu skupiny predtým a teraz]. Čo to stojí: [€ za deň]. Čo urobiť dnes: skontrolovať skupinu: zariadenie, prehliadač, zdroj a vstupné stránky, produktové stránky, dopravu, platby, UX a technické zmeny. Ako to Shop Pilot stráži: overí, že skupina stále chodí, že objednávky v Shoptete sedia a že nejde len o zmenu zloženia skupiny.
- **Pozor:** malé skupiny najviac „tento týždeň“, nikdy „hneď“. Jedna stránka nie je skupina (to je U4).
- **Kanál a priorita:** skupiny, LinkedIn. Priorita 1.

#### U7. Noví zákazníci sa nevracajú na druhý nákup
- **Otázka:** Kde uniká hodnota? Zákazníci, celý e-shop.
- **Dnes v produkte:** návrh (kohortová vrstva).
- **Hook:** „Kedy váš e-shop prestal robiť druhý nákup?“
- **Príbeh:** E-shop mal historicky [X %] druhých nákupov, nedávne skupiny nových zákazníkov výrazne menej. V číslach: [očakávaná vs. skutočná miera druhého nákupu, počet zákazníkov „po termíne“]. Čo to stojí: [€ za deň zo súčasnej skupiny]. Čo urobiť dnes: nastaviť komunikáciu po nákupe, remarketing, ponuku na druhý nákup alebo reaktivačný postup. Ako to Shop Pilot stráži: len pre e-shopy s preukázaným opakovaným nákupom; očakávanie zafixuje pri otvorení, aby sa „nenaučilo“ únik ako normál.
- **Pozor:** nie pre jednorazový sortiment. Kontakty zákazníkov ostávajú v Shoptete (manuálny export), Shop Pilot ich neukladá.
- **Kanál a priorita:** LinkedIn. Priorita 3.

#### U8. Zákazníci po očakávanom čase neobjednávajú znova
- **Otázka:** Kde uniká hodnota? Zákazníci, produkt s cyklom opakovania.
- **Dnes v produkte:** návrh.
- **Hook:** „Vôňa do prania vydrží [6] týždňov. Kto ju už mal objednať a neobjednal?“
- **Príbeh:** Pre spotrebný tovar s overeným cyklom opakovania existuje skupina zákazníkov „po termíne“. V číslach: [zákazníci po termíne, ich priemerná marža]. Čo to stojí: [€ za deň]. Čo urobiť dnes: pripomenúť nákup (export a párovanie v Shoptete), skontrolovať dostupnosť a ponuku. Ako to Shop Pilot stráži: overený cyklus na úrovni produktu, len zákazníci, ktorí už raz opakovali; ak produkt nie je dostupný, najprv sklad.
- **Pozor:** žiadne automatické rozposielanie; Shop Pilot neukladá kontaktné údaje.
- **Kanál a priorita:** LinkedIn, skupiny (spotrebný tovar, kozmetika, krmivá). Priorita 2 (silný príbeh z Kifra.sk po nasadení).

#### U9. Objednávky končia tesne pod hranicou dopravy zdarma
- **Otázka:** Kde uniká hodnota? Ceny a košík, politika dopravy zdarma.
- **Dnes v produkte:** návrh.
- **Hook:** „Doprava zdarma od 50 €. Priemerná objednávka 46 €. Náhoda?“
- **Príbeh:** Nezvyčajne veľa objednávok končí tesne pod hranicou bez zodpovedajúceho skoku nad ňou. V číslach: [rozdelenie hodnôt objednávok okolo hranice]. Čo to stojí: [ušlá prírastková marža po dotácii dopravy]. Čo urobiť dnes: lepšie zobraziť hranicu, ponúknuť zmysluplné doplnky, prehodnotiť hranicu; neznižovať ju naslepo. Ako to Shop Pilot stráži: testuje tvar rozdelenia okolo hranice a hlási len vtedy, keď sa to oplatí aj po dotácii dopravy.
- **Pozor:** trvalý zhluk objednávok pod hranicou daný sortimentom nie je únik.
- **Kanál a priorita:** skupiny. Priorita 2.

#### U10. Objednávky pripravené na vybavenie čakajú príliš dlho
- **Otázka:** Kde uniká hodnota? Prevádzka, fronta objednávok.
- **Dnes v produkte:** návrh.
- **Hook:** „Zaplatené objednávky, ktoré čakajú v sklade, sú budúce storná.“
- **Príbeh:** Rastie počet objednávok pripravených na expedíciu, ktoré čakajú nad prah. V číslach: [počet, vek, hodnota]. Čo to stojí: [marža v riziku € za deň]. Čo urobiť dnes: vyčistiť backlog, najstaršie a najhodnotnejšie prvé, vyriešiť úzke miesto. Ako to Shop Pilot stráži: počíta len objednávky, ktoré sa dajú vybaviť (dobierka po potvrdení áno); blokované patria inam.
- **Pozor:** dopad je marža v riziku, nie celková hodnota backlogu.
- **Kanál a priorita:** skupiny (predvianočná sezóna). Priorita 2.

#### U11. Objednávky blokuje platba alebo doručenie
- **Otázka:** Kde uniká hodnota? Prevádzka, blokované objednávky.
- **Dnes v produkte:** V1 čiastočne (R-Backorder, overiť).
- **Hook:** „Objednávka existuje, peniaze nie. Napíšte im dnes.“
- **Príbeh:** Objednávky uviazli na nezaplatenej online platbe, zlyhanej platbe alebo doručení. V číslach: [počet, hodnota, vek]. Čo to stojí: [marža v riziku € za deň]. Čo urobiť dnes: poslať platobnú pripomienku alebo nový odkaz, kontaktovať zákazníka, ponúknuť inú platbu či dopravu, opraviť problémovú metódu. Ako to Shop Pilot stráži: rozlišuje dobierku (nie je blokovaná) a online platbu po ochrannej lehote.
- **Pozor:** opustený košík pred odoslaním objednávky patrí do U5.
- **Kanál a priorita:** skupiny používateľov Shoptetu. Priorita 2.

### Kde pritlačiť?

#### P1. Výkonná kampaň má priestor na kontrolované škálovanie
- **Otázka:** Kde pritlačiť? Reklama, jedna kampaň.
- **Dnes v produkte:** návrh (overiť).
- **Hook:** „Kampaň, ktorá zarába po všetkých nákladoch a má rezervu. Pritlačte, ale kontrolovane.“
- **Príbeh:** Kampaň je zisková po nákladoch a brzdí ju rozpočet. V číslach: [zisk na objednávku, podiel stratených zobrazení]. Čo to stojí: [ušlý zisk € za deň, konzervatívne]. Čo urobiť dnes: navýšiť rozpočet postupne, rozšíriť cielenie, pridať kreatívy, otestovať podobné publiká. Ako to Shop Pilot stráži: vyberá len kampane ziskové po nákladoch a bez brzdy v sklade či na webe (nedostupný produkt, stránka, ktorá nepredáva, backlog objednávok).
- **Pozor:** stav „sledovať“ alebo „tento týždeň“, nikdy „hneď“. Neškálovať do vypredania.
- **Kanál a priorita:** LinkedIn. Priorita 2 (dôležité pre rovnováhu: nie sme alarm).

#### P2. Emerging bestseller má rastúci dopyt a zaslúži si podporu
- **Text karty v produkte (slice):** „Produkt rýchlo rastie a stojí za pozornosť.“ Stavy „sledovať“ alebo „tento týždeň“; či sa zobrazuje v rannom zozname alebo len v sekcii príležitostí, je v slice-e otvorené (SLICE-OPEN-05).
- **Otázka:** Kde pritlačiť? Sklad, jeden produkt.
- **Dnes v produkte:** V2 slice (nahrádza R4 Rastúci dopyt); publikovať po nasadení.
- **Hook:** „Produkt, ktorého dopyt rastie, kým si to všimne konkurencia.“
- **Príbeh:** Predaje aj záujem o stránku rastú, produkt je dostupný. V číslach: [rast predajov týždeň k týždňu, marža]. Čo to stojí: [nevyužitý potenciál, konzervatívne]. Čo urobiť dnes: doskladniť, zvýrazniť, zaradiť do kampane, newslettera alebo na homepage. Ako to Shop Pilot stráži: rast dopytu plus dostupnosť; keď pokrytie klesne, prepne na „objednať skôr“ a pri vypredaní na „nedostupný“. Jeden produkt, tri stavy, tri rôzne akcie.
- **Pozor:** ide o konkrétny produkt, nie kategóriu. Nesľubovať „každé ráno príležitosť v top zozname“, kým nie je rozhodnuté, kde sa karta zobrazuje.
- **Kanál a priorita:** skupiny, LinkedIn. Priorita 1 (prvý príbeh o príležitosti).

#### P3. Dôležitá stránka má návštevnosť, ktorú vieš lepšie premeniť na predaj
- **Otázka:** Kde pritlačiť? Web, jedna stránka.
- **Dnes v produkte:** návrh.
- **Hook:** „Stránka s ľuďmi, ale bez predaja. Nie je pokazená, len nič nepredáva.“
- **Príbeh:** Stránka s veľkou návštevnosťou alebo záujmom a slabou monetizáciou: chýbajú produkty, výzvy k akcii, odkazy. V číslach: [návštevy, hodnota na návštevu vs. podobné stránky]. Čo to stojí: [konzervatívny odhad príležitosti]. Čo urobiť dnes: doplniť produkty, výzvy k akcii, interné odkazy, ponuku, dôveryhodnostné prvky. Ako to Shop Pilot stráži: väčšinou v sekcii príležitostí; do ranného zoznamu len s konkrétnou akciou a materiálnou návštevnosťou.
- **Pozor:** nie generický report optimalizácie stránok.
- **Kanál a priorita:** blog. Priorita 3.

#### P4. Hodnotný zákaznícky segment vieš znovu aktivovať
- **Otázka:** Kde pritlačiť? Zákazníci, hodnotná skupina.
- **Dnes v produkte:** návrh.
- **Hook:** „[10] % zákazníkov robí [40] % marže. Kedy ste im naposledy napísali?“
- **Príbeh:** Hodnotná skupina zákazníkov bez nedávneho nákupu, mimo skupín riešených inde. V číslach: [veľkosť skupiny, marža]. Čo to stojí: [príležitosť, konzervatívne]. Čo urobiť dnes: VIP alebo vernostná ponuka, remarketing, oslovenie cez export a párovanie v Shoptete. Ako to Shop Pilot stráži: len keď je skupina materiálna a je pripravená konkrétna akcia; stav „sledovať“ alebo „tento týždeň“.
- **Pozor:** Shop Pilot neukladá kontakty a nikoho neoslovuje; export obsahuje len obmedzené identifikátory na párovanie.
- **Kanál a priorita:** LinkedIn. Priorita 3.

### Doplnková karta (follow-up, nie situácia)

#### D1. Produkt je znovu skladom, ale stále je skrytý
- **Text karty v produkte (slice):** „Produkt je znovu skladom, ale stále je skrytý. Skontroluj, či ho nechceš znovu zviditeľniť.“
- **Otázka:** Kde uniká hodnota? Sklad a viditeľnosť produktu.
- **Dnes v produkte:** V2 slice (Task 010 ju môže z MVP odložiť; overiť pred publikovaním).
- **Hook:** „Skryli ste vypredaný produkt, aby nežral reklamu. Kto vám povie, že je zas skladom?“
- **Príbeh:** Produkt bol skrytý (kvôli reklame, alebo len tak), tovar prišiel, stav skladu je niekoľko dní po sebe kladný, a produkt je stále neviditeľný. Nikto nepredáva, čo nie je vidieť. Čo urobiť dnes: skontrolovať a zviditeľniť. Ako to Shop Pilot stráži: nezávisle od toho, či skrytie odporučil on alebo ste ho urobili sami; čaká, kým je stav skladu stabilne kladný (najmenej 3 dni), aby nehlásil jednodňové výkyvy z vrátených zásielok alebo korekcií; rešpektuje zámerne stiahnuté produkty.
- **Pozor:** nie je to situácia ani alarm, je to pripomienka. Nehlási hneď v prvý deň kladného stavu.
- **Kanál a priorita:** skupiny používateľov Shoptetu (malá, konkrétna, každodenná vec). Priorita 1 po nasadení.

---

## 4. Prierezové príbehy (princípy systému)

Tieto príbehy nie sú o jednej situácii, ale o tom, ako systém uvažuje. Sú kľúčové pre pilier „spoľahlivosť“ a pre odlíšenie od dashboardov a AI chatbotov.

| # | Hook | Jadro príbehu | Dnes v produkte |
|---|---|---|---|
| S1 | „Nie najväčšie číslo, ale najbližší termín.“ | Shop Pilot netriedi podľa výšky sumy, ale podľa termínu rozhodnutia: hneď, dnes, tento týždeň, sledovať. Suma rozhoduje až v rámci rovnakého termínu. Inak by každý malý únik navždy predbehol každú veľkú príležitosť a z poradcu by bol alarm. | V2 slice (pre štyri situácie zo slice-u); zvyšok návrh |
| S2 | „5 € denne môže byť kríza.“ | Prahy sú relatívne k veľkosti e-shopu, nie absolútne. Pre e-shop so 150 tisíc je 5 € denne iné číslo než pre e-shop s 3 miliónmi. Produkt s veľkým podielom na tržbách prejde prahom aj vtedy, keď je denný odhad opatrný. | V2 slice |
| S3 | „Skôr než radí, overí, či sa dá dátam veriť.“ | Ak GA4 hlási pád návštevnosti, ale objednávky v Shoptete bežia normálne, nie je to biznisový problém, ale problém merania. Shop Pilot povie „skontrolujte meranie“, nie „padli vám tržby“. | V1 (DR12 Anomálie v dátach); súlad návštevnosti s objednávkami je návrh |
| S4 | „Reklama nefunguje? Pozrite do skladu.“ | Vypredaný produkt a platená návštevnosť naň sú dve situácie, ktoré systém spojí do jednej karty: nezastavuj kampaň naslepo, problém je sklad. Toto dashboard reklamy nevidí, lebo nevidí sklad. | V2 slice (spojená karta); predtým DR4 |
| S5 | „Jeden produkt, tri stavy, tri akcie.“ | Rastúci dopyt → dochádzajú zásoby → nedostupný. Každý prechod je udalosť, ktorá zruší predchádzajúce „už som to videl“; chronická situácia nikdy neutopí novú krízu. Reálny príbeh: PMAG/VEL, jún 2026 (schválený zakladateľom, viď 4.1). | V2 slice |
| S6 | „Nepošle vašim zákazníkom ani jeden e-mail.“ | Shop Pilot neukladá kontaktné údaje zákazníkov a nikoho neoslovuje. Povie, koho sa oplatí osloviť, oslovenie robíte vy zo Shoptetu. Hranica navrhnutá zámerne. | áno, platí dnes |
| S7 | „Každá akcia má výpočet. Žiadne odhady od AI.“ | Deterministické pravidlá: pri každej akcii vidíte, z akých čísel vznikla. Keď nie sú dáta, systém mlčí, namiesto toho, aby si vymyslel odpoveď. | áno |
| S8 | „Keď sa pokazia tri veci naraz, nespočíta stratu trikrát.“ | Vypredaný produkt a reklama naň sú jedna karta s jedným dopadom, nie dve straty. Systém dopad rozdelí, nie sčíta. | V2 slice (spojená karta); zvyšok návrh |
| S9 | „Ak dnes zlyhá import dát, netvrdí, že problém zmizol.“ | Situácia sa zavrie len vtedy, keď detektor bežal, dáta sú čerstvé a výslovne hlási koniec. Chýbajúce dáta nikdy neznamenajú „vyriešené“. Dashboardy toto nerozlišujú: prázdny graf vyzerá ako pokoj. | V2 slice |
| S10 | „Incident sa stal testom.“ | Dáta z 24. až 30. júna 2026 sú trvalý regresný test: každá nová verzia systému ich musí prehrať správne (otvoriť rast, prepnúť na dochádzajúce zásoby, vyhlásiť krízu pri nedostupnosti, spojiť s reklamou), inak nejde do produkcie. | V2 slice |

### 4.1 Štartovací príbeh: PMAG/VEL (schválený, reálny)

Incident z júna 2026: top produkt Kifra.sk s materiálnym podielom na tržbách sa 26. júna vypredal a pôvodný systém to nehlásil (dopady v eurách s rôznymi časovými oknami, chronické potláčanie, dôležitý produkt podhodnotený denným odhadom). Zakladateľ schválil použitie príbehu. Odporúčané použitie:

1. **LinkedIn, dva diely** (šablóny v `02-sablony-textov.md`, kap. 6): diel 1 „čo sa stalo a prečo systém mlčal“, diel 2 „čo sme zmenili: termín pred sumou, tri stavy, dôležitosť podľa podielu na tržbách, incident ako trvalý test“.
2. **Prípadová štúdia na web** po nasadení slice-u: skutočné karty z prehrávky (shadow výstup pre okno 24. až 30. 6.) ako obrázky: rast → dochádzajú zásoby → nedostupný → spojená karta s reklamou.
3. **Ukážka:** tie isté karty ako „toto je skutočné ráno z 27. júna“. Silnejšie než akékoľvek demo dáta.

Poradie je dôležité: diel 1 sa smie publikovať hneď (je pravdivý dnes), diel 2 a prípadová štúdia až po nasadení slice-u do produkcie, aby text netvrdil, že oprava beží, kým beží v tieňovom režime.

---

## 5. Séria „Čo vám Shop Pilot nepovie (a prečo)“

Zaparkované situácie sú obsah. Chatbot odpovie na všetko; poradca povie, na čo nemá dáta. Každý diel: čo nepovieme → prečo → čo namiesto toho.

| Nepovie | Prečo | Namiesto toho |
|---|---|---|
| „Zvýšte cenu produktu X.“ | Bez dát o cenovej elasticite a konkurencii je to hádanie. | Ukáže maržu, dopyt a zľavy ako kontext; rozhodnutie o cene je vaše. |
| „Predávajte A spolu s B ako balíček.“ | Nemá spoľahlivé dáta o súvisiacich produktoch; nebude hádať z kategórií ani názvov. | Nič. Radšej mlčí, než by odporúčal náhodný balíček. |
| „Tento produkt je sezónny.“ | Sezónnosť sa v prvej verzii nemodeluje; tváriť sa, že áno, by bolo klamstvo. | Porovnáva rovnaké dni v týždni a uzavreté obdobia medziročne tam, kde to dáva zmysel. |
| „Doprava vás stojí priveľa.“ | Nevie, aká je „správna“ cena dopravy bez vašej stratégie, konkurencie a sľubu zákazníkom. | Ukáže náklady na doručenie ako súčasť zisku za deň. |
| „Propagujte produkt, lebo má málo vratiek.“ | Nízke vratky nie sú dôvod na promo; dôvod musí prísť z dopytu alebo marže. | Vratkovosť použije ako podporný signál pri inej príležitosti. |
| „Ste príliš závislí od jedného kanála.“ | To je riziko, nie denná akcia. | Patrí do prehľadu zdravia e-shopu, nie do ranného briefingu. |
| „Konkurencia je lacnejšia.“ | Bez dát o cenách konkurencie. | Mimo rozsahu, kým nebudú dáta o cenách trhu. |
| „Poslali sme vašim zákazníkom pripomienku.“ | Zámerne: Shop Pilot neukladá kontakty a nekomunikuje so zákazníkmi. | Povie, koho osloviť; oslovenie robíte vy. |
| „Kategória X vám predáva zle.“ | Kategórie v e-shopoch nie sú spoľahlivé (každý ich má inak), preto sa nepoužívajú na porovnávanie ani prahy. | Hodnotí konkrétne produkty a stránky. |
| „Problém zmizol.“ (keď chýbajú dáta) | Chýbajúci import nie je vyriešený problém. | Situácia ostáva otvorená, kým detektor výslovne nehlási koniec. |

---

## 6. Plán publikovania (12 týždňov, 2 príspevky týždenne)

Východiská: reálne číslo existuje zatiaľ len pre K1 (približne 1 000 €) a reálny incident pre S5/S10 (PMAG/VEL). Ďalšie čísla prídu z dvoch zdrojov: (a) prehrávka a tieňový výstup slice-u V2 pre okno 24. až 30. 6. dá skutočné karty a dopady pre P2, U3, U2, K3 a D1; (b) história odporúčaní V1 v Looker Studio dá jedno reálne pozorovanie pre U5, U6, U1 a K6. Kým čísla nie sú, publikujú sa príbehy, ktoré ich nepotrebujú: princípy (S3, S7, S9), séria „nepovie“ a diel 1 PMAG/VEL.

| Týždeň | Príspevok A | Príspevok B | Podmienka |
|---|---|---|---|
| 1 | K1 Kampaň s vysokým ROAS, stratová (1 000 €) | S7 Každá akcia má výpočet | žiadna |
| 2 | PMAG/VEL diel 1: top produkt vypredal, systém mlčal | S3 Skôr než radí, overí meranie | žiadna |
| 3 | Nepovie: „Zvýšte cenu“ | S9 Ak zlyhá import, netvrdí, že problém zmizol | žiadna |
| 4 | PMAG/VEL diel 2: čo sme zmenili (S1, S5, S10) | Nepovie: „Balíček A + B“ | slice v produkcii |
| 5 | S4 + K3 + U2 Reklama nefunguje? Pozrite do skladu (skutočná spojená karta) | D1 Produkt je znovu skladom, ale stále skrytý | slice v produkcii, čísla z prehrávky |
| 6 | U3 Žiadanému produktu dochádzajú zásoby (karta sa pýta, či je tovar na ceste) | K6 Kupóny ničia maržu | pozorovanie V1 pre K6 |
| 7 | P2 Produkt rýchlo rastie (prvý príbeh o príležitosti) | S2 5 € denne môže byť kríza | čísla z prehrávky |
| 8 | U5 Košík prepúšťa zákazníkov | Nepovie: „Kategória X predáva zle“ | pozorovanie V1 pre U5 |
| 9 | U1 Z dôležitého zdroja chodí menej ľudí | S6 Nepošle zákazníkom ani jeden e-mail | pozorovanie V1 pre U1 |
| 10 | U6 Na mobile ste prestali predávať | Nepovie: „Produkt je sezónny“ | pozorovanie V1 pre U6 |
| 11 | Prípadová štúdia PMAG/VEL na webe (karty z prehrávky) | S8 Nespočíta stratu trikrát | slice v produkcii |
| 12 | K4 Produkt viaže cash (ak živé; inak S1 samostatne) | Rekapitulácia: štyri otázky majiteľa | – |

Ak slice nebude v produkcii do 4. týždňa, týždne 4, 5, 7 a 11 sa posunú a na ich miesto idú ďalšie diely série „nepovie“ a princípy. Z každého príspevku vzniká zároveň: 1 e-mail do sekvencie, 1 slide do ukážky, 1 krátke video (60 s) a neskôr 1 reklama.

---

## 7. Čo potrebujem od zakladateľa

Vyriešené 18. 9. 2026: stav implementácie (slice V2 + pravidlá V1), súhlas s príbehom PMAG/VEL, lokalizácia názvov (bude), hranica pre kontaktné údaje (platí dnes).

1. **Detaily PMAG/VEL pre diel 1:** názov produktu alebo aspoň jeho podiel na tržbách, koľko dní bol nedostupný, čo v tých dňoch ukazoval pôvodný systém namiesto toho, či naň v tom čase chodila platená návštevnosť. Bez toho sa diel 1 dá napísať len všeobecne.
2. **Po nasadení slice-u: export z tieňových tabuliek** pre okno 24. až 30. 6. (karty, prvá akcia, dopad, dôkazy, história). Z toho vzniknú čísla pre K3, U2, U3, P2, D1, prípadová štúdia a ukážkové karty do dema.
3. **Jedno reálne pozorovanie z histórie V1** pre U5 (košík), U6 (mobil), U1 (zdroj návštevnosti) a K6 (kupóny): dátum, čo pravidlo hlásilo, čo sa s tým urobilo. Zaokrúhlené čísla stačia.
4. **Lokalizované názvy situácií**, keď budú hotové, aby sa karty aktualizovali naraz.
5. **Rozhodnutie SLICE-OPEN-05** (kde sa zobrazuje karta rastúceho produktu), aby text P2 nesľuboval viac, než produkt ukáže.

---

## Zmeny

- **v1.1 (18. 9. 2026):** zapracovaný plán prvého slice-u V2 (skladový reťazec, platená návštevnosť na nedostupný produkt, spojená karta, pripomienka zviditeľnenia, prehrávka PMAG/VEL); texty kariet z produktu pre štyri situácie zo slice-u; nová doplnková karta D1; nové princípy S9 a S10; PMAG/VEL ako schválený štartovací príbeh; hranica pre kontaktné údaje potvrdená; plán publikovania prerobený podľa dostupných reálnych čísel.
- **v1 (18. 9. 2026):** prvý návrh.
