---
layout: post
title:  "Portfolio"
date:   2020-12-17 14:28:52 +0100
categories: kariera
tags: kariera cv
author: Maciej Michałek
---
Co nieco o projektach, które zrealizowałem.

## Platforma automatycznego generowania i publikowania artykułów
Celem projektu było wytworzenie platformy, która będzie pozwalała publikować artykuły o charakterystyce lokalnej z użyciem ustrukturyzowanych źródeł danych, poddawanych przetwarzaniu statystycznemu. 
W ramach projektu wytworzona została logika publikacji artykułów, pobierania danych, scrapowania danych.
Rozwiązanie wytworzone jest w całości w języku Python, uruchamiane w wyizolowanym środowisku kontenera Docker.
Obecnie projekt jest nadal rozwijany, przeszkoleni pracownicy Redakcji samodzielnie tworzą nowe cykle artykułów w ramach udostępnionych im źródeł danych i bibliotek.

## Automatyczna kateogryzacja i tagowanie artkułów
Celem projektu była poprawa jakości opisywania materiałów wytwarzanych przez redakcje. W ramach prac badawczych porównano kilka technik NLP, w celu wyłonienia tej, która zapewni najlepszą jakość kategoryzacji artykułów. 
Modele były szkolone w oparciu o należące do Polska Press Grupy zbiory artykułów. Efektywność była testowana na dodatkowo zmoderowanym, osobnym zbiorze testowym.
Wybrana technika przetwarzania została oprogramowana w języku Python i wdrożona w środowisku produkcyjnym, jako mikrousługa wykorzystywana przez CMS. 

## Ochrona marek Klientów
Celem projektu było zasilanie serwera reklamowego wykorzystywanego przez Polska Press Grupę informacjami, dotyczącymi treści potencjalnie niechcianych przez klientów reklamowych. W ramach projektu przeprowadzono prace badawczo-rozowojowe, 
wyłajaniające najprostsze rozwiązanie zapewniające pożądany próg dokładności klasyfikacji. Wybrana technologia przetwarzania została wdrożona w środowisku produkcyjnym jako mikrousługa wykorzystywana przez CMS.

## Silnik rekomendacyjny oparty o treści

## Narzędzie generowania transkrypcji wywiadów dla dziennikarzy
Projekt miał na celu wytworzenie rozwiązania pozwalającego zamieniać nagrania przeprowadzanych prez dziennikarzy wywiadów na teksty ze znacznikami czasowymi. 
Po analizie dostępnych technologii zdecydowaliśmy się korzystać z API udostępnianego w ramach chmury Azure Microsoftu. Rozwiązanie jest produkcyjnie wdrożone jako mikrousługa wykorzystywana przez CMS.

## Automatyzacja obsługi dziennikarskiej wyborów samorządowych
Projekt miał na celu automatyzację obsługi wyborów samorządowych. Ze względu na mnogość lokalizacji, obsługa takich zagadnień jest dużym wyzwaniem logistycznym. W ramach prac połączono ze sobą dane z GUS i Państwowej Komisji Wyborczej.
W publikowanych automatycznie artkułach, opartych o przygotowane redakcyjnie szablony, informowane na poziomie lokalnym o lokalach wyborczych, listach kandydatów oraz wynikach wyborów. 
Przygotowane oprogramowanie jest wykorzystywane także do obsługi innego typu wyborów, zapewniające możliwość analizy i prezentacji wyników w kontekście lokalnym.