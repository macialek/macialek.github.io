---
layout: post
title:  "Wykrywanie kanibalizacji produktów"
date:   2024-09-10 08:55:00 +0200
categories: kariera
tags: kariera cv machine-learning
author: Maciej Michałek
---
Klient — międzynarodowa sieć handlowa z branży wyposażenia wnętrz — wprowadza na rynek tysiące produktów rocznie. Ocena, które nowości zjadają sprzedaż istniejących pozycji z portfela, opierała się na intuicji kategorii menedżerów. Brakowało też odpowiedzi na pytanie, czy wprowadzenie danego produktu ostatecznie się opłaciło.

Trudność jest natury metodologicznej: nie da się zaobserwować sprzedaży, która wystąpiłaby, gdyby nowy produkt nigdy nie powstał. A bez tej wielkości pytanie o opłacalność pozostaje bez rzetelnej odpowiedzi.

Zbudowaliśmy automatyczną detekcję par produktów wykazujących kanibalizację oraz model przewidujący sprzedaż produktu kanibalizowanego w scenariuszu kontrfaktycznym — tak, jak gdyby nowość nie została wprowadzona. Różnica między prognozą kontrfaktyczną a obserwacją daje estymację utraconej sprzedaży.

Rozwiązanie w Pythonie na Azure Databricks. Efektem jest obiektywna i powtarzalna ocena interakcji między produktami w portfelu, skrócony czas przygotowania analizy oraz podstawa do poprawy ROI wprowadzeń.

Pytanie „czy to się opłaciło” prawie zawsze jest pytaniem kontrfaktycznym. Zespoły, które tego nie nazwą wprost, będą w nieskończoność porównywać okresy rok do roku.
