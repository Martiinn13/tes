# Porovnání mikroprocesorových systémů ve sportu: Apple Watch vs. STATSports Apex

## 1. Cíl projektu
Tento ročníkový projekt se zaměřuje na technickou analýzu a praktické srovnání dvou metod měření sportovního výkonu. Cílem je prozkoumat rozdíly mezi komerčními chytrými hodinkami a profesionálním trackovacím systémem používaným v elitním fotbale, a to z pohledu hardwaru, senzoriky a zpracování dat mikrokontroléry.

## 2. Teoretická část: Mikroprocesorové řízení a senzorika

### 2.1 Architektura řídicích jednotek (MCU)
Srdcem obou zařízení jsou vestavné (embedded) systémy, které se však liší svou architekturou:

* **Apple Watch (Consumer Grade):** Využívají vysoce integrovaný **System in Package (SiP)**. Obsahuje vícejádrový procesor (architektura ARM), který musí kromě senzorů obsluhovat i grafický displej, bezdrátovou komunikaci (LTE, Wi-Fi, BT) a komplexní operační systém watchOS. Data ze senzorů jsou zde filtrována koprocesorem pro strojové učení, aby se eliminovaly nežádoucí pohyby ruky.
* **STATSports Apex (Professional Grade):** Jedná se o dedikovanou měřicí jednotku. Mikrokontrolér je zde optimalizován pro **vysokorychlostní sběr dat (Data Logging)**. Na rozdíl od hodinek není zatížen grafickým rozhraním, což umožňuje veškerý výpočetní výkon soustředit na vzorkování senzorů.

### 2.2 Senzorová analýza (IMU a GNSS)
Klíčovým prvkem je **Inerciální měřicí jednotka (IMU)**, která se skládá z:
1.  **Akcelerometr:** Měří lineární zrychlení. U fotbalové vesty jsou použity senzory s vysokým dynamickým rozsahem pro zachycení prudkých nárazů a startů.
2.  **Gyroskop:** Sleduje rotaci těla. Pomáhá odlišit běh od jiných typů pohybu.
3.  **Magnetometr:** Slouží jako digitální kompas pro určení orientace na hřišti.

**Hlavní technický rozdíl: Vzorkovací frekvence**
* **Apple Watch:** Standardní GPS vzorkování probíhá na frekvenci **1 Hz** (1 záznam polohy za sekundu).
* **STATSports Apex:** Profesionální jednotka pracuje na frekvenci **10 Hz až 18 Hz**. 
* *Důsledek:* Při sprintu trvajícím 3 sekundy zaznamenají hodinky pouze 3 body, zatímco vesta až 54 bodů. To umožňuje mnohem přesnější výpočet maximální rychlosti a zrychlení.

---

## 3. Praktická část: Analýza naměřených dat

V rámci testování byla provedena tréninková jednotka, kde byla data zaznamenávána současně oběma systémy.

### 3.1 Přehled výsledků

| Metrika | Apple Watch (Kondice) | STATSports Apex (Vesta) |
| :--- | :--- | :--- |
| **Vzdálenost** | 8,54 km | 8,36 km |
| **Doba trvání** | 41:02 min | 1:40:00 (celkový čas session) |
| **Max. rychlost** | - | 7,86 m/s (28,3 km/h) |
| **Průměrný tep** | 172 BPM | - |
| **Energetický výdej** | 497 kcal (aktivní) | 856 kcal (celkové) |

### 3.2 Porovnání přesnosti měření polohy
Podle mapových podkladů z Apple Watch (lokalita Solnice) je patrné, že hodinky trasu mírně vyhlazují.
* **Vzdálenost 8,54 km (Apple) vs 8,36 km (Vesta):** Rozdíl 180 metrů je způsoben odlišným algoritmem výpočtu. Apple Watch díky 1 Hz vzorkování "řežou zatáčky", což paradoxně může u delších běhů vzdálenost mírně nadhodnotit nebo podhodnotit v závislosti na členitosti trasy.
* **Umístění:** Vesta má anténu mezi lopatkami (přímý výhled na satelity), zatímco hodinky na zápěstí jsou často stíněny pohybem těla.

### 3.3 Intenzita a tepová frekvence
Apple Watch zaznamenaly průměrný tep **172 BPM**, přičemž většinu času (přes 30 minut) se sportovec nacházel v **Zóně 4 (166–180 BPM)**. 
* Tato data potvrzují vysokou intenzitu tréninku, což koresponduje s daty z vesty, která naměřila **352 metrů v HSR (High Speed Running)**.
* Maximální rychlost **7,86 m/s** (naměřená vestou) je špičková hodnota, kterou standardní aplikace Apple Kondice běžně neuvádí v takovém detailu.

---

## 4. Fotodokumentace a grafy

### Apple Watch - Aplikace Kondice
Snímky ukazují detailní rozbor tepu a mapu trasy v okolí Solnice.
![Apple Watch Summary](images/apple_1.png)
![Apple Watch Heart Rate](images/apple_3.png)
![Route Map](images/apple_2.png)

### STATSports Apex - Profesionální analýza
Snímky ukazují srovnání s profesionálními fotbalisty a analýzu rychlostních limitů.
![STATSports Summary](images/stats_1.png)
![Max Speed Analysis](images/stats_2.png)

---

## 5. Závěr
Z technického hlediska je profesionální vesta **STATSports Apex** přesnějším nástrojem pro analýzu krátkých, vysoce intenzivních pohybů typických pro fotbal, a to díky vyšší vzorkovací frekvenci mikrokontroléru. **Apple Watch** jsou naopak vynikající v monitorování fyziologických funkcí (tepová frekvence) a poskytují lepší uživatelské rozhraní pro dlouhodobé sledování kondice. Pro účely profesionálního tréninku je však klíčová fixace senzoru v těžišti těla (vesta), která eliminuje šum způsobený pohybem končetin.

---

## 6. Citace a poděkování
* Snímaná data: Vlastní měření (Apple Watch Series, STATSports Apex)
* Teorie mikrokontrolérů: Dokumentace architektur ARM Cortex-M
* Software: Apple Fitness+, STATSports Apex App

