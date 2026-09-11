---
layout: post
title:  "KPI explainer dla procesów magazynowych"
date:   2024-06-11 09:40:00 +0200
categories: kariera
tags: kariera cv analityka
author: Maciej Michałek
---
Menedżerowie centrów magazynowych mieli komplet dashboardów. W momencie pogorszenia wskaźnika wiedzieli o tym natychmiast — i spędzali kolejne dni na ustalaniu, dlaczego.

Celem projektu było rozłożenie zmiany wskaźnika na czynniki, które faktycznie ją wyjaśniają, a nie tylko z nią korelują, oraz przedstawienie wyniku w formie zrozumiałej dla kierownika zmiany, a nie dla analityka.

Zaprojektowałem silnik dekomponujący odchylenie KPI na wkład poszczególnych czynników: struktury zleceń, dostępności zasobów, wydajności sprzętu i zdarzeń zewnętrznych. Kluczową decyzją projektową było wyprowadzenie na pierwszą pozycję rankingu przyczyn sterowalnych — takich, na które odbiorca ma realny wpływ. Idealna atrybucja do czynników niesterowalnych jest analitycznie satysfakcjonująca i operacyjnie bezużyteczna.

Rozwiązanie oparte o Python i Azure Databricks. Efektem było przejście dashboardu z trybu raportowania do trybu odpowiadania na pytanie, co z tym zrobić.
