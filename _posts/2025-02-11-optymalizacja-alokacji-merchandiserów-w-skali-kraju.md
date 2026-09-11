---
layout: post
title:  "Optymalizacja alokacji merchandiserów w skali kraju"
date:   2025-02-11 10:15:00 +0100
categories: kariera
tags: kariera cv optymalizacja milp
author: Maciej Michałek
---
Klient — oddział globalnego koncernu spożywczego na Filipinach — utrzymuje w terenie zespół merchandiserów odwiedzających punkty sprzedaży detalicznej, żeby kontrolować stany i uzupełniać półki. Roczny koszt tego zespołu sięgał miliarda pesos i rósł wraz z otwieraniem kolejnych punktów, a w tle pojawiała się zapowiedziana podwyżka płacy minimalnej. Przydział merchandiserów do sklepów odbywał się bez ustalonego procesu, w oparciu o doświadczenie lokalnych kierowników.

Problem wygląda na klasyczny routing, ale nim nie jest. Trzeba jednocześnie rozstrzygnąć, jak często i jak długo należy odwiedzać każdy punkt, kto ma go odwiedzić, oraz w jakiej kolejności — przy ograniczeniach, które nie wynikają z geografii. Częstotliwość zależy od wolumenu sprzedaży, czas wizyty od liczby wariantów produktowych, a część ograniczeń ma charakter czysto handlowy: istnieją grupy klientów, których nie wolno obsługiwać w ramach jednej trasy. Do tego regiony sprzedażowe zdefiniowane przez klienta nie pokrywają się z granicami administracyjnymi, więc nie dało się skorzystać z gotowych podziałów.

Rozwiązanie zbudowaliśmy jako trzy sekwencyjne modele optymalizacyjne: przypisanie harmonogramów wizyt do sklepów, optymalizacja tras dziennych i wreszcie optymalizacja harmonogramu tygodniowego. Takie rozbicie było decyzją świadomą — pozwoliło uzyskać rozwiązania wysokiej jakości przy radykalnie mniejszym nakładzie obliczeniowym niż próba sformułowania całości jako jednego zadania. Macierze odległości i czasów przejazdu zbudowaliśmy na rzeczywistej sieci drogowej z OpenStreetMap, wyznaczając najkrótsze ścieżki między wszystkimi parami lokalizacji; do obszarów analizy dodaliśmy bufor, żeby nie obcinać dróg i nie tracić połączeń na granicach regionów. Model uwzględnia ośmiogodzinny dzień pracy, rozróżnia merchandiserów stacjonarnych od objazdowych i rozprowadza niewykorzystany czas trasy pomiędzy odwiedzane sklepy.

Technologie: Azure, Databricks, Python, SQL, FICO Xpress, OR-Tools, OpenStreetMap (osmnx), Snowflake, Power BI.

Rezultaty: redukcja zapotrzebowania na etaty od 20% do 44% w zależności od charakterystyki regionu, przy szacowanej redukcji łącznej na poziomie 30%. Równolegle model wskazał nowe możliwości rozszerzenia pokrycia — punkty, które dotychczas nie były obsługiwane, a mieszczą się w istniejących trasach.

Optymalizacja na tę skalę rzadko wygrywa lepszym solverem. Wygrywa dobrym rozcięciem problemu i prawidłową macierzą odległości — bo trasa licząca odległość w linii prostej wygląda świetnie w raporcie i przestaje się bronić w pierwszym tygodniu pracy w terenie.
