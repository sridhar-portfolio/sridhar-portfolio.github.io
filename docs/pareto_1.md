---
layout: default
---

<img class="article-img" src="/assets/img/pareto_1_0.jpg" alt="Main Picture">
<p style="font-size: 10px; text-align: right; margin-top: 0px;">Foto von Austin Distel auf Unsplash</p>
<h1>Pareto trifft E-Commerce: Entlarvt die Datenanalyse den 80/20-Mythos?</h1>
Ursprünglich auf [LinkedIn](https://www.linkedin.com/pulse/pareto-trifft-e-commerce-entlarvt-die-datenanalyse-den-sridhar-sekar-vgg2e) veröffentlicht

Pareto-Analyse ist ein Entscheidungswerkzeug, das das Pareto-Prinzip, auch bekannt als 80/20-Regel, verwendet, um die wirkungsvollsten Faktoren in einem Unternehmen zu identifizieren und zu priorisieren. Das Prinzip besagt, dass 80 % der Ergebnisse aus 20 % der Ursachen stammen. Mit anderen Worten: In einem Online-Handelsunternehmen tragen nur 20 % der Kunden zu 80 % des Umsatzes bei. Diese Fallstudie ist ein Versuch, die Gültigkeit dieses Prinzips zu überprüfen.

Eine Pareto-Analyse beinhaltet in der Regel das Sammeln von Daten zu einem bestimmten Thema, wie z. B. Produktverkäufen, das Ranking von Kunden nach ihrem Beitrag zum Umsatz und schließlich die Visualisierung dieser Daten mithilfe eines Pareto-Diagramms. Hier werde ich die Python-Bibliothek Pandas verwenden – um die Transaktionsdaten aus dem Einzelhandel zu analysieren – und Matplotlib – um die Ergebnisse zu visualisieren.

Mein Datensatz enthält Transaktionsdaten eines mittelgroßen Online-Handelsunternehmens mit Hauptsitz im Vereinigten Königreich. Jeder Eintrag stellt eine Verkaufs­transaktion dar und enthält relevante Informationen wie Rechnungsdatum, Rechnungsnummer, Kunden-ID, Produktbeschreibung, Produktkategorie und so weiter. Die für unsere Analyse relevanten Felder sind die Kunden-ID und die Kosten.

![Dataset_sample](/assets/img/pareto_1_1.jpg)

<h2>So erstellt man eine Pareto-Analyse mit Pandas</h2>
Mit Pandas beginnt die Analyse damit, den Datensatz von Fehlern und Nullwerten zu bereinigen. Anschließend wird der Datensatz nach Kunden-ID gruppiert, und das Kostenfeld summiert, um ein neues DataFrame zu erstellen, das den Gesamtumsatz pro Kunde zeigt. Danach werden diesem neuen DataFrame drei berechnete Felder hinzugefügt – kumulierter Umsatz, kumulierter Umsatz in %, und Kundenanteil in %. Der Kundenanteil zeigt hier den kumulierten Anteil der Kunden an der Gesamtzahl der Kunden des Unternehmens.

![Python Code](/assets/img/pareto_1_2.jpg)

![Output Table](/assets/img/pareto_1_3.jpg)

<h2>Visualisierung mit Pareto-Diagramm</h2>
Ein Pareto-Liniendiagramm hilft dabei, die „wesentlichen wenigen“ Beitragsleister zu identifizieren, die für den Großteil der Wirkung verantwortlich sind. Hier habe ich Matplotlib verwendet, um das Ergebnis zu visualisieren, wobei der Kundenanteil auf der X-Achse und der kumulierte Umsatzanteil auf der Y-Achse dargestellt wird.

![Visualization Code](/assets/img/pareto_1_4.jpg)

![Pareto Diagram](/assets/img/pareto_1_5.png)

<h2>Interpretation der Ergebnisse</h2>
Die Analyse beweist eindeutig, dass das Pareto-Prinzip kein Mythos ist und im Online-Handel tatsächlich zutrifft. Mein Ergebnis zeigt, dass nahezu 20 % der Kunden für 80 % des Unternehmensumsatzes verantwortlich sind. Als letzter Schritt kann sich der Online-Händler auf die treuesten 20 % der Kunden konzentrieren – durch personalisierte Angebote, Treueprogramme und gezielte Kampagnen.

Als Erweiterung meiner Analyse gibt es weitere Bereiche im Einzelhandel, in denen die Pareto-Analyse ebenfalls eingesetzt werden kann, um verwertbare Erkenntnisse zu gewinnen. Einige davon sind nachfolgend aufgeführt.

1. Produktoptimierung
- Verwenden Sie diese Analyse als Vorlage, um die 20 % der meistverkauften Produkte zu identifizieren, die 80 % des Umsatzes generieren
- Priorisieren Sie Lagerbestand, Marketing und Aktionen für diese Artikel
- Reduzieren oder entfernen Sie schlecht laufende Produkte, um die Abläufe zu optimieren

2. Marketingeffizienz
- Analysieren Sie, welche 20 % der Kampagnen 80 % des Traffics bringen
- Weisen Sie Budget und Ressourcen leistungsstarken Kanälen zu (z. B. SEO, E-Mail)
- Kürzen Sie Maßnahmen mit geringer Wirkung, um den ROI zu verbessern

3. Verbesserung des Kundenservice
- Identifizieren Sie wiederkehrende Probleme aus Support-Tickets oder Bewertungen
- Gehen Sie die wichtigsten 20 % der Probleme an, die 80 % der Unzufriedenheit verursachen
- Verbessern Sie entsprechend die Produktqualität, Benutzererfahrung oder Erfüllungsprozesse

4. Lagerbestandsmanagement
- Verwenden Sie Pareto-Diagramme, um schnelllaufende vs. langsam laufende Artikel zu verfolgen
- Investieren Sie in größere Lagerbestände für stark nachgefragte Produkte
- Vermeiden Sie Überbestände bei schwach performenden Artikeln, um Verschwendung zu reduzieren


