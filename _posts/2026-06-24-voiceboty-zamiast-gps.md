---
layout: post
title:  "Voiceboty zamiast GPS — śledzenie ciężarówek bez trackerów"
date:   2026-06-24 10:10:00 +0200
categories: kariera
tags: kariera cv genai voice-ai logistyka
author: Maciej Michałek
---
Klient — duży koncern spożywczy działający na Filipinach — realizuje transport wyłącznie przez zakontraktowanych przewoźników zewnętrznych o bardzo różnym poziomie dojrzałości cyfrowej. Znaczna część floty jest wynajmowana i nie ma zainstalowanych nadajników GPS, z których dałoby się korzystać. Skutek jest taki, że nie istnieje jedno źródło prawdy o postępie dostawy: statusy aktualizowane są ręcznie, terminy wyjazdu i przyjazdu są niedokładne, a opóźnienia rozpoznaje się dopiero po fakcie. Planiści spędzają istotną część dnia na dzwonieniu do przewoźników po informację o statusie — praca, która nie skaluje się w żadnym kierunku.

Standardowa odpowiedź na ten problem brzmi: zainstalujcie GPS. Jest kosztowna, wymaga zgody właścicieli wynajmowanej floty i nie obejmie przewoźników, którzy jutro dołączą do sieci. Postawiłem więc pytanie inaczej: skoro kierowca i tak ma telefon, a ręczne dzwonienie działa — tylko nie skaluje się — to co się stanie, jeśli zeskalujemy samo dzwonienie?

Zaprojektowałem rozwiązanie, w którym agent głosowy automatycznie dzwoni do kierowców na trasie i zbiera aktualizację pozycji oraz przewidywanego czasu przyjazdu. Telefony są wyzwalane cyklicznie, według konfigurowalnej reguły, a dodatkowo wtedy, gdy dane śledzenia są nieaktualne lub ich brakuje. Agent prowadzi rozmowę zarówno po angielsku, jak i w języku filipińskim — co w tym kontekście nie jest opcją, tylko warunkiem, żeby kierowca w ogóle odebrał i odpowiedział sensownie. Zebrane dane — pozostały dystans i szacowany czas — trafiają automatycznie do systemu, bez udziału dyspozytora. Warstwa wyznaczania tras oparta jest na usłudze mapowej z routingiem uwzględniającym czas i specyfikę pojazdów ciężarowych, co pozwala porównać deklarację kierowcy z realistycznym oszacowaniem i wykryć ryzyko opóźnienia.

Kluczowa zaleta tego podejścia jest organizacyjna, nie techniczna. Wymagania wobec kierowcy zewnętrznego przewoźnika sprowadzają się do dwóch: mieć naładowany telefon z zasięgiem i odebrać połączenie. Nie trzeba negocjować montażu sprzętu w cudzych pojazdach ani wdrażać aplikacji w firmach, nad którymi nie ma się kontroli. To samo rozwiązanie działa dla floty własnej i obcej.

Zakres rozwiązania objął panel administracyjny do zarządzania kierowcami, centrami dystrybucyjnymi, pojazdami i trasami, wizualizację tras i pojazdów na mapie, silnik reguł biznesowych konfigurowalnych również w języku naturalnym, detekcję ryzyka opóźnienia oraz konfigurowalny wyzwalacz połączeń cyklicznych. Świadomie zostawiłem poza zakresem integrację z systemami ERP i GPS, uwierzytelnianie korporacyjne oraz rozpoznawanie tablic rejestracyjnych z kamer — to są rozszerzenia mające sens dopiero po potwierdzeniu, że sam mechanizm działa.

Technologie: Python, ElevenLabs (agent konwersacyjny), Twilio, HERE Maps (routing dla pojazdów ciężarowych z uwzględnieniem czasu), Azure, PostgreSQL, Azure Static Web Apps.

Zbudowałem działające demo i przedstawiłem je klientowi, a następnie przygotowałem strukturę podziału prac oraz plan czterotygodniowego wdrożenia dowodu koncepcji — od warsztatu dotyczącego polityki AI i konfiguracji środowiska, przez integracje i logikę wyzwalania połączeń, po strojenie agenta głosowego i testy akceptacyjne. Klient potwierdził, że rozwiązanie bezpośrednio adresuje problem ręcznego obdzwaniania dużej liczby kierowców, szczególnie w przypadku floty zewnętrznej.

Wniosek, który uważam za najciekawszy w tym projekcie: najtańsze rozwiązanie problemu widoczności nie polegało na dołożeniu czujników, tylko na zauważeniu, że czujnik już tam jest — siedzi w kieszeni kierowcy i mówi po filipińsku. Rozmowa telefoniczna przestała być wąskim gardłem w momencie, w którym jej koszt krańcowy spadł do pomijalnego poziomu.
