---
layout: default
---

## Welcome to another page

<h1>Datenanalyse: Wie man mithilfe der RFM-Analyse im Onlinehandel High-Value-Kunden identifiziert</h1>

Foto von Jay Chan auf Unsplash

In einem Einzelhandelsunternehmen tragen nicht alle Kunden gleichermaßen zum Umsatz des Geschäfts bei. Einige kaufen sehr häufig ein, andere seltener – aber wenn sie es tun, kaufen sie viel. Durch das Verständnis und die Segmentierung ihrer Kundschaft verschaffen sich Unternehmen einen strategischen Vorteil, der ihnen bei ihren Marketingkampagnen helfen kann.

<h2>Was ist eine RFM-Analyse?</h2>
Die RFM-Analyse steht für „Recency, Frequency, and Monetary Analysis“ – also für Aktualität, Häufigkeit und Geldwert. Sie dient dazu, Kunden basierend auf ihren letzten Transaktionen zu klassifizieren. Wie der Name schon sagt, berücksichtigt die Analyse drei Aspekte des Kaufverhaltens:
- Wie aktuell war der letzte Kauf des Kunden?
- Wie häufig hat dieser Kunde in einem bestimmten Zeitraum eingekauft?
- Und wie viel Geld hat der Kunde in diesem Zeitraum ausgegeben?
Um eine objektive Analyse zu ermöglichen, erhält jeder Kunde basierend auf diesen Variablen eine numerische Bewertung.
Je nach Größe des Datensatzes können verschiedene Werkzeuge zur Durchführung der RFM-Analyse verwendet werden. Bei kleinen Datensätzen reicht eine einfache Tabellenkalkulation aus. Bei großen Transaktionsdaten empfiehlt sich der Einsatz von BI-Tools (wie Power BI und Tableau) oder Programmiersprachen (wie Python und R). In meiner Analyse habe ich Python verwendet, insbesondere die Bibliothek pandas, bei einem mittelgroßen Online-Handelsunternehmen mit Hauptsitz im Vereinigten Königreich.
<h2>Durchführung der RFM-Analyse mit pandas</h2>
Die Analyse beginnt mit der Bereinigung der Transaktionsdaten und der Auswahl relevanter Merkmale. In meinem Datensatz sind die relevanten Merkmale: Rechnungsnummer, Rechnungsdatum, Kosten und Kunden-ID. Alle anderen Merkmale sind überflüssig, können jedoch im Modell verwendet werden, um die Ergebnisse zu visualisieren.
Pic rfm_1_1: Rechnungsnummer, Rechnungsdatum, und Kosten sind die relevante Merkmale für RFM-Analyse.
**Recency (Aktualität)**: Sie misst, wie kürzlich ein Kunde einen Kauf getätigt hat. Die Aktualität wird üblicherweise in Tagen geschätzt und ergibt sich aus der Differenz zwischen dem letzten Kaufdatum und dem aktuellen Datum für jeden Kunden. In pandas verwendet man die groupby()-Methode, um den Datensatz nach dem Merkmal „Kunden-ID“ zu gruppieren. Anschließend wird das Merkmal „Rechnungsdatum“ mit einer Lambda-Funktion aggregiert, wie hier gezeigt.
PIC
**Frequency (Häufigkeit)**: Sie zeigt, wie oft ein Kunde einen Kauf tätigt. In meinem Datensatz lässt sich die Häufigkeit eines Kunden ermitteln, indem man die Anzahl der Rechnungsnummern für jeden Kunden über den gesamten Datensatz hinweg zählt.
**Monetary (Geldwert)**: Sie misst, wie viel Geld ein Kunde insgesamt ausgegeben hat. Um den monetären Wert zu berechnen, summiert man die Variable „Kosten“, nachdem der Datensatz nach dem Merkmal „Kunden-ID“ gruppiert wurde.
**Kundensegmentierung**: Die berechneten RFM-Werte können schwer zu interpretieren sein und es ist nicht einfach, die besten Kunden zu identifizieren. Deshalb nutzen Unternehmen die RFM-Werte, um Cluster von Kunden mit ähnlichen Werte zu erkennen. Dies nennt man Kundensegmentierung. In pandas habe ich die Methode qcut() verwendet, um die RFM-Werte auf einer Skala von 1 bis 5 einzuteilen und zu kennzeichnen.
PIC
Anschließend habe ich die R-, F- und M-Werte jedes Kunden addiert, um einen endgültigen RFM-Score zu erhalten. Der maximale Score, den ein Kunde erreichen kann, beträgt 15 (also jeweils eine 5), und der minimale Score ist 3 (also jeweils eine 1). Schließlich habe ich eine neue Variable „Segment“ erstellt, die die Kunden basierend auf ihrem RFM-Score nach folgenden Kriterien einteilt:
- High-Value-Kunde: RFM-Score von 12 oder höher
- Medium-Value-Kunde: RFM-Score zwischen 9 und 12
- Low-Value-Kunde: RFM-Score zwischen 6 und 9
- Gefährdeter Kunde: RFM-Score unter 6
Das Endergebnis wird hier dargestellt.
PIC
Basierend auf der Kundensegmentierung starten Unternehmen gezielte Marketingkampagnen. Zum Beispiel können High-Value-Kunden mit Treuepunkten belohnt werden. Kunden mit hoher Aktualität und niedriger Häufigkeit sind nichts anderes als Neukunden und können gezielt angesprochen werden, um sie zu Stammkunden zu machen. Gefährdete Kunden können mit Rückgewinnungskampagnen angesprochen werden.

[back](./)
