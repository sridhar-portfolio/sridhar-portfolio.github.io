---
layout: default
---

<img class="article-img" src="/assets/img/basket_1_0.jpg" alt="Main Picture">
<p style="font-size: 10px; text-align: right; margin-top: 0px;">Foto von <a href="https://unsplash.com/@karsten116?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">Karsten Winegeart</a> auf <a href="https://unsplash.com/photos/a-person-pushing-a-shopping-cart-full-of-food-CZtK_E89omo?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">Unsplash</a></p>
<h1>Warenkorbanalyse im E-Commerce: Was Ihre Kunden wirklich zusammen kaufen</h1>
August 08, 2025

Warenkorbanalyse ist eine leistungsstarke Data-Mining-Technik, die die Kombinationen von Produkten untersucht, die von einem Kunden gemeinsam gekauft werden. Ziel der Analyse ist es, das Kaufverhalten der Kunden zu verstehen. Sie beantwortet die Frage: „Wenn ein Kunde Produkt A kauft, wie hoch ist die Wahrscheinlichkeit, dass er auch Produkt B kauft?“

Die Analyse identifiziert Zusammenhänge zwischen Artikeln in einer Transaktion anhand von drei Hauptkennzahlen: Support, Confidence und Lift.

1. Support – Häufigkeit, mit der beide Produkte gemeinsam in allen Transaktionen gekauft werden
2. Confidence – Wahrscheinlichkeit, dass Produkt B gekauft wird, wenn Produkt A gekauft wurde
3. Lift – Im Vergleich zum Zufall: Wie viel wahrscheinlicher wird Produkt B zusammen mit A gekauft (Lift > 1 = starke Zusammenhang)

<h2>Wie man eine Warenkorbanalyse mit Pandas durchführt</h2>
In meiner Analyse habe ich die Python-Bibliotheken pandas, mlxtend und matplotlib auf Transaktionsdaten eines mittelgroßen Online-Handelsunternehmens verwendet. Jeder Eintrag im Datensatz stellt eine Produkttransaktion dar und enthält relevante Informationen wie Rechnungsdatum, Rechnungsnummer, Kunden-ID, Produktbeschreibung, Produktkategorie und so weiter. Die relevanten Felder für die Warenkorbanalyse sind Rechnungsnummer, Produktbeschreibung und Menge.

![Dataset Sample](/assets/img/basket_1_1.jpg)

Mit der Methode groupby() in Pandas habe ich eine Matrix aus True und False erstellt. Jede Zeile in dieser Tabelle steht für eine Rechnungsnummer, jede Spalte für eine Produktbeschreibung. Der Grund für die Erstellung einer solchen Tabelle ist, dass die Funktion apriori() aus der mlxtend-Bibliothek eine Matrix als Eingabe benötigt. Das Ergebnis der apriori()-Funktion ist eine Tabelle, die die Stärke der Assoziation zwischen verschiedenen Produkten zeigt.

![Calculating lift](/assets/img/basket_1_2.jpg)

Die „Antecedents“ sind Produkt A, und die „Consequents“ sind Produkt B. Wenn ein Kunde ein Produkt aus den Antecedents kauft, besteht eine hohe Wahrscheinlichkeit, dass er auch das zugehörige Produkt aus den Consequents kauft. Die Stärke dieser Assoziation wird durch den Lift dargestellt. Wenn der Lift größer als 1 ist, besteht die Verbindung zwischen den Produkten nicht zufällig; je höher der Lift, desto stärker die Assoziation.

![Scatter plot](/assets/img/basket_1_3.jpg)

Das Streudiagramm zeigt die Beziehung zwischen Confidence und Lift bei verschiedenen Produktkategorien. Es zeigt sich, dass der Zusammenhang bei Produkten aus den Kategorien Küche und Garten stark ist, während sie bei Artikeln aus der Kategorie Mode & Bekleidung schwach ausgeprägt ist.

<h2>Bedeutung der Warenkorbanalyse</h2>
Unternehmen nutzen die Warenkorbanalyse für verschiedene Zwecke. Sie entwickeln gezielte Marketingstrategien, wie z. B. das Platzieren verwandter Artikel nebeneinander im Geschäft. Durch das Verständnis darüber, welche Artikel häufig gemeinsam gekauft werden, können sie sicherstellen, dass diese Produkte ausreichend im Lager verfügbar sind.

Darüber hinaus können Unternehmen gebündelte Aktionen oder Rabatte für Artikel anbieten, die oft zusammen gekauft werden. Sie können auch personalisierte Empfehlungen aussprechen, etwa durch die Funktion „Kunden kauften auch …“.

_[Ursprünglich auf [LinkedIn](https://www.linkedin.com/pulse/kundenaktivit%C3%A4t-verstehen-und-nutzen-mit-power-bi-recency-sekar-kzx8e) veröffentlicht]_
