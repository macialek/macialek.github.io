---
layout: post
title:  "Standardy programowania wspierane przez AI"
date:   2026-03-18 09:30:00 +0100
categories: kariera
tags: kariera cv genai standardy
author: Maciej Michałek
---
Asystenci kodu weszli do zespołów szybciej, niż powstały zasady ich używania. Efektem był rozjazd: różne konfiguracje lokalne, różni dostawcy modeli, różna jakość tego, co ostatecznie trafiało do repozytorium.

Celem było ustandaryzowanie pracy z AI w wytwarzaniu oprogramowania bez spowalniania zespołów i bez zamieniania standardu w dokument, którego nikt nie czyta.

Współtworzyłem firmowe standardy programowania w Pythonie oparte na trzech filarach. Pierwszy to skonteneryzowane środowiska deweloperskie — identyczne u każdego programisty, a także dla agenta kodującego, co eliminuje całą klasę problemów typu „u mnie działa”. Drugi to zarządzanie kontekstem dla asystentów, żeby model pracował na tej samej wiedzy o projekcie co człowiek. Trzeci to automatyczne bramki jakości w CI/CD zamiast ręcznego pilnowania zasad podczas code review.

Osobnym elementem było ujednolicenie nazewnictwa struktury repozytoriów. Wydaje się banalne, dopóki nie okaże się, że folder „infrastructure” oznacza coś zupełnie innego dla architekta pracującego w modelu heksagonalnym, a coś innego dla inżyniera DevOps — i że ta kolizja semantyczna myli nie tylko ludzi, ale też agentów kodujących.

Praktyczne znaczy sprawne, a nie niedbałe. Mnóstwo zysku z AI w kodzie bierze się nie z szybszego pisania, lecz z tego, że nie trzeba pisać rzeczy, które już były rozwiązane.
