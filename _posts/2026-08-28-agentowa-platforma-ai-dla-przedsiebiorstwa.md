---
layout: post
title:  "Agentowa platforma AI dla przedsiębiorstwa"
date:   2026-08-28 09:50:00 +0200
categories: kariera
tags: kariera cv genai agenty architektura
author: Maciej Michałek
---
Organizacje, z którymi pracowałem, przeszły w ostatnich latach ten sam cykl. Najpierw jeden chatbot oparty o RAG. Potem drugi. Potem dziesięć — każdy z własnym uwierzytelnianiem, własnym dostawcą modeli i własnym pomysłem na logowanie. Koszt utrzymania zaczął rosnąć szybciej niż dostarczana wartość.

Potrzebny był fundament pozwalający zespołom budować agentów bez powtarzania tej samej pracy: wspólne uwierzytelnianie, wspólny routing do modeli, wspólna obserwowalność i jasne granice odpowiedzialności między agentem, narzędziem a danymi.

Zaprojektowałem platformę opartą o wzorzec backend-for-frontend. Aplikacja SPA nigdy nie przechowuje tokenów, sesja żyje po stronie backendu, a dostęp do modeli prowadzi przez jedno proxy z limitami i rozliczaniem kosztów w podziale na zespoły. Agenci są budowani w LangGraph i wystawiani przez ustandaryzowane protokoły, dzięki czemu jeden agent może być narzędziem dla drugiego bez pisania integracji od zera. Całość działa na Azure Container Apps, z infrastrukturą opisaną deklaratywnie i pełnym śladem wykonania zbieranym w Langfuse.

Technologie: Python, LangGraph, FastAPI, Azure Container Apps, Entra ID, LiteLLM, Langfuse, Docker, Terraform.

Nowy agent startuje z gotowym uwierzytelnianiem, obserwowalnością i politykami bezpieczeństwa, zamiast budować je od podstaw. Koszt inferencji stał się mierzalny i przypisany do konkretnego zespołu, a nie do jednej wspólnej faktury na koniec miesiąca.

Najdroższym elementem platformy agentowej nie jest model. Są nim granice: kto ma dostęp do jakich danych, kto ponosi koszt i kto odpowiada za treść odpowiedzi. Jeżeli nie rozstrzygnie się tego w architekturze, orkiestrator jedynie rozprowadzi ten problem na większą powierzchnię.
