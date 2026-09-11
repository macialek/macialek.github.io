---
layout: post
title:  "Monitorowanie jakości danych dla krytycznego silnika predykcyjnego"
date:   2025-07-08 09:20:00 +0200
categories: kariera
tags: kariera cv data-engineering
author: Maciej Michałek
---
Duża, krytyczna biznesowo aplikacja predykcyjna u klienta z branży rozlewniczej zwracała wyniki, którym użytkownicy przestali ufać. Istniejące kontrole jakości danych były punktowe, nieskalowalne i nie odpowiadały na pytanie, dlaczego dzisiejszy wynik różni się od wczorajszego.

Problem nie polegał na braku kontroli, lecz na braku wspólnego interfejsu. Każdy moduł weryfikował dane po swojemu, a wyniki nie składały się w żaden obraz całości.

Zaprojektowaliśmy bibliotekę implementującą modularne kontrole jakości udostępniane przez jeden wspólny interfejs — skalowalne reguły z frameworka open source uzupełnione zestawem kontroli własnych, napisanych pod specyfikę domeny. Na wierzchu stanął dashboard pozwalający filtrować wyniki w podziale na projekt, moduł i rynek.

Technologie: Azure Databricks, Python, PySpark.

Efektem jest wzrost wiarygodności wyników aplikacji krytycznej biznesowo oraz możliwość dokładania kontroli do kolejnych aplikacji jako standardowej praktyki. Najistotniejszy okazał się jednak efekt trzeci: świadomość po stronie biznesu, ile konkretnie kosztuje zła jakość danych. Ogólne stwierdzenie, że mamy problem z danymi, nie uruchamia żadnego budżetu. Zestawienie w podziale na rynki i moduły uruchamia go natychmiast.
