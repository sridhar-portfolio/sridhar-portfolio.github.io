---
layout: default
---

<img class="article-img" src="/assets/img/recency_1_0.jpg" alt="Main Picture">
<p style="font-size: 10px; text-align: right; margin-top: 0px;">Foto von <a href="https://unsplash.com/@kmitchhodge?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">K. Mitch Hodge</a> auf <a href="https://unsplash.com/photos/people-walking-on-pedestrian-lane-during-daytime-Fo2HDb1xsDE?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">Unsplash</a></p>
<h1>Kundenaktivität verstehen und nutzen – mit Power BI und Recency Heatmap</h1>
Juli 31, 2025

Im Bereich der Geschäftsanalytik misst die "Recency" (Aktualität), wie kürzlich ein Kunde einen Kauf getätigt hat. Sie spiegelt die Zeit wider, die seit der letzten Interaktion oder Transaktion des Kunden mit dem Unternehmen vergangen ist. Der zugrunde liegende Gedanke ist, dass Kunden, die kürzlich gekauft haben, eher auf zukünftige Aktionen reagieren oder sich erneut engagieren. Die Recency hilft dabei, aktive und inaktive Kunden zu identifizieren.

In einem Einzelhandelsunternehmen wird die Recency berechnet, indem das aktuelle Datum vom Datum des letzten Kaufs jedes Kunden subtrahiert wird. Diese Kennzahl wird in der Regel kontinuierlich überwacht, und ein niedriger Recency-Wert (d. h. weniger Tage seit dem letzten Kauf) weist auf eine kürzlich erfolgte Transaktion hin.

Eine Möglichkeit, die Recency zu visualisieren, ist über ein Histogramm. Es bietet einen Gesamtüberblick über die Verteilung der Kunden auf Basis ihrer Aktivitäten.

![Histogram_sample](/assets/img/recency_1_1.jpg)

Die wohl am häufigsten genutzte Visualisierung für Recency ist die Heatmap. Sie verwendet Farbverläufe, um Bereiche mit hoher und niedriger Intensität hervorzuheben. Die Verwendung von warmen Farben (z. B. Rot) und kühlen Farben (z. B. Blau) macht Heatmaps visuell ansprechend und leicht verständlich – auch für nicht-technische Zielgruppen. Sie eignen sich besonders gut für die Darstellung großer Datenmengen.

<h2>Bedeutung der Recency</h2>
**Kundenbindung**: Die Recency ist ein Indikator für die Kundenbindung. Sie dient als wertvoller Input für Machine-Learning-Modelle, die eine Abwanderung von Kunden vorhersagen. Im Vergleich zu anderen Kennzahlen in diesem Bereich ist die Recency der stärkste Prädiktor für zukünftiges Kundenverhalten. Sie hilft dabei, zwischen aktuell engagierten Kunden und potenziell abwandernden Kunden zu unterscheiden.

**Marketingkampagnen**: Unternehmen können Kunden anhand ihrer Recency-Werte segmentieren und ihnen kurz nach einem Kauf personalisierte Angebote senden, um die Kaufdynamik zu nutzen. Darüber hinaus hilft der Recency-Wert dabei, Ressourcen nicht an Kunden zu verschwenden, die voraussichtlich nicht reagieren werden. Auf diese Weise kann der Return on Investment (ROI) von Kampagnen maximiert werden.

<h2>Fallstudie: Online-Einzelhandelsunternehmen</h2>
Unser Datensatz enthält die Transaktionsdaten eines mittelgroßen Online-Einzelhandelsunternehmens mit Hauptsitz im Vereinigten Königreich. Jeder Eintrag stellt eine Produktverkaufs-Transaktion dar, mit relevanten Informationen wie Rechnungsdatum, Rechnungsnummer, Kunden-ID, Produktbeschreibung, Produktkategorie und weiteren Details. Für unsere Analyse sind die relevanten Felder: Rechnungsdatum, Land und Unterkategorie.

![Dataset sample](/assets/img/recency_1_2.jpg)

**Berechnung der Recency**: In Power BI ist die Berechnung der Recency unkompliziert. Man erstellt eine Measure, die die Differenz zwischen dem aktuellen Datum und dem letzten Kaufdatum berechnet. In der Regel wird die Recency in Tagen gemessen. Da unser Datensatz jedoch täglich tausende Transaktionen umfasst, liefert eine Messung in Stunden oder Minuten tiefere Einblicke.

```dax
RecencyDays = 
VAR ref_date = DATE(2011,12,10) + TIME(0,0,0)
RETURN
DATEDIFF(MAX(Online_Retail_New[InvoiceDate]), ref_date, DAY)
```

**Heatmaps in Power BI**: Ich habe zwei Heatmaps erstellt – eine zur Visualisierung der Recency über verschiedene Länder hinweg, und eine weitere über die einzelnen Produktunterkategorien.

![Heatmap Product Subcategory](/assets/img/recency_1_3.jpg)

Recency-Heatmap der Produktunterkategorien

![Heatmap Country](/assets/img/recency_1_4.jpg)

Recency-Heatmap der Verkäufe in verschiedenen Ländern

In unserem Einzelhandelsgeschäft verkaufen sich Produkte aus den Kategorien Gartenmöbel und Handwerkzeuge am wenigsten. Ebenso weisen die Länder Litauen, Libanon und Saudi-Arabien die höchsten Recency-Werte auf. Das Unternehmen kann geeignete Maßnahmen im Bereich Lagerbestand oder Marketing ergreifen, um die Recency-Werte zu senken.

_[Ursprünglich auf [LinkedIn](https://www.linkedin.com/pulse/kundenaktivit%C3%A4t-verstehen-und-nutzen-mit-power-bi-recency-sekar-kzx8e) veröffentlicht]_
