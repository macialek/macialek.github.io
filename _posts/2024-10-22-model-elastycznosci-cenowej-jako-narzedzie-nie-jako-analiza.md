---
layout: post
title:  "Model elastyczności cenowej jako narzędzie, nie jako analiza"
date:   2024-10-22 10:30:00 +0200
categories: kariera
tags: kariera cv machine-learning
author: Maciej Michałek
---
Klient, globalny producent alkoholi premium, dysponował modelem elastyczności cenowej działającym jako zestaw notatników na Databricks. Model dawał liczby, ale nie dawał procesu: nie rozróżniał elastyczności promocyjnej od regularnej, nie uwzględniał sezonowości i nie skalował się na kolejne rynki.

Istotna trudność merytoryczna polega na tym, że decyzja cenowa nie jest decyzją o jednym produkcie. Obniżka ceny jednego SKU przesuwa sprzedaż w obrębie całej rodziny marki, a konkurencja reaguje. Model, który tego nie widzi, prowadzi do dobrych decyzji lokalnych i złych globalnych.

W ramach prac zastąpiliśmy notatniki elastycznym frameworkiem z wersjonowaniem modeli i śledzeniem jakości. Przetestowaliśmy kilka rodzin modeli, w tym log-log z efektami losowymi oraz double machine learning, oceniając je na trzech osiach: trafność, odporność i złożoność obliczeniowa — ta ostatnia miała znaczenie ze względu na plan ekspansji na kolejne rynki. Do modelu weszło rozróżnienie promo i non-promo, czynnik sezonowy oraz efekt kanibalizacji liczony przez elastyczności krzyżowe.

Wyniki trafiają bezpośrednio do Power BI, gdzie użytkownik biznesowy samodzielnie buduje scenariusze „co jeśli”, wraz z założeniami dotyczącymi ruchów konkurencji, i widzi efekt na poziomie całej marki, a nie pojedynczego produktu.

Technologie: Python, Azure, Databricks, Power BI.
