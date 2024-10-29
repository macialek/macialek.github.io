---
layout: post
title:  "Portfolio"
date:   2024-04-17 09:36:52 +0100
categories: kariera
tags: kariera cv
author: Maciej Michałek
---
Co nieco o projektach, które zrealizowałem.

## Narzędzie streszczania komentarzy i śledzenia ich tonu

Rozwiązanie korzysta z aktualizowanych raz na dobę danych dotyczących komentarzy zostawianych pod produktami przedsiębiorstwa sprzedawanymi na różnych platformach eCommerce. Z wykorzytaniem GPT4 turbo ocenia ton danego komentarza (pozytywny, negatywny, neutralny) oraz w zadanym oknie czasowym, z wykorzystaniem przygotowanych promptów streszcza treść komentarzy, opisując przy tym pewne konretkne aspekty, jak uwagi dotyczące jakości, czasu dostawy oraz pomysły na rozwój produktów. Dane są przetwarzane batchowo, zapisywane w data lake, wizualizowane jako dodatkowa warstwa analityczna w PBI.

## Narzędzie weryfikacji publikowanych treści pod kątem zgodności z wytycznymi dotyczącymi ekspozycji marki

Celem projektu było pobranie kreacji publikowanych w różnych mediach społecznościowych i wewnętrznych kanałach komunikacji klienta, a następnie ich walidacja pod kątem zgodności z wytycznymi dotyczącymi prezentowania marki i zwizualizowanie uzyskanych danych w postaci raportu. Byłem odpowiedzialny za defincję problemu z klientem i przygotowanie pomysłu na jego rozwiązanie oraz architektury rozwiązania. W projekcie uczestniczyłem także w roli lidera technologicznego, dbając o zapewnienie ciągłego dostarczania ustalonego zakresu w pożądanej jakości. Samodzielnie zaprogramowałem kilka modułów rozwiązania, wykonywałem rewizje dostarczanego kodu. Rozwiązanie od strony data science korzysta z klasycznego podejścia CV wzbogaconego rozpoznawaniem obiektów z wykorzystaniem modelu Yolo. Architekturalnie to grupa niezależnych mikroserwisów obudowanych API (fastAPI), skonteneryzowanych i wdrożonych jako Web App na dedykowanym App Service Plan. 

## Generowanie opisów produktów klienta z branży meblarskiej korzystającego z systemy Magento dla eCommerce

Celem projektu było wygenerowanie i zapewnienie możliwości dalszego generowania opisów produktów w oparciu o ich zdjęcia i elementy opisu (np. wymiary) zawarte w bazie danych. Wygenerowane opisy miały być wielojęzyczne. W ramach prac zapewniłem połączenie z Magento API (pobieranie i wysyłanie danych) oraz wygenerowanie i walidację niezbędnych opisów z użyciem modelu GPT4o. Rozwiązanie zostało wdrożone 

## 

## Narzędzie wykrywania defektów w szklanych opakowaniach

Celem projektu było wykorzystanie zdjęć wykonywanych w podczerwieni butelkom na linii produkcyjnej tuż po rozdmuchu i wykorzystanie sztucznej inteligencji do wykrywania potencjalnych wad. W projekt byłem zaangażowany jako Data Scientist i odpowiedzialny za przygotowanie PoC. Po rozmowach z ekpertami zaimplementowałem dwa mechanizmy sprawdzania anomalii. Jeden, uniwersalny mechanizm niezależny od typu rozdmuchiwanej butelki opierał się na odnajdywaniu jej osi symetrii i badaniu podobieństwa pomiędzy wyznaczonymi połówkami. Różnica z dużym prawdopodobieństwem oznacza wadę. Zaletą tego rozwiazania jest szybkość, bez problemu może być wdrożone jako rozwiązanie typu embedded działające bezpośrednio przy kamerze przemysłowej. Drugie podejście korzystało z oznakowanych danych. Na przygotowanym razem z ekspertami zbiorze danych oznaczone zostały prostokąty zawierające defekty wraz z typem defektu. Zbiór treningowy następie poszerzyłem technikami augmentacji, wyszkoliłem na nim kilka popularnych modeli oraz model o samodzielnie zdefiniowanej architekturze (Tensorflow, w oparciu o pracę naukowców opisaną w artykule dostępnym w arXiv). Rozwiązanie zapewniało niezbędną skuteczność i szybkość działania.


## Platforma automatycznego generowania i publikowania artykułów

Celem projektu było wytworzenie platformy, która będzie pozwalała publikować artykuły o charakterystyce lokalnej z użyciem ustrukturyzowanych źródeł danych, poddawanych przetwarzaniu statystycznemu.
W ramach projektu wytworzona została logika publikacji artykułów, pobierania danych, scrapowania danych.
Rozwiązanie wytworzone jest w całości w języku Python, uruchamiane w wyizolowanym środowisku kontenera Docker.
Obecnie projekt jest nadal rozwijany, przeszkoleni pracownicy Redakcji samodzielnie tworzą nowe cykle artykułów w ramach udostępnionych im źródeł danych i bibliotek.

## Automatyczna kategoryzacja i tagowanie artkułów

Celem projektu była poprawa jakości opisywania materiałów wytwarzanych przez redakcje. W ramach prac badawczych porównano kilka technik NLP, w celu wyłonienia tej, która zapewni najlepszą jakość kategoryzacji artykułów.
Modele były szkolone w oparciu o należące do Polska Press Grupy zbiory artykułów. Efektywność była testowana na dodatkowo zmoderowanym, osobnym zbiorze testowym.
Wybrana technika przetwarzania została oprogramowana w języku Python i wdrożona w środowisku produkcyjnym, jako mikrousługa wykorzystywana przez CMS. 

## Ochrona marek Klientów

Celem projektu było zasilanie serwera reklamowego wykorzystywanego przez Polska Press Grupę informacjami, dotyczącymi treści potencjalnie niechcianych przez klientów reklamowych. W ramach projektu przeprowadzono prace badawczo-rozowojowe,
wyłajaniające najprostsze rozwiązanie zapewniające pożądany próg dokładności klasyfikacji. Wybrana technologia przetwarzania została wdrożona w środowisku produkcyjnym jako mikrousługa wykorzystywana przez CMS.

## Silnik rekomendacyjny oparty o treści

Celem projektu było poprawienie wyników CTR treści polecanych w portfolio artykułów Polska Press Grupy. Zaprojektowana i oprogramowana mechanika korzysta z bieżących danych analitycznych dotyczących odsłon artykułów oraz modelu językowego określającego podobieństwo materiałów.

## Narzędzie generowania transkrypcji wywiadów dla dziennikarzy

Projekt miał na celu wytworzenie rozwiązania pozwalającego zamieniać nagrania przeprowadzanych prez dziennikarzy wywiadów na teksty ze znacznikami czasowymi. 
Po analizie dostępnych technologii zdecydowaliśmy się korzystać z API udostępnianego w ramach chmury Azure Microsoftu. Rozwiązanie jest produkcyjnie wdrożone jako mikrousługa wykorzystywana przez CMS.

## Automatyzacja obsługi dziennikarskiej wyborów samorządowych

Projekt miał na celu automatyzację obsługi wyborów samorządowych. Ze względu na mnogość lokalizacji, obsługa takich zagadnień jest dużym wyzwaniem logistycznym. W ramach prac połączono ze sobą dane z GUS i Państwowej Komisji Wyborczej.
W publikowanych automatycznie artkułach, opartych o przygotowane redakcyjnie szablony, informowane na poziomie lokalnym o lokalach wyborczych, listach kandydatów oraz wynikach wyborów. 
Przygotowane oprogramowanie jest wykorzystywane także do obsługi innego typu wyborów, zapewniające możliwość analizy i prezentacji wyników w kontekście lokalnym.

## Wyszukiwanie tekstowe nieopisanych zdjęć

Projekt miał na celu umożliwienie sprawnego przeszukiwania bardzo dużego repozytorium zdjęć grupy. Warunkiem brzegowym było założenie, że zdjęcia nie zawierają żadnego opisu tekstowego. Zaprojektowane rozwiązanie buduje embeddingi dla każdego zdjęcia z repozytorium oraz dla szukanych fraz i następnie wydajnie szuka najbliższych sąsiadów w bardzo dużym zbiorze wektorów (o długości 512 wartości float32).