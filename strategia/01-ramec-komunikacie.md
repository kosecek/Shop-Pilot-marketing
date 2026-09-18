# Shop Pilot – rámec komunikácie so zákazníkmi (v1.1)

Stav: návrh, 18. 9. 2026, v1.1 po zapracovaní odpovedí zakladateľa (cena, integrácie, trhy, referencia, spôsob ukážky).
Cieľ dokumentu: dostať majiteľa e-shopu od „nepoznám vás“ k „chcem vidieť ukážku“ a dať tejto ceste jednotný jazyk.

**Rozhodnutia a fakty, na ktorých dokument stojí (18. 9. 2026):**

| Téma | Stav |
|---|---|
| Cena | 100 € mesačne, jedno pásmo (MVP); ďalšie pásma neskôr |
| Integrácie | Shoptet + Google Ads + Meta Ads + GA4 + faktúry, sklad a fixné náklady; ďalšie platformy v pláne |
| Trhy | Slovensko a Česko ako prvé, potom medzinárodne |
| Referencie | Zatiaľ len Kifra.sk: Shop Pilot odhalil kampaň s vysokým ROAS, ktorá bola v skutočnosti stratová; úspora približne 1 000 € |
| Ukážka | Na mierne upravených reálnych dátach Kifra.sk. Prepojenie dát záujemcu nie je automatizované (niekoľko hodín ručnej práce), preto sa robí až v pilote |
| Hosting | Google Cloud, každý zákazník má vlastného tenanta (oddelené prostredie); región overiť |

---

## 0. Zhrnutie na jednu stranu

1. **Nepredávame dashboard ani analytiku. Predávame denné rozhodnutie:** „čo dnes urobiť, aby e-shop zarobil viac“. Kategória, ktorú obsadzujeme: **denný poradca (kopilot) pre e-shopy na Shoptete.** Dashboardy sú podpora, nie hlavné posolstvo. Medzinárodná mapa konkurencie ukazuje, že v kategórii „dashboard/reporting“ začína cena na 35 USD mesačne a nikto tam nevyhráva na kvalite.
2. **Nepriateľ v komunikácii: riadenie podľa pocitu a podľa ROAS.** Majiteľ vidí tržby a ROAS, ale nevie, koľko včera skutočne zarobil, a nevie, ktorá z dvadsiatich vecí je dnes najdôležitejšia. Náš vlastný dôkaz: kampaň s vysokým ROAS, ktorá bola stratová, úspora približne 1 000 €.
3. **Najsilnejší hook: ukázať mu číslo o jeho e-shope, ktoré nepozná.** Skutočný denný zisk a cena nekonania. Nie sľuby, konkrétny výpočet, ktorý si vie overiť.
4. **Žiadosť o prezentáciu prerámcujeme na „ukážku rána s Shop Pilotom“:** 20 minút, na reálnych číslach reálneho e-shopu (Kifra.sk), záujemca nič nepripravuje. To, že ukážka nebeží na jeho dátach, nie je slabina, ale nízky prah: žiadne prístupy, žiadna práca. Jeho vlastné dáta prídu v pilote, ktorý je platený, a preto sa ručný onboarding oplatí.
5. **Motor obsahu: každé pravidlo expertného systému = jeden príbeh** (situácia → čo to stojí → čo urobiť dnes). Desiatky pravidiel znamenajú desiatky konkrétnych, overiteľných príspevkov, e-mailov a neskôr reklám bez vymýšľania.
6. **Hlas: e-shopár e-shopárom.** Zakladateľ s vlastným e-shopom (Kifra.sk) hovorí v prvej osobe a s číslami. Vizuál ostáva prémiový podľa brand manuálu, tón je vecný a ľudský.
7. **Cieľovka je ostrá: e-shopy na Shoptete v SK a CZ s obratom 150 tis. – 3 mil. €, ktoré platia za Google alebo Meta reklamu.** Shoptet je zároveň kvalifikačný filter, personalizačný háčik v outbounde aj distribučný kanál (skupiny používateľov, doplnky). Záujemcov mimo Shoptetu zbierame na čakaciu listinu podľa platformy, čo určí poradie ďalších integrácií.
8. **Cena 100 € mesačne, transparentne, ukotvená vlastným príbehom:** „Jedna zle nastavená kampaň ma stála približne 1 000 €. Shop Pilot stojí 100 € mesačne.“ Sedí presne medzi lacné profit aplikácie (35 – 149 USD) a atribučné platformy (od 219 USD).
9. **Kanály na prvých 90 dní:** (a) predkvalifikovaný outbound na Shoptet e-shopy s aktívnou reklamou, (b) obsah z pravidiel v skupinách e-shopárov a používateľov Shoptetu a na LinkedIn, (c) partneri – Shoptet, účtovníci, konzultanti, (d) Upterdam a podobné podujatia. Platená reklama až po overení hookov.

---

## 1. Východiská

### 1.1 Čo predávame (fakty o produkte)

- Zber dát zo Shoptetu, Google Ads, Meta Ads, GA4, faktúr, skladu a dôležitých fixných nákladov v nočnom cykle.
- Skutočný zisk za každý deň (po reklame, tovare, doprave a fixných nákladoch).
- Deterministický expertný systém: vyhodnotí dáta, prioritizuje a každý deň vyberie najdôležitejšie akcie. Pri každej akcii: čo urobiť, z čoho to vyplýva, prečo je to dôležité a aký je finančný dopad nekonania.
- Dashboardy na detail, keď treba rozhodnutie podložiť alebo vykonať.
- V pláne: MCP rozhranie – otázky na vlastné dáta ľudskou rečou cez LLM; ďalšie e-shopové platformy.
- Cena: 100 € mesačne, jedno pásmo.
- Hosting: Google Cloud, každý zákazník má vlastného tenanta; prístupy k zdrojom read-only, kde to zdroj umožňuje.
- Hodnoty: akurátnosť (relevantné, hodnotné návrhy) a spoľahlivosť (žiadne halucinácie, dá sa na to spoľahnúť).
- Dôkaz z praxe: na Kifra.sk odhalil kampaň s vysokým ROAS, ktorá bola po započítaní nákladov stratová; úspora približne 1 000 €.

### 1.2 Čo z toho je komunikačne unikátne

| Vlastnosť produktu | Čo z toho má zákazník | Ako to povedať |
|---|---|---|
| Denný zoznam prioritizovaných akcií | Nemusí každé ráno prehrabávať päť nástrojov a rozhodovať sa podľa pocitu | „Každé ráno tri veci, ktoré dnes urobiť.“ |
| Finančný dopad nekonania pri každej akcii | Vie, čo ho stojí odklad; vie si zoradiť deň | „Vypredaný bestseller s bežiacou kampaňou vás stojí X € denne.“ |
| Skutočný denný zisk | Prvýkrát vidí zisk denne, nie o mesiac z účtovníctva | „Koľko ste zarobili včera? Nie tržby. Zisk.“ |
| Determinizmus a vysledovateľnosť | Môže tomu veriť, vidí dáta za každým návrhom | „Žiadne AI halucinácie. Každý návrh ukáže čísla, z ktorých vznikol.“ |
| Reklama + predaj + sklad + náklady na jednom mieste | Reklamu posudzuje podľa zisku a skladu, nie podľa ROAS | „ROAS nestačí. Rozhodujte podľa zisku a skladu.“ |
| Vyvinuté majiteľom e-shopu pre vlastný e-shop | Dôvera: „vie, čo riešim“ | „Postavil som to pre svoj e-shop. Teraz ho dávam vám.“ |
| Integrácia so Shoptetom | Nič nemení, pripojí to, čo má | „Pre e-shopy na Shoptete. Pripojíte a ráno máte briefing.“ |
| Vlastný tenant na Google Cloud | Jeho dáta sú oddelené od ostatných zákazníkov, nikto iný ich nevidí | „Vaše dáta bežia vo vlastnom oddelenom prostredí na Google Cloud.“ |

### 1.3 Signály z trhu (program Upterdam 2026)

Program konferencie potvrdzuje, že „zisk namiesto ROAS“ a „riadenie podľa dát a cash-flow“ sú živé témy: prednášky „ROAS nestačí: Ako zistiť, čo marketing naozaj priniesol“ (Dedoles), „Ako riadiť zisk a cashflow vo vlastnej firme“ (Roivis), „Koľko si môžete dovoliť rásť?“, „Načo som sa mal pozerať pred krízou?“ (zakladateľ Dedoles).

Dva dôsledky: (1) publikum je na tému pripravené, nemusíme ju vysvetľovať od nuly; (2) hovoria o nej konzultanti a CFO, teda ľudia, ktorých si menší e-shop nemôže dovoliť. Shop Pilot dáva tú istú disciplínu do rúk majiteľovi každý deň bez konzultanta.

---

## 2. Komu hovoríme

### 2.1 Ideálny zákazník (ICP)

- **E-shop na Shoptete** (jediná podporovaná platforma v MVP; zároveň najrozšírenejšia platforma v našom segmente v SK a CZ).
- Ročné tržby 150 tis. – 3 mil. €, Slovensko a Česko.
- Aktívne investuje do Google Ads a/alebo Meta Ads (má z čoho optimalizovať a má dáta).
- Vlastný sklad alebo vlastný tovar (skladové pravidlá majú zmysel).
- Rozhoduje majiteľ (menšie e-shopy) alebo manažér e-shopu (väčšie).
- Bolesť: dáta v piatich a viac nástrojoch, zisk vidí až z účtovníctva, reklamu hodnotí cez ROAS, rozhoduje podľa pocitu, nemá čas.

### 2.2 Tri segmenty podľa veľkosti (rôzne bolesti, rovnaký produkt)

| Segment | Kto rozhoduje | Typický deň | Hlavná bolesť | Vstupné posolstvo |
|---|---|---|---|---|
| **A: 150 – 500 tis. €** | Majiteľ robí všetko sám | Balí, odpovedá zákazníkom, večer pozerá Ads | „Neviem, či som po reklame v pluse. Nemám čas analyzovať.“ | „5 minút ráno namiesto hodiny večer. A vidíte zisk, nie tržby.“ |
| **B: 500 tis. – 1,5 mil. €** | Majiteľ + 1 až 3 ľudia, PPC agentúra alebo freelancer | Rieši sklad, dodávateľov, agentúru | „Agentúra hlási ROAS, ja neviem, čo mi to reálne prinieslo. Sklad mi viaže peniaze.“ | „Kontrola nad agentúrou aj skladom na jednom mieste, podľa zisku.“ |
| **C: 1,5 – 3 mil. €** | Manažér e-shopu alebo majiteľ v úlohe CEO | Tím, porady, reporty v Sheets alebo Power BI | „Reporty máme, ale nikto z nich nevyťahuje akcie. Rozhodnutia meškajú.“ | „Z reportov k akciám: každý deň zoznam priorít pre tím, s dopadom v eurách.“ |

**Odporúčanie na štart: segment B ako hlavný.** Má najsilnejšiu bolesť (ROAS verzus zisk, sklad), rozpočet, jedného rozhodovateľa a 100 € mesačne je preňho pod prahom rozhodovania. Segment A je objemovo najväčší a najlacnejší na oslovenie (skupiny na Facebooku, príbeh zakladateľa naň sedí najlepšie), ale je citlivejší na cenu; oslovujeme ho obsahom. Segment C je najlukratívnejší, ale má dlhší predajný cyklus; prichádza cez partnerov a referencie.

### 2.3 Persona: „Majiteľ Martin“ (segment B)

- E-shop s doplnkami výživy na Shoptete, obrat 900 tis. €, 2 zamestnanci na sklade a podpore, PPC rieši freelancer.
- Ráno: mobil, objednávky za noc v Shoptete, potom Google Ads, Meta, GA4 a Excel so skladom. 40 minút, žiadna odpoveď na otázku „čo dnes“.
- Otázky, ktoré si kladie: Som po reklame v pluse? Čo mám objednať a kedy? Prečo klesla konverzia? Robí freelancer to, čo má? Koľko mi viaže sklad?
- Kde je: skupiny e-shopárov a používateľov Shoptetu na Facebooku, Upterdam a Reshoper, newslettre o e-commerce, LinkedIn občas.
- Čomu neverí: sľubom o AI, agentúrnym reportom, „ďalšiemu nástroju, ktorý budem musieť plniť“, novej firme bez referencií.
- Čo ho presvedčí: konkrétne číslo z reálneho e-shopu, príbeh iného e-shopára, jasná cena, dôkaz, že mu to čas berie a nie pridáva, možnosť skončiť kedykoľvek.

### 2.4 Koho neoslovujeme (negatívny ICP)

- **E-shopy mimo Shoptetu** (zatiaľ): neoslovujeme aktívne, ale na webe im ponúkneme čakaciu listinu podľa platformy. Dopyt z listiny určí poradie ďalších integrácií.
- Predaj len cez marketplace (bez vlastného webu a reklamy).
- E-shopy bez platenej reklamy (v prvom kroku nemáme čo optimalizovať).
- Čistý dropshipping bez skladu: čiastočný fit, nie prioritný.
- Firmy s BI tímom a obratom nad 3 mil. €: iný nákupný proces, iná konkurencia (dátové platformy).

---

## 3. Pozicionovanie

### 3.1 Pozičné prehlásenie

> **Pre** majiteľov a manažérov menších e-shopov na Shoptete (150 tis. – 3 mil. €), ktorí riadia e-shop popri všetkom ostatnom a každé ráno riešia, čo je dnes najdôležitejšie,
> **je Shop Pilot** denný poradca (kopilot) pre e-shop,
> **ktorý** každé ráno z dát o reklame, predaji, sklade a nákladoch vyberie najdôležitejšie akcie na dnešný deň a pri každej povie, prečo, z čoho vyplýva a čo stojí odklad.
> **Na rozdiel od** dashboardov, ktoré ukážu grafy, a AI asistentov, ktorí si môžu vymýšľať,
> **Shop Pilot** pracuje deterministicky, každé odporúčanie je vysledovateľné k dátam a zisk počíta za každý deň, nie raz za mesiac. Pripojí sa na Shoptet, Google Ads, Meta Ads a GA4; nič nemeníte.

Jednovetový claim pre všetko ostatné:

> **Dashboard ukáže, čo sa stalo. Shop Pilot povie, čo s tým dnes urobiť.**

### 3.2 Kategória: v čom súťažíme a v čom nie

Vychádza z mapy konkurencie (`konkurencia/`), doplnené o lokálne alternatívy, s ktorými zákazník reálne porovnáva.

| Kategória | Kto tam je | Cena (verejná, mesačne) | Prečo v nej (ne)súťažiť |
|---|---|---|---|
| Štatistiky platformy | Shoptet (Štatistiky, doplnky) | v cene platformy | Nesúťažiť. Sú to naše vstupné dáta, nie konkurent. Ukazujú tržby a objednávky, nie zisk po všetkých nákladoch ani denné priority. |
| GA4, Looker Studio, agentúrne reporty | agentúry, freelanceri | zadarmo alebo v cene agentúry | Nesúťažiť ako „lepší report“. Ukazujú, čo sa stalo, hodnotia cez ROAS. |
| Profit-first Shopify aplikácie | TrueProfit, Lifetimely | 35 – 149 USD | Čiastočná konkurencia v segmente A. Počítajú zisk a P&L, ale nehovoria, čo urobiť, nesledujú sklad a nemajú Shoptet. Nesúťažiť cenou, súťažiť akciami a lokálnosťou. |
| Atribučná a operačná vrstva pre DTC | Triple Whale, Out Of The Blue | 199 – 749+ USD, podľa GMV | Najbližší produktový presah (alerty, AI operátor Moby). Sú stavané pre značky s vlastným performance tímom, Shopify a angličtinu. Súťažiť zrozumiteľnosťou, deterministickými akciami a cenou pod ich vstupom. |
| Dátové platformy a BI | Daasity | 1 499 – 1 999+ USD | Nie náš segment. Ich klienti sú nad 3 mil. €. Nepokúšať sa o „data platform“ jazyk. |
| Finančné riadenie ako služba | typ Roivis | individuálne, ľudia | Partner, nie konkurent. Mesačný pohľad cez účtovníctvo; my dopĺňame denný pohľad. |
| Dátové projekty na mieru | typ Stratodata (BigQuery) | projekt v tisícoch € | Nie náš segment; ich odmietnutí klienti sú náš segment C. |
| AI asistenti nad dátami | Moby (Triple Whale), všeobecné LLM nad exportmi | v rámci balíka | Súťažiť priamo: „deterministické, vysledovateľné, bez halucinácií“. Naše MCP rozhranie komunikovať až keď existuje a vždy ako vrstvu nad overenými výpočtami. |

**Cena 100 € mesačne, jedno pásmo.** Sedí presne tam, kam mapa konkurencie ukazuje priestor: nad profit aplikácie (35 – 149 USD, len výkaz zisku) a pod atribučnú vrstvu (od 219 USD, vyžaduje performance tím). Komunikujeme ju otvorene na webe (segment neznáša „kontaktujte nás“) a vždy s kotvou: „jedna zle nastavená kampaň s vysokým ROAS ma stála približne 1 000 €“. Pre český trh uvádzať aj cenu v Kč (prepočítať aktuálnym kurzom a zaokrúhliť). Keď pribudnú pásma, prví zákazníci si nechajú pôvodnú cenu (viď 6.4, zakladajúci zákazníci).

### 3.3 Porovnávacia tabuľka pre web (návrh)

| | Štatistiky platformy / GA4 | Profit aplikácie (Shopify) | Atribučné platformy (DTC) | **Shop Pilot** |
|---|---|---|---|---|
| Skutočný zisk za deň (po reklame, tovare, doprave, fixných nákladoch) | nie | áno | čiastočne | **áno** |
| Sklad a zásoby v rozhodovaní | nie | nie | nie | **áno** |
| Každé ráno prioritizované akcie s cenou nekonania | nie | nie | alerty | **áno** |
| Vysvetlenie každej akcie (z čoho, prečo) | – | – | AI chat | **deterministicky, s dátami** |
| Shoptet, SK/CZ faktúry a sklad | áno (vlastné) | nie | nie | **áno** |
| Jazyk a mena | SK/CZ | EN, USD | EN, USD | **SK/CZ, EUR a Kč** |
| Potrebný tím | – | – | performance tím | **majiteľ, 5 minút ráno** |
| Cena mesačne | v cene platformy | 35 – 149 USD | 199 – 749+ USD | **100 €** |

Presné zaškrtnutia overiť proti aktuálnym funkciám konkurentov pred zverejnením (ceny a funkcie sa menia, viď upozornenie v mape konkurencie).

### 3.4 Nepriateľ (proti čomu stojíme)

- **Riadenie podľa pocitu.** Rozhodnutia bez čísel, lebo čísla sú v šiestich záložkách.
- **ROAS ilúzia.** ROAS 4 vyzerá dobre; po tovare, doprave, poplatkoch a fixných nákladoch môže byť zisk nula. Na Kifra.sk to bola stratová kampaň s vysokým ROAS a približne 1 000 €.
- **Zisk o mesiac neskôr.** Účtovníctvo povie, ako to dopadlo, keď sa už nedá nič zmeniť.
- **Ďalší nástroj, ďalší graf.** Reporting, ktorý nikto nečíta a z ktorého nikto nevyťahuje akcie.
- **AI, ktorá si vymýšľa.** Odpoveď znie sebavedomo, ale nedá sa overiť.

### 3.5 Ako hovoríme o AI

- Hlavné posolstvo nestojí na AI. Trh je presýtený „AI-powered“ a naša výhoda je práve spoľahlivosť.
- Expertný systém opisujeme ako „pravidlá overené v praxi e-shopu, ktoré počítač každú noc aplikuje na vaše dáta“: deterministicky, bez halucinácií, s výpočtom pri každej akcii.
- LLM/MCP rozhranie (plán) komunikujeme až keď existuje, ako „opýtajte sa svojich dát ľudskou rečou“, vždy s dodatkom, že odpovede vychádzajú z tých istých overených výpočtov.
- Nikdy netvrdiť „AI odporúčania“ tam, kde ide o pravidlá. Presnosť pomenovania je súčasť hodnoty „spoľahlivosť“.

---

## 4. Posolstvá (message house)

### 4.1 Strecha

> **Každé ráno viete, čo urobiť, aby váš e-shop zarobil viac.**

Brandový claim „Always two steps ahead“ (v slovenčine „Vždy o dva kroky vpred“) používame ako podpis pod logom, nie ako hlavný titulok. Majiteľ chce najprv vedieť, čo z toho má. Kvalifikátor „pre e-shopy na Shoptete“ patrí do podtitulku alebo hneď pod hero, aby sa návštevník sám zaradil.

### 4.2 Tri piliere a dôkazy

**Pilier 1: Jedno miesto, jedno číslo: skutočný denný zisk.**
- Shoptet, reklama, sklad a náklady v jednom pohľade.
- Zisk za každý deň, nie tržby a nie ROAS.
- Dôkazy: skutočný screenshot ranného prehľadu; prepočet „ROAS 4 → zisk 0“ na príklade; zoznam integrácií.

**Pilier 2: Denný zoznam priorít, nie ďalší graf.**
- Každé ráno 3 až 5 akcií zoradených podľa finančného dopadu.
- Pri každej: čo urobiť, prečo, z čoho to vyplýva, čo stojí nekonanie.
- Dôkazy: ukážka jednej konkrétnej akcie s výpočtom; počet pravidiel v systéme; príbeh stratovej kampane s vysokým ROAS z Kifra.sk (úspora približne 1 000 €).

**Pilier 3: Spoľahlivé, vysledovateľné, bez halucinácií.**
- Deterministický expertný systém, žiadne generované odhady.
- Každé odporúčanie ukáže dáta, z ktorých vzniklo.
- Read-only prístupy, ktoré kedykoľvek zrušíte; dáta bežia na Google Cloud, každý zákazník má vlastného tenanta (oddelené prostredie); región uviesť po overení.
- Dôkazy: „ukážte mi výpočet“ priamo v ukážke; verejne opísaná metodika; ukážka na reálnych dátach zakladateľovho e-shopu, nie na vymyslených.

### 4.3 Verzie pitchu

- **5 slov:** „Každé ráno viete, čo robiť.“
- **1 veta:** Shop Pilot každé ráno vyberie z dát o reklame, predaji, sklade a nákladoch najdôležitejšie akcie pre váš e-shop na Shoptete a povie, koľko vás stojí, keď ich neurobíte.
- **30 sekúnd (výťah):** „Mám e-shop s vôňami do prania na Shoptete. Každé ráno som otváral Google Ads, Metu, Analytics, sklad a faktúry a aj tak som nevedel, či som včera zarobil a čo mám dnes riešiť. Tak som si postavil systém, ktorý to v noci pospája, spočíta skutočný zisk za deň a ráno mi dá tri veci, ktoré mám urobiť, aj s tým, koľko ma stojí, keď ich odložím. Hneď na začiatku mi odhalil kampaň s vysokým ROAS, ktorá bola stratová; ušetril som asi tisíc eur. Volá sa Shop Pilot a dnes ho dávam ďalším e-shopom na Shoptete.“
- **2 minúty:** príbeh (30 s) + stratová kampaň s vysokým ROAS ako pravidlo s číslami (30 s) + ako vyzerá ráno s Shop Pilotom (30 s) + čo je ukážka a čo je pilot (30 s).

### 4.4 Tón a jazyk

**Robíme:** konkrétne čísla, krátke vety, vykanie na webe a v e-mailoch, prvá osoba zakladateľa v komunitách a na LinkedIn, slovenské výrazy (zisk, marža, sklad, náklady), bolesť pomenovať priamo, vždy ukázať výpočet, o ukážke hovoriť pravdivo („reálne dáta môjho e-shopu, niektoré hodnoty upravené“).

**Nerobíme:** „AI-powered“, „revolučný“, „all-in-one platforma“, „business intelligence“, „dashboard“ ako hlavné slovo, „insights“, „actionable“, sľuby percent rastu bez zdroja, porovnávanie s konkurentmi, ktorých zákazník nepozná, sľuby integrácií, ktoré ešte nie sú.

**Slovník značky (pilotná metafora z brand manuálu, používať striedmo a konzistentne):**

| Pojem | Čo znamená |
|---|---|
| Ranný briefing | denný zoznam prioritizovaných akcií (hlavný výstup produktu) |
| Kokpit | dashboardy na detail |
| Predletová kontrola | prvý krok pilotu: prepojenie Shoptetu a reklamných účtov a prvý ranný briefing na dátach zákazníka |

---

## 5. Ako zaujať: hooky a magnety

### 5.1 Princíp

Majiteľ e-shopu nechce prezentáciu softvéru. Chce vedieť o svojom e-shope niečo, čo nevie. Preto každý hook je konkrétne zistenie alebo výpočet, ktorý si vie overiť, spojený s otázkou, ktorá ho zneistí („Viete, koľko ste zarobili včera?“). Produkt spomíname až na konci, ako spôsob, akým sa to dá strážiť každý deň.

### 5.2 Päť hookov na otestovanie

| # | Hook | Text (jadro) | Segment | Kanál | Čo meriame |
|---|---|---|---|---|---|
| 1 | Skutočný zisk | „Viete, koľko ste zarobili včera? Nie tržby. Zisk po reklame, tovare, doprave a fixných nákladoch. Väčšina e-shopov to zistí o mesiac z účtovníctva.“ | A, B | skupiny, LinkedIn, cold e-mail | odpovede, kliky na kalkulačku |
| 2 | Cena nekonania | „Bestseller vypredaný, kampaň naň beží ďalej. Každý deň platíte za kliky, ktoré nemôžu skončiť nákupom.“ (doplniť reálne číslo z Kifra.sk) | B, C | cold e-mail, skupiny, neskôr reklama | odpovede, žiadosti o ukážku |
| 3 | ROAS ilúzia | „Moja najlepšia kampaň podľa ROAS bola stratová. Zistil som to, až keď som si zisk spočítal po všetkých nákladoch. Stálo ma to asi 1 000 €.“ | B | LinkedIn, skupiny, blog (break-even ROAS), webinár | kliky, kalkulačka, ukážky |
| 4 | 5 minút ráno | „40 minút denne preklikávania Ads, Meta, GA4 a skladu. Alebo 5 minút a tri veci, ktoré dnes urobiť.“ | A | skupiny, krátke video | zhliadnutia, odpovede |
| 5 | E-shopár e-shopárom | „Postavil som to pre svoj e-shop s vôňami do prania, lebo som ráno nevedel, čo riešiť. Teraz to dávam ďalším e-shopom na Shoptete.“ | A, B | LinkedIn, podcasty, konferencie | dosah, pozvania, ukážky |

Po dvoch týždňoch testu ide víťazný hook do hero titulku na webe, do predmetu cold e-mailov a neskôr do reklamy. Hook 3 je jediný s reálnym číslom, preto ho odporúčam nasadiť ako prvý.

### 5.3 Magnety (hodnota výmenou za kontakt)

1. **Ukážka „ráno s Shop Pilotom“** (20 minút, video-hovor): hlavná výzva k akcii. Beží na mierne upravených reálnych dátach Kifra.sk, záujemca nič nepripravuje ani nezdieľa. Scenár v kapitole 6.3.
2. **Kalkulačka skutočného zisku a break-even ROAS** (web alebo Google Sheet): zákazník zadá tržby, nákup tovaru, dopravu, poplatky, reklamu a fixné náklady, dostane denný zisk, break-even ROAS a koľko ho stojí jeden deň s bežiacou kampaňou na vypredaný produkt. Zbiera e-mail. Prácnosť 1 až 2 dni. Zároveň SEO cieľ („break-even ROAS“, „výpočet zisku e-shopu“, „POAS“).
3. **Checklist „12 tichých únikov zisku v e-shope“** (jedna strana PDF): odvodený z pravidiel expertného systému. Lacný, na zber e-mailov v skupinách a ako rozlúčka v outbounde.
4. **Čakacia listina pre e-shopy mimo Shoptetu:** formulár s výberom platformy. Nie je to magnet na predaj, ale na meranie dopytu po ďalších integráciách.
5. **Neskôr, po automatizácii onboardingu: bezplatná analýza na dátach záujemcu** („3 akcie do 3 dní“). Dnes by stála niekoľko hodín ručnej práce na jedného záujemcu, preto ju nechávame na fázu, keď bude prepojenie Shoptetu a reklamných účtov samoobslužné.

### 5.4 Motor obsahu: pravidlá → príbehy

Každé pravidlo expertného systému prepíšeme do jednotného formátu:

1. **Situácia** (čo sa v e-shope deje).
2. **Ako to vyzerá v číslach** (mini-príklad, ideálne z Kifra.sk).
3. **Čo to stojí** (dopad nekonania za deň alebo týždeň).
4. **Čo urobiť dnes.**
5. **Ako to Shop Pilot stráži** (jedna veta na konci, nie na začiatku).

Prvý príbeh je hotový: kampaň s vysokým ROAS, ktorá bola po započítaní tovaru, dopravy a poplatkov stratová, a približne 1 000 € úspory po jej oprave. Ďalšie témy (nahradiť reálnymi pravidlami zo systému): kampaň beží na vypredaný produkt; produkt s najvyšším podielom reklamy má po nákladoch zápornú maržu; zásoba bestselleru vydrží 9 dní pri dodacej lehote 14 dní; mŕtve zásoby viažu X € hotovosti; konverzný pomer klesol tri dni po sebe pri rovnakej návštevnosti; CPC v Meta vyskočilo o 40 % týždeň k týždňu; náklady na dopravu na objednávku rastú rýchlejšie než priemerná objednávka.

Výstup z jedného pravidla: 1 príspevok (Facebook alebo LinkedIn) + 1 e-mail do sekvencie + 1 slide do ukážky + neskôr 1 reklama. Pri 40 pravidlách je to obsah na rok bez vymýšľania a každý kus je overiteľný, čo je v súlade s hodnotou „spoľahlivosť“.

---

## 6. Cesta k žiadosti o ukážku

### 6.1 Prerámcovanie výzvy k akcii

Nie „Vyžiadajte si prezentáciu“, ale:

- **Primárne:** „Chcem vidieť ráno s Shop Pilotom“ (20 minút, reálne čísla reálneho e-shopu, nič nepripravujete).
- **Sekundárne:** „Vypočítať skutočný zisk“ (kalkulačka).
- **Terciárne:** „Pozrieť 3-minútové video“ (skrátená ukážka pre tých, čo nechcú hovor).

Dôvody: nízke vnímané riziko, žiadna práca na strane záujemcu, zvedavosť. „Prezentácia“ znie ako predajná schôdzka; „ukážka rána“ znie ako niečo, čo si pozrie pri káve. To, že ukážka nebeží na jeho dátach, komunikujeme otvorene a ako výhodu: „nič nemusíte zdieľať ani pripravovať; vaše dáta prídu na rad v pilote“. Otázka na začiatok každej ukážky (prevzatá z mapy konkurencie): **„Aké tri rozhodnutia dnes robíte v Exceli alebo cez päť oddelených nástrojov?“**

### 6.2 Lievik: čo dostane zákazník v ktorej fáze

| Fáza | Stav v hlave zákazníka | Čo dostane | Kanál | Výzva | Metrika |
|---|---|---|---|---|---|
| Pozornosť | „Hm, to je o mne.“ | hook z pravidla | skupiny, LinkedIn, cold e-mail, konferencia | prečítať, odpovedať | dosah, odpovede, kliky |
| Záujem | „Koľko som zarobil včera?“ | kalkulačka alebo checklist | landing page | zadať e-mail | návštevník → kontakt |
| Dôvera | „Nie je to ďalší AI nezmysel? Nie sú to nováčikovia?“ | 3-min video, metodika, príbeh stratovej kampane, príklad pravidla | e-mailová sekvencia (5 správ) | pozrieť, odpovedať | otvorenia, kliky, odpovede |
| Žiadosť o ukážku | „Chcem to vidieť.“ | ukážka rána s Shop Pilotom na dátach Kifra.sk | formulár, rezervačný kalendár | rezervovať | kontakt → ukážka |
| Ukážka | „Toto by som chcel na svojich číslach.“ | scenár 6.3; na konci ponuka pilotu | video-hovor 20 až 30 min | pilot za 100 € mesačne | ukážka → pilot |
| Pilot (Predletová kontrola) | „Bez toho ráno už nezačnem.“ | prepojenie Shoptetu a reklamných účtov, prvý ranný briefing do X dní, 2 kontrolné hovory | produkt | pokračovanie predplatného | pilot → platiaci po 1. mesiaci |

### 6.3 Scenár ukážky (20 až 30 minút)

Ukážka beží na mierne upravených reálnych dátach Kifra.sk. Na otázku, či sú to reálne čísla, odpovedáme pravdivo: „reálne dáta môjho e-shopu, niektoré hodnoty sú upravené kvôli obchodnému tajomstvu“.

| Minúty | Čo sa deje | Cieľ |
|---|---|---|
| 0 – 5 | Otázka: „Aké tri rozhodnutia dnes robíte v Exceli alebo cez päť nástrojov?“ Zapísať ich. Krátko: platforma, reklamné kanály, kto rieši PPC, sklad. | Zistiť jeho bolesti, kvalifikovať (Shoptet? reklama?), získať slová, ktorými to opisuje |
| 5 – 8 | Príbeh: ráno pred Shop Pilotom (päť záložiek, 40 minút) a stratová kampaň s vysokým ROAS, približne 1 000 €. | Dôvera cez vlastnú skúsenosť |
| 8 – 18 | Ranný briefing naživo: 3 až 5 akcií, pri každej čo, z čoho, prečo, dopad. Ukázať kliknutie do kokpitu na jednu z nich. Pri každej akcii sa spýtať: „Stalo sa vám to niekedy?“ | Nech vidí svoj e-shop v našich dátach |
| 18 – 22 | Vrátiť sa k jeho trom rozhodnutiam: ktoré pravidlá by ich pokrývali; čo by videl ráno on. | Preklopenie z „pekné“ na „moje“ |
| 22 – 27 | Ponuka pilotu (6.4): čo treba z jeho strany, kedy uvidí prvý briefing, cena, garancia, zakladajúci zákazníci. Dohodnúť termín onboardingu hneď na hovore. | Záväzok s termínom |
| 27 – 30 | Otázky. Po hovore do hodiny e-mail s rekapituláciou a odkazom na prístupy. | Neprerušiť tempo |

### 6.4 Ponuka pilotu a program zakladajúcich zákazníkov (návrh na rozhodnutie)

Ručný onboarding stojí niekoľko hodín. Preto ho robíme len pre záujemcov, ktorí sa zaviažu, a záväzok je platba od prvého mesiaca. Aby bol záväzok ľahký, pridáme garanciu a výhody pre prvých zákazníkov.

- **Pilot:** 30 dní za 100 €, platba vopred. Zo strany zákazníka: prístup k Shoptetu (API), Google Ads, Meta Ads a GA4 (read-only, kde sa dá), zoznam fixných nákladov, 30-minútový onboarding hovor. Z našej strany: prvý ranný briefing do X pracovných dní od získania prístupov, dva kontrolné hovory (po 1. a po 4. týždni).
- **Garancia (odporúčam):** „Ak Shop Pilot za prvý mesiac nenájde aspoň jednu akciu s dopadom vyšším ako 100 €, vrátime peniaze.“ Produkt dopad počíta, takže garancia je merateľná a je v súlade s hodnotou „spoľahlivosť“. Rozhodnutie: zakladateľ.
- **Zakladajúci zákazníci (prvých 10):** cena 100 € mesačne natrvalo aj po zavedení pásiem, priama linka na zakladateľa, vplyv na poradie pravidiel a integrácií. Výmenou: mesačný 20-minútový spätnoväzobný hovor a po troch mesiacoch súhlas s referenciou alebo prípadovou štúdiou, ak budú spokojní. Rieši to chýbajúce referencie.
- **Alternatíva:** prvý mesiac zadarmo len pre zakladajúcich zákazníkov výmenou za prípadovú štúdiu. Neodporúčam ako predvolené: neplatiaci pilot neodfiltruje nezáväzných záujemcov a onboarding by sa robil zbytočne.

### 6.5 Landing page (kostra)

1. **Hero:** titulok „Každé ráno viete, čo urobiť, aby váš e-shop zarobil viac.“ Podtitulok: „Pre e-shopy na Shoptete. Shop Pilot v noci pospája Shoptet, Google Ads, Meta Ads a GA4 s nákladmi, spočíta skutočný zisk za každý deň a ráno vám dá 3 najdôležitejšie akcie: prečo, z čoho vyplývajú a koľko vás stojí, keď ich odložíte.“ Primárna výzva „Chcem vidieť ráno s Shop Pilotom (20 min)“, sekundárna „Vypočítať skutočný zisk“. Vizuál: skutočný ranný briefing (screenshot), nie ilustrácia.
2. **Problém:** tri karty (dáta v šiestich záložkách; ROAS nie je zisk; zisk až z účtovníctva).
3. **Ako vyzerá ráno s Shop Pilotom:** tri kroky (prepojíte Shoptet a reklamné účty → v noci prepočítame → ráno tri akcie), s ukážkou jednej akcie: čo, prečo, z čoho, dopad.
4. **Prečo tomu veriť:** deterministický systém, každý návrh ukáže dáta, žiadne halucinácie; read-only prístupy, vlastný tenant na Google Cloud; príbeh zakladateľa a stratovej kampane s vysokým ROAS (približne 1 000 €).
5. **Pre koho:** e-shopy na Shoptete, 150 tis. – 3 mil. €, Google alebo Meta Ads, vlastný sklad. Pod tým: „Nie ste na Shoptete? Nechajte nám e-mail a platformu, dáme vedieť, keď pribudne.“
6. **Cena:** „100 € mesačne, bez viazanosti. Jedna zle nastavená kampaň ma stála približne 1 000 €.“ Pre CZ verziu aj v Kč. Garancia, ak bude schválená.
7. **FAQ:** námietky z kapitoly 7.
8. **Záverečná výzva** na ukážku.

### 6.6 E-mailová sekvencia po kalkulačke (5 správ, 10 dní)

| Deň | Obsah | Výzva |
|---|---|---|
| 0 | Výsledok kalkulačky a čo znamená; jedno pravidlo | pozrieť 3-min video |
| 2 | ROAS ilúzia: príbeh stratovej kampane s vysokým ROAS a výpočet | odpovedať: „aký máte ROAS a maržu?“ |
| 4 | Príbeh zakladateľa a ako vyzerá ráno s Shop Pilotom | video |
| 7 | Pravidlo o sklade a cena nekonania | checklist |
| 10 | Pozvánka na ukážku rána s Shop Pilotom (20 minút, nič nepripravujete) | rezervovať |

---

## 7. Námietky a odpovede

| Námietka | Odpoveď | Dôkaz |
|---|---|---|
| „Mám štatistiky v Shoptete a GA4.“ | Ukazujú, čo sa stalo. Nepoznajú vaše náklady, sklad ani zisk a nepovedia, čo urobiť dnes. | ukážka jednej akcie |
| „Mám agentúru na reklamu.“ | Agentúra optimalizuje ROAS. Vy potrebujete zisk a sklad. Shop Pilot je váš kontrolný nástroj a agentúre dáva jasné priority (čo je vypredané, čo má zápornú maržu). | príbeh stratovej kampane s vysokým ROAS |
| „Nemám čas na ďalší nástroj.“ | 5 minút ráno. Nič nevypĺňate, dáta sa zbierajú samy v noci. Čas nahrádza, nepridáva. | 3-min video |
| „Nechcem dávať prístup k dátam.“ | V ukážke nič nezdieľate. V pilote read-only prístupy, ktoré kedykoľvek zrušíte. Vaše dáta bežia vo vlastnom oddelenom prostredí (tenant) na Google Cloud; nikto iný ich nevidí, ani iní zákazníci. | stránka o bezpečnosti |
| „AI si vymýšľa.“ | Nie je to AI. Deterministické pravidlá; každé odporúčanie ukáže výpočet a dáta, z ktorých vzniklo. | „ukážte výpočet“ v ukážke |
| „Koľko to stojí?“ | 100 € mesačne, bez viazanosti. Jedna zle nastavená kampaň s vysokým ROAS ma stála približne 1 000 €. | vlastný príbeh, garancia |
| „Ste noví, nemáte referencie.“ | Prvá referencia je môj e-shop a číslo, ktoré si viete overiť v ukážke. Prvých desať zákazníkov má cenu natrvalo a priamu linku na mňa; ak za mesiac nenájdeme akciu za viac ako 100 €, vrátim peniaze. | program zakladajúcich zákazníkov |
| „Som na to malý.“ | Postavil som to pre e-shop so 150 tis. € obratu. | príbeh zakladateľa |
| „Nie som na Shoptete.“ | Zatiaľ podporujeme Shoptet. Nechajte mi platformu a e-mail; poradie ďalších integrácií určuje dopyt. | čakacia listina |
| „Prečo nie Triple Whale alebo Lifetimely?“ (segment C) | Sú pre Shopify a americké DTC značky s performance tímom, v angličtine a USD, bez Shoptetu, a nepovedia, čo urobiť dnes. | porovnávacia tabuľka (3.3) |

---

## 8. Kanály a taktiky na 90 dní

### 8.1 Predkvalifikovaný outbound (hlavný kanál pre segment B)

- **Zdroj:** zoznam e-shopov z Heureky (existuje na Drive), obohatiť o: **platforma = Shoptet** (zistiteľná zo zdrojového kódu stránky, napr. odkazy na doménu myshoptet.com), kategória, počet recenzií (odhad veľkosti), aktívna reklama (Meta Ad Library, Google Ads Transparency Center), odhad tržieb (Finstat pre SK, obdobné registre pre CZ), kontakt na majiteľa (obchodný register, LinkedIn).
- **Kvalifikácia:** len Shoptet e-shopy s aktívnou reklamou a vlastným skladom, odhad tržieb 300 tis. – 3 mil. €.
- **Personalizácia:** jedna konkrétna vec z ich verejných dát. Najlepší otvárač: bežiaca kampaň na produkt, ktorý je na webe označený ako vypredaný, lebo je to priamo naše pravidlo a dá sa overiť za minútu. Druhý: „váš e-shop beží na Shoptete, Shop Pilot je preň stavaný“.
- **Sekvencia:** e-mail 1 (hook) → po 3 dňoch e-mail 2 (iné pravidlo alebo príbeh stratovej kampane) → po 4 dňoch LinkedIn alebo telefón → e-mail 3 (rozlúčka s checklistom).
- **Jazyk:** slovenským e-shopom po slovensky, českým po česky (Shoptet má väčšinu základne v Česku, takže česká verzia textov je potrebná od prvého mesiaca).
- **Kapacita:** 30 až 50 personalizovaných kontaktov týždenne pre jedného človeka.

### 8.2 Obsah z pravidiel (komunity a LinkedIn)

- **Skupiny používateľov Shoptetu a skupiny e-shopárov na Facebooku (SK aj CZ):** 2 príspevky týždenne vo formáte „situácia → čísla → čo urobiť“, bez odkazu v texte (pravidlá skupín), odkaz v komentári alebo v správe. Prvý príspevok: stratová kampaň s vysokým ROAS.
- **LinkedIn zakladateľa:** 2 až 3 príspevky týždenne, prvá osoba, čísla z Kifra.sk.
- **Video:** 3-minútové „ráno s Shop Pilotom“ (zostrih ukážky) + 60-sekundové verzie pravidiel (Reels, YouTube Shorts, LinkedIn).
- **Blog a SEO (od 2. mesiaca):** „break-even ROAS“, „ako vypočítať zisk e-shopu“, „POAS vs. ROAS“, „kedy objednať tovar: výpočet“, „zisk e-shopu na Shoptete“; výzva vždy kalkulačka.

### 8.3 Partneri

| Typ partnera | Príklady | Čo z toho má partner | Ako začať |
|---|---|---|---|
| **Platforma (prioritný partner)** | Shoptet: doplnky, partnerský program, blog, podujatia | doplnok, ktorý používateľom dáva zisk a denné priority, teda dôvod zostať na platforme | overiť podmienky zaradenia medzi doplnky a partnerský program; pripraviť popis doplnku v jazyku ranného briefingu |
| Účtovníctvo a finančné riadenie | Roivis, Kros | jeho klienti dostanú denný pohľad, on ostáva autoritou na mesačnú uzávierku; možná integrácia faktúr | spoločný webinár „Zisk denne vs. mesačne“, odporúčací program |
| Konzultanti a CRO | Blueweb, ui42 | nástroj, ktorým podložia odporúčania klientom na Shoptete | pilot pre 2 až 3 ich klientov |
| PPC agentúry a freelanceri | Dexfinity, menšie agentúry | priority od klienta, menej hádok o ROAS; riziko: vnímajú nás ako kontrolu, preto komunikovať ako spojenca | partnerská cena, spoločná prípadová štúdia |
| Médiá a asociácie | E-commerce Bridge, E-commerce Slovakia, podcasty | obsah na tému „zisk namiesto ROAS“ | článok, rozhovor |

### 8.4 Podujatia

- **Upterdam 2026:** cieľ = X rozhovorov s e-shopármi a Y partnerských stretnutí (plán stretnutí už existuje). Otvárač: „Viete, koľko ste zarobili včera? Nie tržby.“ Kvalifikačná otázka: „Na čom beží váš e-shop?“ QR kód na kalkulačku alebo rovno na rezerváciu ukážky. Follow-up do 48 hodín s jedným pravidlom relevantným pre daný e-shop.
- **Reshoper (CZ), podujatia a stretnutia používateľov Shoptetu, lokálne stretnutia e-shopárov.**

### 8.5 Platená reklama

Až po organickom overení hookov (mesiac 3 a neskôr): Meta retargeting na návštevníkov kalkulačky; Google Search na „break-even ROAS“, „zisk e-shopu“, „kalkulačka marže e-shop“, „Shoptet zisk“. Kreatíva = najlepšie fungujúce príspevky z pravidiel.

---

## 9. Meranie

### 9.1 KPI lievika (orientačné hodnoty, overiť prvými dátami)

| Krok | Metrika | Orientačný cieľ |
|---|---|---|
| Outbound | odpovede / odoslané | 8 – 15 % pri personalizácii |
| Outbound | ukážky / odoslané | 2 – 5 % |
| Landing page | kontakt (kalkulačka) / návštevník | 3 – 8 % |
| Landing page | čakacia listina mimo Shoptetu / návštevník mimo Shoptetu | sledovať, určuje ďalšiu integráciu |
| E-mailová sekvencia | ukážka / kontakt | 10 – 20 % |
| Ukážka | pilot / ukážka | 30 – 50 % (platený pilot znižuje pomer, ale zvyšuje kvalitu) |
| Pilot | pokračuje po 1. mesiaci / pilot | 60 % a viac |
| Obsah | žiadosti o ukážku za mesiac | 3 – 5 (mesiace 1 a 2), 10+ (mesiac 3) |

### 9.2 Experimenty

- **Test hookov:** 5 hookov × 2 kanály, 2 týždne; metrika odpovede a kliky. Víťaz ide do hero titulku a reklamy.
- **Test výzvy k akcii:** „ukážka rána s Shop Pilotom“ vs. „ukážka na reálnych číslach“ vs. „prezentácia“.
- **Test segmentu:** A vs. B v outbounde: kde je vyššia konverzia na pilot a nižšie odpadávanie.
- **Test ponuky pilotu:** s garanciou vs. bez garancie; sledovať konverziu ukážka → pilot a počet vrátení.

---

## 10. Plán na 90 dní

| Týždne | Čo | Výstup |
|---|---|---|
| 1 – 2 | Schváliť pozičnú vetu, hooky a ponuku pilotu; pripraviť demo dataset z Kifra.sk a scenár ukážky; landing page v1 (SK, potom CZ); kalkulačka; 3-min video zo záznamu ukážky; 10 pravidiel prepísaných do príspevkov (prvý: stratová kampaň s vysokým ROAS); 200 predkvalifikovaných Shoptet e-shopov | web + magnet + ukážka + obsah na mesiac + zoznam |
| 3 – 4 | Outbound 1. vlna (100); 4 príspevky v skupinách, 6 na LinkedIn; Upterdam (rozhovory + partneri, Shoptet); prvých 5 ukážok; prví 2 zakladajúci zákazníci v pilote | prvé ukážky, prvé piloty, partnerské rozhovory |
| 5 – 8 | Vyhodnotiť hooky, upraviť hero; outbound 2. vlna (150, z toho polovica CZ); 2 partnerské piloty; e-mailová sekvencia; 5 pilotov na produkte; zmerať čas onboardingu a začať ho skracovať | overený hook, piloty, dáta o onboardingu |
| 9 – 12 | Prvá prípadová štúdia (Kifra.sk + prvý zakladajúci zákazník); webinár s partnerom „ROAS nestačí“; SEO články; žiadosť o zaradenie medzi doplnky Shoptetu; test platenej reklamy | cieľ: 10 ukážok mesačne, 5 pilotov mesačne, 10 zakladajúcich zákazníkov |

---

## 11. Otvorené otázky (potrebné od zakladateľa)

Vyriešené v v1.1: cena (100 €), integrácie (Shoptet), trhy (SK a CZ), referencie (Kifra.sk, približne 1 000 €), spôsob ukážky (dáta Kifra.sk), hosting (Google Cloud, vlastný tenant).

1. **Garancia pilotu:** schváliť alebo zamietnuť „ak za prvý mesiac nenájdeme akciu za viac ako 100 €, vrátime peniaze“ (6.4).
2. **Program zakladajúcich zákazníkov:** schváliť podmienky (cena natrvalo, spätná väzba, referencia po 3 mesiacoch).
3. **Bezpečnosť (hosting vyriešený: Google Cloud, vlastný tenant):** doplniť región (EÚ?), aké prístupy presne pilot vyžaduje (Shoptet API, Google Ads, Meta, GA4) a či sú read-only; pripraviť krátky návod na udelenie prístupov a stránku o bezpečnosti.
4. **Onboarding:** koľko hodín dnes trvá a čo z toho sa dá automatizovať ako prvé; od toho závisí, kedy sa dá spustiť bezplatná analýza na dátach záujemcu (5.3, bod 5).
5. **Cena v Kč** pre český web a e-maily.
6. **Kapacita:** hodiny týždenne na obsah, outbound, ukážky a onboarding; koľko pilotov mesačne je zvládnuteľných.
7. **Zoznam pravidiel expertného systému:** základ motora obsahu (kap. 5.4). Stačí názov pravidla, čo sleduje a ako počíta dopad.
8. **Detail príbehu stratovej kampane** pre obsah: kanál (Google alebo Meta), ROAS, skutočná marža, ako dlho bežala, čo sa zmenilo po oprave. Čím konkrétnejšie, tým dôveryhodnejšie.

---

## Zmeny

- **v1.1 (18. 9. 2026):** zapracované odpovede zakladateľa: cena 100 € (jedno pásmo), integrácia len Shoptet, trhy SK a CZ, referencia Kifra.sk (stratová kampaň s vysokým ROAS, úspora približne 1 000 €), ukážka na dátach Kifra.sk namiesto analýzy na dátach záujemcu, hosting Google Cloud s vlastným tenantom pre každého zákazníka. Pridaný scenár ukážky (6.3), ponuka pilotu a program zakladajúcich zákazníkov (6.4), čakacia listina pre platformy, česká verzia textov v pláne.
- **v1 (18. 9. 2026):** prvý návrh.
