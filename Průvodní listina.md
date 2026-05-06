Úvod do projektu:

Na vašem analytickém oddělení nezávislé společnosti, která se zabývá životní úrovní občanů, jste se dohodli, že se pokusíte odpovědět na pár definovaných výzkumných otázek, které adresují dostupnost základních potravin široké veřejnosti. Kolegové již vydefinovali základní otázky, na které se pokusí odpovědět a poskytnout tuto informaci tiskovému oddělení. Toto oddělení bude výsledky prezentovat na následující konferenci zaměřené na tuto oblast.
Potřebují k tomu od vás připravit robustní datové podklady, ve kterých bude možné vidět porovnání dostupnosti potravin na základě průměrných příjmů za určité časové období.
Jako dodatečný materiál připravte i tabulku s HDP, GINI koeficientem a populací dalších evropských států ve stejném období, jako primární přehled pro ČR.

Primární tabulky:
czechia_payroll – Informace o mzdách v různých odvětvích za několikaleté období. Datová sada pochází z Portálu otevřených dat ČR.
czechia_payroll_calculation – Číselník kalkulací v tabulce mezd.
czechia_payroll_industry_branch – Číselník odvětví v tabulce mezd.
czechia_payroll_unit – Číselník jednotek hodnot v tabulce mezd.
czechia_payroll_value_type – Číselník typů hodnot v tabulce mezd.
czechia_price – Informace o cenách vybraných potravin za několikaleté období. Datová sada pochází z Portálu otevřených dat ČR.
czechia_price_category – Číselník kategorií potravin, které se vyskytují v našem přehledu.

Číselníky sdílených informací o ČR:
czechia_region – Číselník krajů České republiky dle normy CZ-NUTS 2.
czechia_district – Číselník okresů České republiky dle normy LAU.

Dodatečné tabulky:
countries - Všemožné informace o zemích na světě, například hlavní město, měna, národní jídlo nebo průměrná výška populace.
economies – HDP, GINI, daňová zátěž atd. pro daný stát a rok.

Výstup projektu
Pomozte kolegům s daným úkolem. Výstupem by měly být dvě tabulky v databázi, ze kterých se požadovaná data dají získat. Tabulky pojmenujte t_{jmeno}{prijmeni}project_SQL_primary_final (pro data mezd a cen potravin za Českou republiku sjednocených na totožné porovnatelné období – společné roky) a t{jmeno}{prijmeni}_project_SQL_secondary_final (pro dodatečná data o dalších evropských státech). Dále připravte sadu SQL, které z vámi připravených tabulek získají datový podklad k odpovězení na vytyčené výzkumné otázky. Pozor, otázky/hypotézy mohou vaše výstupy podporovat i vyvracet! Záleží na tom, co říkají data.

Výzkumné otázky:
1) Rostou v průběhu let mzdy ve všech odvětvích, nebo v některých klesají?
2) Kolik je možné si koupit litrů mléka a kilogramů chleba za první a poslední srovnatelné období v dostupných datech cen a mezd?
3) Která kategorie potravin zdražuje nejpomaleji (je u ní nejnižší percentuální meziroční nárůst)? 
4) Existuje rok, ve kterém byl meziroční nárůst cen potravin výrazně vyšší než růst mezd (větší než 10 %)?
5) Má výška HDP vliv na změny ve mzdách a cenách potravin? Neboli, pokud HDP vzroste výrazněji v jednom roce, projeví se to na cenách potravin či mzdách ve stejném nebo následujícím roce výraznějším růstem?

Odpovědi:

1) Rostou v průběhu let mzdy ve všech odvětvích, nebo v některých klesají?

Mzdy nerostou ve všech odvětvích lineárně; v historii existují případy, kdy průměrná mzda v konkrétních odvětvích meziročně klesla.
Níže jsou klíčová zjištění z dat:
Nejčastější poklesy: Odvětví Těžba a dobývání zaznamenalo v sledovaném období hned 4 meziroční poklesy (roky 2009, 2013, 2014 a 2016).

Kritické roky:
Rok 2013 byl pro mzdy v ČR velmi nepříznivý – k poklesu došlo v naprosté většině sledovaných odvětví (např. Informační a komunikační činnosti, Peněžnictví, Stavebnictví).
Rok 2021 ukázal poklesy v odvětvích jako Vzdělávání, Kulturní a zábavní činnosti nebo Zemědělství.

Příklady výrazných poklesů:
V roce 2013 v odvětví Peněžnictví a pojišťovnictví klesla průměrná mzda o 4 484 Kč oproti předchozímu roku.
V roce 2020 v odvětví Činnosti v oblasti nemovitostí klesla mzda o 2 150 Kč.

Závěr: 
Ačkoliv je dlouhodobý trend mezd rostoucí, existují specifické roky a odvětví, kde dochází k propadům. Odpověď pro tvůj projekt tedy zní: V některých odvětvích mzdy v určitých letech klesají.

2) Na základě analýzy databází mezd a cen potravin jsem zjistila, že prvním rokem, pro který máme k dispozici obě datové sady (srovnatelné období), je rok 2006, a posledním dostupným rokem je rok 2018.

Z výsledků vyplývá následující porovnání kupní síly:
Chléb (konzumní kmínový)
V roce 2006 si občan s průměrnou hrubou mzdou (21 084 Kč) mohl při průměrné ceně 16,12 Kč/kg koupit celkem 1 308 kg chleba.
V roce 2018 průměrná mzda vzrostla na 33 039 Kč a cena chleba na 24,24 Kč/kg. Za průměrnou mzdu tak bylo možné pořídit 1 363 kg chleba.

Množství chleba, které si lze koupit za průměrnou mzdu, se zvýšilo o 55 kg.

Mléko (polotučné pasterované)
V roce 2006 si bylo možné z průměrné mzdy (21 084 Kč) při ceně 14,44 Kč/l koupit 1 460 litrů mléka.
V roce 2018 při průměrné mzdě (33 039 Kč) a ceně 19,82 Kč/l se toto množství zvýšilo na 1 667 litrů mléka.

Množství mléka, které si lze koupit za průměrnou mzdu, se zvýšilo o 207 litrů.

Závěr:
Ačkoliv v absolutních číslech cena obou základních potravin mezi lety 2006 a 2018 vzrostla, průměrné mzdy rostly rychlejším tempem. Díky tomu se reálná dostupnost chleba i mléka pro širokou veřejnost v tomto období prokazatelně zvýšila.

3) Která kategorie potravin zdražuje nejpomaleji (je u ní nejnižší percentuální meziroční nárůst)? 
