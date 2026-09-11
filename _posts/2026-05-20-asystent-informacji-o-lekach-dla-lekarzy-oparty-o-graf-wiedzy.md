---
layout: post
title:  "Asystent informacji o lekach dla lekarzy oparty o graf wiedzy"
date:   2026-05-20 10:45:00 +0200
categories: kariera
tags: kariera cv genai rag
author: Maciej Michałek
---
Projekt realizowany dla wiodącej firmy farmaceutycznej. Lekarze potrzebują szybkiego dostępu do rzetelnej informacji o lekach — dawkowaniu, przeciwwskazaniach, interakcjach — a producent potrzebuje sposobu na wprowadzenie ich w nowe leki i terapie. Rynek jest silnie regulowany, a system w rozumieniu AI Act klasyfikuje się jako średniego ryzyka.

Klasyczny RAG oparty o embeddingi radzi sobie dobrze z pytaniami ogólnymi i zawodzi dokładnie tam, gdzie jest najważniejszy: na nazwach własnych leków, jednostkach dawkowania i relacjach między substancjami. W tej dziedzinie halucynacja nie jest usterką kosmetyczną.

Uporządkowałem wiedzę farmaceutyczną w dedykowaną taksonomię łączącą wiele źródeł danych. Dołożyliśmy wyspecjalizowane rozpoznawanie encji dla terminów medycznych i nazw leków, a retrieval oparliśmy na grafie — model językowy dostaje kontekst wynikający z relacji między bytami, a nie z podobieństwa tekstu. Odpowiedź jest generowana warstwowo i zawsze z cytowaniem źródła, a każde wywołanie modelu jest śledzone w Langfuse, co daje pełną audytowalność rozwiązania.

Osobnym, istotnym obszarem mojej pracy była rama oceny jakości: definicja metryk zrozumiałych dla nietechnicznego interesariusza i kategoryzacja typów błędów. Oceniona trafność odpowiedzi wyniosła około 95%, a w obszarach krytycznych — dawkowanie i przeciwwskazania — około 99%.

Technologie: Python, Azure, LangGraph, Cosmos DB z API Gremlin, Langfuse.

Zanim zacznie się mierzyć halucynacje, trzeba zdefiniować, czym jest odpowiedź poprawna. Zbudowanie ramy oceny okazało się trudniejsze niż zbudowanie samego retrievalu.
