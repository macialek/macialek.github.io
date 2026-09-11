---
layout: post
title:  "Platforma prognozowania popytu dla globalnego koncernu FMCG"
date:   2024-12-05 09:15:00 +0100
categories: kariera
tags: kariera cv machine-learning
author: Maciej Michałek
---
Klient prognozował popyt w dużej mierze ręcznie. Proces był czasochłonny, kosztowny w utrzymaniu i nie skalował się na kolejne rynki, a problemy z optymalizacją zapasów wracały co kwartał.

Sedno problemu leżało w powtarzalności pracy: każdy nowy rynek oznaczał przejście pełnego cyklu od analizy danych, przez inżynierię cech i eksperymenty, po refaktoryzację kodu badawczego do postaci produkcyjnej. Klasyczne podejście projektowe nie miało szans nadążyć za tempem ekspansji.

Zamiast kolejnego modelu zbudowaliśmy platformę. Wspólny model danych konsoliduje sprzedaż, zapasy, promocje i uzupełnienia z wielu źródeł w jedną strukturę, z tabelami rozszerzeń przeznaczonymi na specyfikę rynkową. Nad nim stoi rdzeń definiujący wewnętrzne API, biblioteka komponentów wielokrotnego użytku oraz moduł bazowy z domyślną implementacją zadań: trening, predykcja, ewaluacja, postprocessing i publikacja. Uruchomienie nowego rynku sprowadza się do konfiguracji i ewentualnych własnych fragmentów kodu, a nie do nowego projektu. Oczekiwania wobec danych są definiowane deklaratywnie i weryfikowane testami jakości z użyciem biblioteki Great Expectations. Dodatkowym elementem jest moduł sugestii zamówień, łączący prognozę, stany magazynowe i zamówienia otwarte.

Rezultaty: czas onboardingu nowego rynku skrócony do dwóch tygodni, osiem krajów i około czterdziestu rynków korzystających z prognoz generowanych przez platformę, istotny wzrost liczby zamówień składanych z wyprzedzeniem.

Technologie: Azure Databricks, Python, PySpark, LightGBM.

Najważniejszą decyzją projektową w takiej platformie jest przebieg granicy między rdzeniem a customizacją. Przesunięta w jedną stronę powoduje, że rdzeń puchnie od wyjątków. Przesunięta w drugą sprawia, że każdy rynek pisze wszystko od nowa.
