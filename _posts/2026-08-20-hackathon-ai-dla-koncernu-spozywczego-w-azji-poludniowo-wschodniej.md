---
layout: post
title:  "Hackathon AI dla koncernu spożywczego w Azji Południowo-Wschodniej"
date:   2026-08-20 09:00:00 +0200
categories: kariera
tags: kariera cv genai hackathon facylitacja
author: Maciej Michałek
---
Celem projektu było przeprowadzenie firmowego programu otwartej innowacji, którego tegoroczna edycja została w całości poświęcona sztucznej inteligencji. Klient — wiodący koncern spożywczo-napojowy działający w kilku krajach Azji Południowo-Wschodniej — organizuje ten program cyklicznie, ale po raz pierwszy potrzebował partnera technologicznego, który wprowadzi uczestników w temat AI i pomoże im dojść od pomysłu do koncepcji gotowej do wyceny.

Zakres obejmował całość: przygotowanie przed wydarzeniem, dwudniowe warsztaty stacjonarne, dziesięć zdalnych sesji mentoringowych w trakcie dwutygodniowego sprintu prototypowania oraz udział w finałowej prezentacji. Byłem odpowiedzialny za projekt merytoryczny programu, przygotowanie wszystkich materiałów i prowadzenie warsztatów na miejscu, a następnie za mentoring zespołów. Uczestnikami było około pięćdziesięciu osób z ról biznesowych, nie technicznych — z obszarów HR, sprzedaży, łańcucha dostaw, produkcji i rozwoju produktu, z kilku krajów regionu.

## Problem, który trzeba było rozwiązać zanim zaczął się hackathon
Hackathony AI dla osób nietechnicznych mają jedną charakterystyczną przypadłość: kończą się zestawem pomysłów na chatbota. Uczestnik, który zna AI wyłącznie z asystenta w przeglądarce, będzie proponował warianty tego, co zna. Efektem jest dzień dobrej energii i portfel koncepcji, których nikt nie sfinansuje, bo żadna nie została połączona z konkretnym procesem, konkretnym użytkownikiem i konkretną liczbą.

Drugi problem to rozrzut wiedzy. W sali siedzą obok siebie ludzie, dla których GenAI to codzienne narzędzie, i tacy, którzy nie używali go nigdy. Warsztat prowadzony na uśrednionym poziomie zanudzi jednych i zgubi drugich.

## Rozwiązanie

Przed wydarzeniem przygotowałem kwestionariusz oceny wiedzy o AI, GenAI, agentach, RAG, gotowości danych i odpowiedzialnym stosowaniu AI. Wypełniło go czterdzieści osób na pięćdziesiąt cztery, a wyniki posłużyły mi do skalibrowania modułu wprowadzającego — przygotowałem materiał z nadmiarem, żeby mieć co przycinać, zamiast improwizować w trakcie. Ten sam kwestionariusz, w wersji powtórzonej po wydarzeniu, pozwolił zmierzyć faktyczny przyrost wiedzy, a nie tylko zadowolenie uczestników.

Program został zbudowany według jasnej logiki. Dzień pierwszy to inspiracja i nauka: wspólny słownik pojęć, przegląd realnych zastosowań AI w branży FMCG i w operacjach, praktyczny tutorial promptowania, zasady bezpiecznego i zgodnego z regulacjami korzystania z narzędzi oraz — co uważam za najważniejszy moduł całego dnia — sesja o tym, jak przejść od generycznego pomysłu na chatbota do rozwiązania powiązanego z wartością biznesową, zmianą procesu i konkretnym użytkownikiem. Domknąłem to blokiem o adopcji i fazie RUN, bo zespoły z reguły kończą myślenie na dniu wdrożenia.

Dzień drugi to warsztat pracy własnej zespołów: kwestionowanie ambicji pomysłu, ramowanie problemu, mapa beneficjentów, projekt koncepcji rozwiązania, reality check dotyczący danych i wykonalności, przygotowanie makiety lub przykładowego wyniku oraz szkielet pitcha. Mentorzy i wyznaczeni przez klienta AI Champions mieli w tym dniu jedną wyraźną zasadę: nie rozwiązują problemów biznesowych za zespoły i nie podsuwają rozwiązań. Naprawadzają celnymi pytaniami.

Narzędziowo oparliśmy program o wewnętrzne, agentyczne rozwiazanie Lingaro, uruchomione jako dedykowana instancja na naszej infrastrukturze, z osobnymi kluczami dostępowymi dla pięciu zespołów. Przygotowałem dwa szablony pracy: jeden do indywidualnego kształtowania pomysłu przed pracą zespołową, drugi jako główny szablon prowadzący zespół od wybranego kierunku do udokumentowanej koncepcji. Narzędzie nie generuje pomysłów za uczestników — zadaje pytania, które zadałby dobry facylitator: kto dokładnie skorzysta, jakie dowody potwierdzają problem, co musi być prawdą, żeby to zadziałało, jakie dane są potrzebne i jak wyglądałby wiarygodny MVP. Przy okazji zapisuje tok myślenia zespołu i zamienia go w ustrukturyzowaną, porównywalną dokumentację.

Osobnym zadaniem było uporządkowanie kryteriów oceny. W poprzedniej edycji każde wyzwanie biznesowe miało odrębne zasady, co uniemożliwiało porównywanie zespołów między sobą. Przygotowałem jednen, wspólny arkusz ocen, obejmujący dopasowanie strategiczne, wartość dla użytkownika i biznesu, wykonalność, sensowność zastosowania AI oraz gotowość do przejścia poza pilotaż, z dodatkową premią za siłę narracji. Do arkusza dopisałem reguły pomocne dla sędziów,np. która że premii za prezentację nie wolno używać do kompensowania słabej treści. Kryteria zamieniłem następnie w dedykowany szablon w naszym agentycznym rozwiązaniu, którr dzięki temu potrafiło wygenerować zestaw prawdopodobnych pytań od jury na podstawie materiałów zespołu i pomóc się przygotować do ostatecznej prezentacji.

## Efekt

Pięć koncepcji gotowych do prototypowania, z udokumentowanym problemem, beneficjentami, założeniami co do danych, hipotezą wartości i planem MVP. Łączna pula wartości zidentyfikowana przez zespoły przekroczyła 6 mln EUR rocznie — w wariancie kierunkowym, wymagającym walidacji po stronie klienta, co konsekwentnie komunikowaliśmy, żeby nikt nie pomylił projekcji z potwierdzoną oszczędnością.

Zwycięski projekt wyszedł z obszaru łańcucha dostaw i produkcji: platforma decyzyjna dla zakładów produkcyjnych, przewidująca odchylenia procesu, optymalizująca parametry pracy dla danej partii, podpowiadająca operatorom działania korygujące i ucząca się z kolejnych cykli. Zespół zaadresował nim realne straty — wydajność fermentacji poniżej celu, zmienność uzysku, utracone partie i czas reakcji na odchylenie sięgający dobę. Uważam to za najlepszy przykład tego, co chciałem osiągnąć programem: AI wpływająca bezpośrednio na wskaźniki operacyjne i rentowność produkcji, a nie kolejne usprawnienie pracy biurowej.

Satysfakcja uczestników wyniosła 4,5 na 5, a NPS po dniu otwierającym przekroczył +70.

## Czego się nauczyłem

Po pierwsze, kwestionariusz przed wydarzeniem był najtańszym elementem programu i jednym z najbardziej wartościowych. Kilka godzin pracy dało mi konkretną wiedzę o tym, co przyciąć, a co rozwinąć — zamiast zgadywania na sali.

Po drugie, gotowość techniczna po stronie klienta to ryzyko, które trzeba testować, a nie deklarować. Drugiego dnia okazało się, że firewall przepuszcza do narzędzia wyłącznie pliki markdown i CSV, blokując PDF-y i obrazy. Lokalny zespół IT odblokował to w trakcie, ale kilkadziesiąt minut pracy zespołów zostało straconych. Przy kolejnych edycjach test end-to-end z udziałem IT klienta wchodzi do zakresu obowiązkowo.

Po trzecie, jestem mocno zorientowany na pracę i przy planowaniu drugiego dnia nie zaplanowałem żadnych aktywności rozluźniających. Zwrócili mi na to uwagę koledzy z zespołu i mieli rację — dołożone ćwiczenia przełamujące rytm wyraźnie poprawiły energię grupy po przerwie obiadowej. Warsztat to nie tylko agenda merytoryczna.

Na koniec kwestia, która w tego typu wydarzeniach bywa pomijana: dane. Po finale klient otrzymał komplet materiałów wejściowych i wyjściowych wytworzonych w narzędziu, a instancja została wyłączona i skasowana wraz z potwierdzeniem, że nie zostały na niej żadne pliki. Warto mieć to zaplanowane od początku, a nie ustalać po fakcie.
