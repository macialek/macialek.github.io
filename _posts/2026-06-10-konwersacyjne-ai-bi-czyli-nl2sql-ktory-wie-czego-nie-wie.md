---
layout: post
title:  "Konwersacyjne AI/BI, czyli NL2SQL, który wie czego nie wie"
date:   2026-06-10 09:00:00 +0200
categories: kariera
tags: kariera cv genai nl2sql
author: Maciej Michałek
---
Klient, globalny koncern z branży napojów, chciał umożliwić menedżerom w kilkudziesięciu rynkach zadawanie pytań o sprzedaż własnymi słowami i otrzymywanie wiarygodnej liczby — zamiast czekania dwóch dni na dostępność analityka.

Naturalne pytanie jest z definicji wieloznaczne. „Sprzedaż w zeszłym kwartale” oznacza co innego w finansach, co innego w łańcuchu dostaw, a w każdym rynku może mieć jeszcze odrębną definicję lokalną. Model językowy chętnie wygeneruje SQL dla każdego z tych pytań, w tym dla tego źle zrozumianego, i zrobi to z jednakową pewnością siebie.

Punktem ciężkości rozwiązania nie był zatem model, lecz warstwa semantyczna: jedno źródło prawdy dla metryk, joinów, synonimów i wariantów rynkowych. Routing i orkiestracja działają nad nią, a nie zamiast niej. Dołożyliśmy zestaw kontroli: tożsamość użytkownika przenoszona do zapytania, bezpieczeństwo na poziomie wierszy i kolumn, rozróżnienie w odpowiedzi między faktem, wyliczeniem, prognozą i symulacją, a także progi pewności, poniżej których system świadomie odmawia odpowiedzi zamiast zgadywać.

Byłem odpowiedzialny za architekturę rozwiązania oraz za odpowiedzi na pytania architektoniczne stawiane przez architektów klienta — w tym za wyznaczenie granic zastosowania, czyli wskazanie przypadków, w których wzorzec konwersacyjny nie jest właściwym narzędziem i należy sięgnąć po inne.

Odmowa odpowiedzi jest tu funkcją, nie awarią. Każda zwrócona liczba ma pochodzenie, wersję modelu i ślad w logach.

Routing nie zastąpi semantyki. Jeżeli definicje metryk i warianty rynkowe nie są rozstrzygnięte w warstwie semantycznej, orkiestrator jedynie rozprowadzi tę niejednoznaczność po większej liczbie interfejsów.
