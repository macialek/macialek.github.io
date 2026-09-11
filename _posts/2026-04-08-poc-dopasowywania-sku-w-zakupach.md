---
layout: post
title:  "PoC dopasowywania SKU w zakupach — od tygodni do godzin"
date:   2026-04-08 09:45:00 +0200
categories: kariera
tags: kariera cv genai embeddings optymalizacja
author: Maciej Michałek
---
Klient, międzynarodowa grupa działająca w obszarze usług gastronomicznych, mierzy się z rosnącą złożonością analizy zakupowej. Katalogi produktowe puchną, a kolejne przejęcia dokładają następne — każde z własnym modelem danych. Menedżerowie kategorii spędzali tygodnie na ręcznym dopasowywaniu i porównywaniu SKU w arkuszach kalkulacyjnych, co opóźniało decyzje o oszczędnościach i wprowadzało niespójność. Dane podstawowe nie były wiarygodne, a między rynkami nie istniał żaden wzorzec złotego rekordu.

Trudność nie polega na tym, że produktów jest dużo. Polega na tym, że ten sam produkt u dwóch dostawców ma inną nazwę, inną jednostkę miary i inną strukturę opisu, a część atrybutów istotnych dla porównania — jak gramatura porcji — w ogóle nie występuje jako pole w danych, tylko siedzi w tekście opisu.

Podejście, które przyjąłem, opiera się na warstwowym dopasowaniu. Najpierw katalog jest dzielony na porównywalne kubełki: częściowo według hierarchii obecnych w danych, częściowo według atrybutów wywnioskowanych przez model z opisu tekstowego. Wołowina to jedna kategoria, ale w jej obrębie liczy się już wielkość opakowania i gramatura — a te trzeba wydobyć z tekstu. Dopiero wewnątrz kubełka działa wyszukiwanie semantyczne oparte na embeddingach, zestawione z porównaniem atrybutów i opatrzone oceną pewności oraz wyjaśnieniem, dlaczego dwa produkty uznano za odpowiedniki. Reguły biznesowe — na przykład zakaz mieszania produktów bio z nie-bio — działają zarówno jako zdefiniowane ograniczenia, jak i jako doprecyzowania wydawane w języku naturalnym. Osobny moduł wydobywa jednostki miary z nazw produktów podejściem hybrydowym, łączącym reguły heurystyczne z modelem językowym tam, gdzie heurystyka zawodzi, i normalizuje ceny do porównywalnej ceny za jednostkę. Na końcu wchodzi solver MILP, który na podstawie uploadowanego planu popytu rekomenduje optymalny miks dostawców z uwzględnieniem minimalnych wielkości zamówienia, czasu dostawy i kosztów transportu.

Prototyp demonstrujący pełny przepływ — od wczytania katalogu, przez wyszukiwanie semantyczne i dopasowanie z wyjaśnieniem, po wykrywanie oszczędności i zoptymalizowany plan zakupowy — zbudowałem w tydzień. To zmieniło trajektorię całej rozmowy z klientem: przestaliśmy dyskutować, czy to zadziała, a zaczęliśmy rozmawiać o tym, jak szybko można to wdrożyć i o ile taniej.

Technologie: Python, embeddingi, wyszukiwanie wektorowe, LLM, MILP (OR-Tools / PuLP), Azure.

Uczestniczyłem w kształtowaniu podejścia technicznego i wycenie prac. Wniosek, który zapamiętałem: działający prototyp jest mocniejszym argumentem handlowym niż najlepiej przygotowana prezentacja, a koszt jego zbudowania dzięki AI Assisted Coding bywa niższy niż koszt jej przygotowania.
