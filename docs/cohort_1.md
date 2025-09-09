---
layout: default
---

<img class="article-img" src="/assets/img/cohort_1_0.jpg" alt="Main Picture">
<p style="font-size: 10px; text-align: right; margin-top: 0px;">Foto von <a href="https://unsplash.com/@nate_dumlao?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">Nathan Dumlao</a> auf <a href="https://unsplash.com/photos/group-of-people-standing-in-front-of-food-stall-counter-66RxrYlPShI?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">Unsplash</a></p>
<h1>Wie lange bleiben Ihre Kunden? Eine datenbasierte Analyse der Kundenbindung</h1>
September 09, 2025

Kundenbindung ist entscheidend für den Erfolg eines Unternehmens. Denn die Gewinnung eines neuen Kunden ist fünf- bis siebenmal teurer als die Bindung eines bestehenden Kunden. Eine gängige Methode, mit der Unternehmen die Kundenbindung analysieren, ist die Kohortenanalyse.

Die Kohortenanalyse hilft dabei, das Kundenverhalten über einen bestimmten Zeitraum hinweg zu verstehen, indem Personen gruppiert werden, die ein gemeinsames Merkmal innerhalb eines definierten Zeitraums teilen – typischerweise ihre erste Interaktion oder ihren ersten Kauf. Diese Gruppe wird als Kohorte bezeichnet.

Eine Kohortenanalyse umfasst in der Regel:
1. Die Gruppierung von Kunden nach dem Monat ihres ersten Kaufs
2. Die Verfolgung der Kundenbindung, indem beobachtet wird, wie viele dieser Kunden in den Folgemonaten zurückkehren
3. Die Visualisierung dieser Daten in einer Matrix oder Heatmap, um Trends zu erkennen

In meinem E-Commerce-Datensatz habe ich die Kunden basierend auf dem Monat ihres ersten Kaufs gruppiert und anschließend verfolgt, wie viele von ihnen in den darauffolgenden Monaten zurückgekehrt sind.

<h2>Durchführung einer Kohortenanalyse mit Python</h2>
Mein Datensatz enthält Transaktionsdaten von Produktverkäufen mit Feldern wie Rechnungsdatum, Rechnungsnummer, Kunden-ID, Produktbeschreibung, Produktkategorie und weiteren. Die relevanten Felder für die Kohortenanalyse sind Rechnungsdatum, Rechnungsnummer und Kunden-ID.

![Dataset_sample](/assets/img/cohort_1_1.jpg)

Basierend auf diesen drei Spalten habe ich drei neue Spalten erstellt – Rechnungsmonat, Kohortenmonat und Kohortenindex. Der Rechnungsmonat extrahiert einfach den Monatsanteil des Rechnungsdatums. Der Kohortenmonat ermittelt den Monat des ersten Kaufs für jeden Kunden. Der Kohortenindex berechnet die Differenz zwischen dem Rechnungsmonat und dem Kohortenmonat. Je länger der Kohortenindex eines Kunden ist, desto stärker ist die Bindung zum Unternehmen.

![Python_code](/assets/img/cohort_1_3.jpg)

Der Kohortenindex zeigt, wie lange ein Kunde dem Unternehmen treu bleibt. Unser Ziel ist jedoch ein umfassenderer Überblick – nämlich herauszufinden, wie viele Kunden insgesamt in jedem Monat bleiben. Um das zu ermitteln, habe ich die Tabelle so umstrukturiert, dass der Kohortenmonat als Zeilen, die Kohortenindizes als Spalten und die Anzahl der Kunden als Werte dargestellt werden, wie unten gezeigt.

![Cohort_Matrix](/assets/img/cohort_1_2.jpg)

Diese Matrix zeigt, dass die Kunden, die im Dezember 2010 gewonnen wurden, länger bleiben. Ein weiterer Trend ist, dass die Kundenbindung stark von Monat 0 zu Monat 1 abnimmt, was auf ein schlechtes Onboarding oder mangelnde Kundenbindung hinweisen könnte. Schließlich gewinnt das Unternehmen regelmäßig etwa 20 % seiner ursprünglichen Kunden zurück.

Vorschläge:
1. Eine vereinfachte Erstkauf-Erfahrung kann die Kundenbindung im ersten Monat verbessern.
2. Die Einführung von Treueprogrammen oder personalisierten Empfehlungen kann die Gesamtbindung erhöhen.
3. Die Bindungsraten können genutzt werden, um den Umsatz zu schätzen, den jede Kohorte generieren wird.

_[Ursprünglich auf [LinkedIn](https://www.linkedin.com/pulse/wie-lange-bleiben-ihre-kunden-eine-datenbasierte-analyse-sekar-kdh0e) veröffentlicht]_
