# Titanic Survival Prediction Using Machine Learning


Dieses Repo behandelt das Titanc-Dataset.
Im Großen und Ganzen finden sich fast überall im Script Beschreibungen, warum etwas umgesetzt wird. 
Daher gehe ich im Folgenden nur recht knapp auf die einzelnen Abschnitte ein.


## Importieren der Libraries

Für dieses Projekt sind Libraries vonnöten, welche die Manipulation der Daten gleichermaßen wie die Visualisierung dieser unterstützen. Daher wurden pandas, numpy, seaborn und matplotlib.pyplot ausgewählt. 

- **pandas** bietet Mittel zur Datenanalyse, -manipulation und -aufbereitung.
- **numpy** unterstützt die Datenanalyse und das maschinelle Lernen.
- **seaborn** ermöglicht die Datenvisualisierung und baut auf Matplotlib auf und arbeitet eng mit pandas zusammen.
- **matplotlib.pyplot** ist weit verbreitet bei der Erstellung von Diagrammen und ist essentiell wichtig, um die Daten und die daraus gewonnenen Einsichten optimal zu visualisieren.


## Laden der Daten

Hier werden die bereitgestellten CSV-Dateien geladen.


## Exploratory 

Data AnalysisDieser Abschnitt ist recht lang, da dort erstmal getestet wird, was die bereitgestellten Daten alles beinhalten und wie man diese in Beziehung setzen kann. Es wird getestet, wo möglicherweise NULLs vorliegen, die entfernt oder ersetzt werden müssen.


## Data Cleaning

Dort fallen ein paar der gegebenen Merkmale raus. Cabin hatte sehr viele NULL-Werte und es ließe sich zwar auch mit den wenigen Werten arbeiten, aber da ich dort nicht wie bei anderen einen sinnvollen Durchschnitt oder Modus bestimmen konnte, fällt das Merkmal lieber raus. PassengerId und Name fallen ebenfalls raus, da sie meines Erachtens nicht essentiell für die Überlebensprognose sind. Als Letztes fällt noch das Ticket weg. Es ließe sich zwar so umwandeln, dass es sich bestimmt verwenden lässt, aber in diesem Durchlauf wollte ich das erstmal überspringen.Des Weiteren wurden hier ein paar Merkmale, die NULL-Werte aufwiesen, durch Werte, die den Median oder Modus darstellen, aufgestockt, um trotzdem mit allen Spalten arbeiten zu können.


## Arbeit mit den Merkmalen

Hier wird nur kurz geguckt, zwischen welchen Merkmalen möglicherweise eine Korrelation bestehen könnte.Es werden zudem Merkmale, die beispielsweise durch Strings repräsentiert werden, in Zahlenwerte umgewandelt, damit die später verwendeten Modelle diese einwandfrei verwenden können.


## Testen anhand verschiedener Modelle

Es wird getestet, ob verschiedene Machine-Learning-Ansätze bessere Ergebnisse liefern. Das am Ende gewählte Modell erreichte eine Accuracy von 74.64%. Bei ungefähr einem Viertel der Passagiere wurde richtig vorhergesagt, ob diese bei dem Unglück ums Leben kommen oder nicht. Jedoch lässt sich die Accuracy bestimmt noch etwas weiter verbessern, was ich wann anders bestimmt nochmal versuchen werde.
