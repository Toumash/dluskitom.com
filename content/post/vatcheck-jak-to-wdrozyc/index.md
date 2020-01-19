---
title: "Vatcheck - jak to wdrożyć? [Azure]"
date: 2020-01-19T17:17:22+02:00
publishDate: "2020-01-19T17:17:22+02:00"
draft: true
---

W dniu TODO.12.2019 Ministerstwo Finansów opublikowało nowy endpoint do sprawdzania vatu. Jest w to końcu skok w dobrą stronę - w kierunku nowych technologii, ale także nie bez przyczyny.

## Co się zmienia?

Zmienia się typ webserwisu. Ministerstwo przepisało webserwis vatcheck z usługi SOAP (z plikiem wsdl) na aplikację REST (bez pliku schematu).

## Co ze stroną biznesową?

Biznesowo powstał kolejny dodatek - każda firma po dniu 1 stycznia 2020 roku ma **obowiązek** sprawdzać każdy podmiot i jego rachunek bankowy w momencie opłacania faktury. 

## O co chodzi?
Chodzi o status płatnika VATu. Jeśli wyślemy przelew powyżej 15 000,00 zł na rachunek nieistniejący w bazie danych ministerstwa nie będziemy mogli wpisać tej transakcji w koszty.

Ok, po tym przydługim wstępnie moge w końcu przejść do rozwiązania.

Aktualnie ministerstwo wspomina na stronie [xxx]() TODO że liczba zapytań ograniczona jest do 30.

Poniżej przyjrzyjmy się przykładowej implementacji opartej o Microsoft Azure. Wykorzystujemy tutaj darmowe dla wszystkich **Azure Functions**, które przechwytują od użytkownika plik z listą NIPów do sprawdzenia, a następnie kolejkowana jest praca sprawdzająca - tutaj już napisana funkcja azure dokonuje sprawdzenia statusu płatnika VAT oraz kont bankowych dla podanych nipów. Wynik takiej operacji wstawiany jest do drugiego kontenera blob o nazwie `results`.

Poniżej znajduje się diagram zastosowanej architektury.

TODO diagram


Kod
TODO wrzuć jako gist czy coś
https://github.com/Toumash/azure-functions-demo/blob/master/azurefunctionsdemo/FunctionApp1/Function1.cs

