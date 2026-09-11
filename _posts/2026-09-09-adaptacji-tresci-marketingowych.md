---
layout: post
title:  "Adaptacja treści marketingowych w branży farmaceutycznej"
date:   2026-09-09 11:00:00 +0200
categories: kariera
tags: kariera cv genai architektura agenty
author: Maciej Michałek
---
Demo przygotowane dla globalnego koncernu farmaceutycznego. Problem dotyczy tego, co dzieje się już po zatwierdzeniu kreacji: agencja tworzy materiał wzorcowy, przechodzi on globalną akceptację, a następnie rynki lokalne adaptują go do własnych wymogów regulacyjnych, języka i odbiorcy. Każda adaptacja staje się osobną wersją z własnym identyfikatorem, poza polem widzenia zespołu globalnego, a autonomia rynków sprawia, że efekty potrafią mocno rozjechać się z materiałem źródłowym.

Mnożnik jest tu bezlitosny: jeden zatwierdzony materiał globalny razy liczba rynków, języków, grup odbiorców, kanałów i formatów. Przy czym każdy wariant musi nadal nieść wszystkie elementy obowiązkowe — informacje bezpieczeństwa, równowagę przekazu, odnośniki do charakterystyki produktu i kody zadań. To nie jest zadanie, które można oddać generatorowi treści i sprawdzić wyrywkowo.

Odpowiadałem za architekturę techniczną rozwiązania. Zaprojektowałem ją wokół jednego środowiska Azure Container Apps, obejmującego aplikację frontendową, API, UI dla HITL oraz samych agentów.

Sam przepływ jest wieloetapowy. Zadania adaptacyjne wykonują się równolegle, korzystając z dynamicznych baz wiedzy opisujących markę, kanał i rynek. Po wygenerowaniu materiał przechodzi przez warstwę walidacji i krytyki z iteracją — model ocenia i poprawia własny wynik, zanim cokolwiek trafi do człowieka. Dopiero potem wchodzi przegląd z udziałem recenzenta, który może wprowadzić poprawki poleceniem w języku naturalnym. Osobnym, niełatwym wymaganiem była izolacja między markami: pełne oddzielenie kontekstu i danych, zrealizowane przez wydzielone kontenery, kontrolę dostępu opartą na rolach i prywatne punkty końcowe.

Technologie: Azure Container Apps, Python, agenci LLM, Azure AI Search, zewnętrzne API generatywne

Wartość demo polegała na pokazaniu zwielokrotnienia liczby wariantów przy zachowaniu elementów obowiązkowych i wyjściu w postaci plików warstwowych, edytowalnych, a nie zamkniętych artefaktów wygenerowanych przez model.

W treściach regulowanych warstwa walidacji jest ważniejsza od warstwy generującej. Model, który tworzy dwadzieścia wariantów, jest tani. Model, który potrafi udowodnić, że wszystkie dwadzieścia niesie komplet wymaganych elementów, jest tym, za co klient faktycznie płaci.
