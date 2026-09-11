---
layout: post
title: "Silnik rekomendacji treści i wycena potencjału artykułu"
date: 2024-04-19
categories: kariera
tags: [portfolio, ai, machine-learning]
excerpt: "Co czytelnik przeczyta następne — i czy ten tekst warto było napisać."
---

Co czytelnik przeczyta następne — i czy ten tekst warto było napisać.

**Okres:** 2019 – 2021  
**Klient:** Duży wydawca prasowy  
**Moja rola:** Head of AI/ML — projekt, wdrożenie, 80% pracy hands-on

## Kontekst

Redakcja produkowała ogromne wolumeny treści bez systematycznej wiedzy o tym, które teksty faktycznie budują zasięg i przychód.

## Wyzwanie

Rekomendacje oparte na popularności prowadzą do bańki: promują to, co już się promuje. Potrzebne było podejście oparte na treści, działające także dla artykułów bez historii odsłon.

## Rozwiązanie

Silnik rekomendacji content-based operujący na reprezentacji tekstu, uzupełniony modelami szacującymi potencjalną wartość artykułu jeszcze przed publikacją oraz — osobno — automatyką multi-armed bandit zapewniającą ciągłe testowanie zakładanej efektywności artykułu na części populacji i uzalażnianie cyklu życia materiału od wyniku eksperymentu.

## Efekt

Rekomendacje działające od pierwszej minuty życia artykułu i dane wejściowe do decyzji redakcyjnych o alokacji pracy i doborze tematów.

## Czego się nauczyłem

Modele oparte na popularności są łatwe do wdrożenia i trudne do obrony. Podejście oparte na treści wymaga więcej pracy, ale rozwiązuje zimny start — a w mediach zimny start to codzienność.

**Technologie:** Python, NLP, Scikit-learn, TensorFlow, SQL
