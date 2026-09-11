---
layout: post
title:  "Produktyzacja i wdrożenie modeli ML w 28 rynkach"
date:   2025-09-24 11:40:00 +0200
categories: kariera
tags: kariera cv mlops
author: Maciej Michałek
---
Klient, jeden z największych rozlewników napojów na świecie, przeprowadził udany PoC modeli optymalizujących kanał detaliczny i działania marketingowe. Następnie potrzebował partnera do produktyzacji i wdrożenia rozwiązania na 28 rynkach — przy bardzo napiętym harmonogramie i równoległej modernizacji architektury danych, co istotnie podnosiło złożoność dostarczania.

Kod z PoC nie jest produktem. Do tego każdy rynek wnosi własne wymagania, a źródła danych migrują w trakcie trwania rolloutu. Wdrażanie sekwencyjne, rynek po rynku, nie mieściło się w żadnym realnym kalendarzu.

Zbudowaliśmy framework techniczny pozwalający prowadzić rollouty równolegle, partiami po trzy do sześciu rynków. Do architektury danych klienta weszły nowe komponenty: biblioteka wejścia i wyjścia danych, rejestr modeli MLflow oraz skalowanie orkiestracji w Azure Data Factory. Wyprodukcjonalizowane zostały cztery moduły ML wraz z licznymi personalizacjami rynkowymi: mikrosegmentacja klientów, rekomendacja asortymentu, potencjał wartości klienta i rekomendowana częstotliwość wizyt handlowych.

Rezultaty: czas wdrożenia pojedynczego rynku spadł z dwóch miesięcy do około półtora tygodnia, koszt przetwarzania zmniejszył się o 50%, a czas przetwarzania o 40%.

Technologie: Azure, Databricks, Python, MLflow, Azure Data Factory.

Przyspieszenie rzędu trzy do pięciu razy nie wzięło się z lepszych modeli. Wzięło się stąd, że personalizacja rynkowa dostała własne, wyraźnie odgraniczone miejsce w strukturze kodu.
