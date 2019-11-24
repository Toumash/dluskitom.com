---
title: "Polly - obowiązkowa biblioteka do komunikacji HTTP"
date: 2019-11-24T16:27:30+02:00
publishDate: "2019-11-24T17:17:22+02:00"
draft: false
---

W jaki sposób obsługujesz zapytania internetowe w swojej aplikacji?
Co się stanie, jeśli jakiś request zwyczajnie nie "pójdzie w świat"? Co będzie jeśli się zawiesi.
A w przypadku chwilowego downtime-u twojej usługi?

Wszystkie te problemy rozwiązuje nam biblioteka o nazwie `Polly`.
Pozwala nam ona na deklaratywne definiowanie zasad postępowania w przypadku błędu komunikacji.

Na poniższym przykładzie widać wykorzystanie prostej akcji próbowania requestów po czasie 1s a potem 2s w razie występienia błędu usługi, lub timeoutu.
{{< gist toumash 9d28ae65044ff6e1ee00c3d82b55b909 >}}

## Do czego stosować?

U mnie największą przydatność taka biblioteka posiada w przypadku masowego wywoływania jakiegoś api.
Dzięki zastosowaniu takich konstrukcji polityk retry-ów mogę spokojnie wywoływać usługi na paru wątkach, bo wiem, że jak coś pójdzie nie tak, to w przypadku błędu usługa zostanie zwyczajnie zapytania kolejny raz o to samo :)

## A co z frontendem?

Dla frontendowców także mamy coś dobrego - biblioteka [Fetch-Retry](https://www.npmjs.com/package/fetch-retry) robi dokładnie to samo co Polly dla dotnetu :)