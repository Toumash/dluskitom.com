---
title: "Mój Todoist w 2019"
date: 2019-08-20T17:15:30+02:00
draft: false
---


### Cześć i czołem programistyczne freaki ;)

Dzisiejszym tematem, który weźmiemy na tapet jest Todoist. Todoist to przepiękna, darmowa aplikacja na wszystkie urządzenia służąca za niezastąpione narzędzie do GTD (Getting Things Done) -  kto nie słyszał zapraszam do prezentacji Macieja Aniserowicza https://www.youtube.com/watch?v=2-f1z5uvZxQ.

Jeśli to czytasz, to jestem w trakcie tworzenia posta na temat tego w jaki sposób roczpoczać przygodę w produktywnym świecie właśnie z narzędziem klasy todoist [Tutaj](/post/jak-stac-sie-produktywnym)

![Todoist marketing header](todoist-header.png)

## Mój todoist setup 2019

Lista projektów:
![Lista Projektów](todoist-projekty.png)

Dashboard:

![Todoist dashboard](todoist-dashboard.png)

## Jak wygląda mój workflow?

### Dodadawanie zadań

Zgodnie z [GTD](https://pl.wikipedia.org/wiki/Getting_Things_Done) dodawanie zadań zaczynam od "Skrzynki Odbiorczej", w której składuje wszystkie swoje pomysły.
Codziennie wieczorem kategoryzuje zadania ze skrzynki odbiorczej i przydzielam je do odpowiednich kategorii.

### Kategoryzowanie

Zadania księguje sobie na odpowiednie projekty - osobiste/praca.
Każdy ważny projekt trzymam poza tym rozdzieleniem, dlatego też nadchodzące szkolenie z todoista jest osobnym projektem.
 
Dzięki rozłożeniu projektów na 3 sfery - praca, osobiste oraz blog nie boję się odpalać todoista na drugim monitorze w pracy po zastosowaniu filtrów np. Praca.


#### Etykiety
Etykiet używam tylko do dwóch rzeczy:
 - przypisanie osoby z którą muszę pogadać jeśli to zadanie menedżerskie
 - wykonanie telefonu - wtedy mogę wykonać to jako cała seria telefonów



### Gotowe filtry
Jeśli chcesz skopiować filtr ode mnie, zapraszam

Praca: 
{{< highlight plain >}}
(today | overdue )& ##*praca
{{< /highlight>}}
Tydzień poza pracą:
{{< highlight plain >}}
next 7 days & !##*praca
{{< /highlight>}}
Dzisiejsza żaba:
{{< highlight plain >}}
(today | overdue )& p1
{{< /highlight>}}