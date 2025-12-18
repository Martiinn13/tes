# Porovnání systémů pro analýzu sportovního výkonu: Profesionální GPS vesty vs. Apple Watch

## 1. Cíl projektu
Cílem tohoto projektu je technická analýza a praktické porovnání dvou metod měření fyzické zátěže u sportovců (konkrétně fotbalistů). Projekt se zaměřuje na:
* **Teoretický rozbor:** Studium mikrokontrolérů, senzorů (akcelerometry, gyroskopy) a GNSS systémů používaných v nositelné elektronice.
* **Praktické porovnání:** Konfrontace dat naměřených profesionální "GPS vestou" a chytrými hodinkami Apple Watch (aplikace Kondice).
* **Analýza přesnosti:** Vyhodnocení rozdílů v metodice měření a interpretaci dat.

## 2. Teoretická část: Mikroprocesorové řídicí systémy a senzory

V obou typech zařízení (vesta i hodinky) se nachází sofistikované vestavné (embedded) systémy. 

### 2.1 Mikrokontroléry (MCU) a SoC
Základem obou zařízení je řídicí jednotka, která musí splňovat přísná kritéria na energetickou efektivitu a výkon.
* **Apple Watch:** Používají vysoce integrovaný systém na čipu (SoC) řady Apple S-series. Obsahuje vícejádrový procesor (architektura ARM), GPU a specializovaný Neural Engine pro zpracování dat ze senzorů pomocí strojového učení.
* **Fotbalové vesty (např. Catapult, STATSports):** Často využívají nízkoenergetické mikrokontroléry (např. ARM Cortex-M4 nebo M7). Jejich hlavní úlohou není obsluha grafického displeje, ale extrémně rychlé vzorkování dat ze senzorů a jejich ukládání na vnitřní paměť.

### 2.2 Senzorová výbava (IMU jednotky)
Klíčem k měření pohybu je **IMU (Inertial Measurement Unit)**, která se skládá z:
1.  **Akcelerometr (tříosý):** Měří zrychlení. U fotbalových vest se používají senzory s vysokým rozsahem (až 16g nebo více), aby zachytily prudké starty a nárazy.
2.  **Gyroskop:** Měří úhlovou rychlost a pomáhá určit orientaci těla v prostoru.
3.  **Magnetometr:** Funguje jako digitální kompas pro určení směru pohybu.

### 2.3 Metodika měření (GNSS vs. RTK)
* **Vzorkovací frekvence:** Toto je hlavní rozdíl. Zatímco běžné hodinky vzorkují GPS polohu většinou 1x za sekundu (1 Hz), profesionální vesty pracují na frekvenci **10 Hz až 18 Hz**. To znamená, že vesta zaznamená 18 polohových bodů za jedinou sekundu, což je klíčové pro měření krátkých sprintů a změn směru, které hodinky často "vyhladí".
* **Lokalizace:** Vesty využívají pokročilé GNSS čipy, které kombinují systémy GPS, GLONASS, Galileo a Beidou.

## 3. Rozbor komponentů: "Podprsenka" vs. Hodinky

| Parametr | Profesionální GPS vesta | Apple Watch (Kondice) |
| :--- | :--- | :--- |
| **Umístění** | Mezi lopatkami (těžiště těla) | Zápěstí (periferie) |
| **Přesnost GPS** | Vysoká (10-18 Hz vzorkování) | Střední (standardně 1 Hz) |
| **Měření tepu** | Hrudní pás nebo optický senzor | Optický senzor (PPG) na zápěstí |
| **Hlavní metrika** | High Intensity Running, Player Load | Aktivní kalorie, tréninkový čas |
| **Datový výstup** | Surová data pro analytiky | Uživatelsky přívětivé grafy |

### Proč nosí fotbalisté "podprsenky"?
Umístění senzoru mezi lopatkami je klíčové. Je to bod nejblíže těžišti těla. Senzor na zápěstí (hodinky) je ovlivněn pohyby rukou, které neodpovídají pohybu celého těla (např. při signalizaci nebo v soubojích), což vnáší do měření šum.

## 4. Dokumentace současného stavu
* **Hardware:** Apple Watch Series [DOPLNIT MODEL], Profesionální tracker [DOPLNIT NÁZEV/ZNAČKU].
* **Software:** Aplikace Apple Kondice, analytický software k vestě.
* **Stav:** Aktuálně probíhá sběr dat z testovacích tréninkových jednotek.

## 5. Praktická část (V přípravě)
*Zde budou vloženy výsledky porovnání obou zařízení z konkrétních měření.*
1. Srovnání celkové uběhnuté vzdálenosti.
2. Srovnání maximální naměřené rychlosti.
