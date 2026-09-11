---
layout: post
title:  "AutoPilot — orkiestrator operacji magazynowych"
date:   2025-01-14 09:25:00 +0100
categories: kariera
tags: kariera cv optymalizacja milp
author: Maciej Michałek
---
Projekt realizowany dla koncernu FMCG z listy Fortune 500. Celem było zastąpienie pracy „pilotów magazynu” — ludzi, którzy ręcznie decydowali, co, kiedy i przez kogo ma być zrobione — kompletnym orkiestratorem planującym operacje wyjściowe w horyzoncie najbliższych 24 godzin.

Do projektu trafiłem w nietypowych okolicznościach. Zadanie brzmiało: przejąć kod od specjalisty opuszczającego organizację i przygotować go do wdrożenia oraz skalowania. Już podczas wstępnego przeglądu okazało się, że rozwiązanie nie spełnia zakładanych wymagań funkcjonalnych, a kod nie spełnia wewnętrznych standardów wytwarzania oprogramowania. Wcześniejsza próba wydania produkcyjnego zakończyła się niepowodzeniem. Moja rola i zaangażowanie zostały poszerzone: razem z klientem przygotowaliśmy specyfikację wymagań z oznaczeniem funkcji faktycznie zrealizowanych, a następnie plan naprawczy obejmujący przygotowanie danych i scenariuszy testowych, pokrycie kodu testami, refaktoryzację monolitu na moduły i klasy, oraz uzupełnienie braków funkcjonalnych. Plan został zaakceptowany, a ja pełniłem w trakcie jego realizacji rolę lidera technologicznego po stronie backendu i doradcy Data Science.

Od strony modelowania AutoPilot to trzy połączone solvery pracujące w kaskadzie. Pierwszy minimalizuje dystans między lokalizacją pobrania a grupą pasów kompletacyjnych, przypisując ruchy przewoźników do tych pasów, które mogą je obsłużyć z najmniejszym ryzykiem opóźnienia. Jego wynik jest wejściem dla kolejnego etapu, w którym powstaje plan dla ruchów już zatwierdzonych — przypisania zasobów i czasów — a następnie plan dla ruchów pozostałych, uwzględniający wynik pierwszego solvera. Całość sformułowana jako MILP, rozwiązywana komercyjnym solverem FICO Xpress.

Zakres decyzji podejmowanych przez system jest szeroki. AutoPilot wyznacza czas rozpoczęcia i zakończenia każdego zadania — pobrania, foliowania, transportu i załadunku — dla każdego zamówienia, z uwzględnieniem terminu wykonania. Priorytetyzuje zadania: „live loads” mają wyższą wagę i dodatkowe ograniczenie czasowe. Decyduje o uzupełnieniach zapasów: czy popyt uzasadnia uzupełnienie, kiedy je wykonać i jak długo potrwa. Wybiera lokalizację pobrania i docelowy pas kompletacyjny, minimalizując dystans przejazdu, a przy braku wolnego pasa umieszcza zamówienie w pasie oczekiwania i podaje dokładny moment przeniesienia. Planuje wyłącznie tyle pracy, na ile pozwalają dostępne zasoby, rozróżniając przy tym, które typy maszyn obsługują które zadania. Obsługuje również wyjątki: klientów z dedykowanymi pasami, wymogiem foliowania palet czy dodatkowego etykietowania wydłużającego czas załadunku.

Technologie: Python, FICO Xpress, MILP, Azure, GitHub, CI/CD.

Projekt zakończył się sukcesem — rozwiązanie trafiło na produkcję w pierwszym magazynie, a następnie zostało zaadaptowane do kolejnego, wyposażonego w automatycznie prowadzone wózki wykonujące pobranie. Warto jednak odnotować, jaka była droga do tego wyniku: od nieudanego wydania i realnego ryzyka anulowania, przez uporządkowanie wymagań i refaktoryzację, po decyzję klienta o powierzeniu nam dalszych strumieni produktu.

Nauka z tego projektu jest niewygodna, ale użyteczna: kiedy przejmujesz cudzy kod, najkosztowniejszym błędem jest przyjęcie założenia, że działa tak, jak mówi dokumentacja. Tydzień poświęcony na spisanie, co faktycznie zostało zrealizowane, oszczędził kwartał.
