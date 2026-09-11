---
layout: post
title:  "Predykcja zużycia narzędzi w utrzymaniu ruchu"
date:   2024-07-09 11:05:00 +0200
categories: kariera
tags: kariera cv machine-learning
author: Maciej Michałek
---
Narzędzia na linii produkcyjnej wymieniano według stałego harmonogramu. Część trafiała do wymiany zbyt wcześnie, generując zbędny koszt. Część zbyt późno, generując przestój i braki jakościowe.

Zużycie narzędzia zależy od obrabianego materiału, parametrów pracy i historii eksploatacji. Sygnał jest zaszumiony, a zdarzeń awarii — na szczęście dla klienta, mniej szczęśliwie dla modelu — jest bardzo mało. Zbudowałem model szacujący pozostały czas pracy narzędzia na podstawie danych procesowych i historii użycia, z progami alarmowymi różnicowanymi według krytyczności stanowiska.

Technologicznie: Python, Scikit-learn, analiza szeregów czasowych, dane z czujników.

Wniosek, który wyniosłem z tego projektu: predictive maintenance sprzedaje się jako problem modelowania, a w praktyce jest problemem zaufania. Pierwszy fałszywy alarm kosztuje więcej zaufania operatorów, niż pierwsza trafna predykcja jest w stanie zbudować. Dobór progu decyzyjnego okazał się ważniejszy niż wybór rodziny modeli.
