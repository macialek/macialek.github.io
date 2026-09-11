---
layout: post
title: "Wyszukiwarka tekstowa dla nieopisanych zdjęć"
date: 2024-04-30
categories: kariera
tags: [portfolio, ai, machine-learning]
excerpt: "Milion fotografii bez metadanych i jedno pole wyszukiwania."
---

Milion fotografii bez metadanych i jedno pole wyszukiwania.

**Okres:** 2021 – 2022  
**Klient:** Duży wydawca prasowy  
**Moja rola:** Senior data scientist / inżynier automatyzacji

## Kontekst

Archiwum fotograficzne rosło od lat, a opisy zdjęć powstawały nieregularnie. Praktycznie oznaczało to, że duża część zasobu była niedostępna — istniała, ale nie dało się jej znaleźć.

## Wyzwanie

Ręczne opisanie archiwum było nierealne kosztowo. Redaktor potrzebował wpisać „protest przed urzędem, zima” i dostać sensowne wyniki.

## Rozwiązanie

Wyszukiwanie oparte na wspólnej przestrzeni reprezentacji obrazu i tekstu, wystawione jako API i wdrożone na Kubernetes. Do tego pipeline'y ETL i analiza dużych wolumenów w PySpark i BigQuery.

## Efekt

Archiwum stało się przeszukiwalne bez etapu ręcznego opisywania.

## Czego się nauczyłem

Najszybszą drogą do wartości bywa zmiana definicji problemu. Zamiast „jak opisać milion zdjęć” warto zapytać „jak znaleźć zdjęcie bez opisu”.

**Technologie:** Python, TensorFlow, embeddingi obrazu i tekstu, Kubernetes, GCP, BigQuery
