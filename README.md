# Binder Badge
https://mybinder.org/v2/gh/eddide/Recomender-Systems/HEAD

# Dokumentation zur Ausführung
1. Aktivieren des Links zu Binder
2. Öffnen des Python-Notebooks "Installationen"
3. In der Toolbar unter "Kernel" "Restart & Run All" aktivieren. --> Bestätigen des Pop-up Fensters mit "Restart and Run All Cells"
4. Nach der erfolgreichen Ausführung Schließen des Python-Notenooks "Installationen"
5. Öffnen des Pyhton-Notebooks "Recommender Systems"
6. In der Toolbar unter "Kernel" "Restart & Run All" aktivieren. --> Bestätigen des Pop-up Fensters mit "Restart and Run All Cells"
7. Ergebnisse mit den unten beschriebenen Ergebnissen abgleichen

# Empfehlungssysteme
In diesem Notebook geht es daraum ein einfaches funktionierendes Empfehlungssystem zu erstellen, dass Items empfiehlt, die möglichst ähnlich zu einem bestimmten Item sind. In unserem Fall wird es sich um Filme handeln. Denkt aber bitte daran, dass dies kein ausgeklügeltes reales Empfehlungssystem ist; es sagt uns einfach nur, welche Filme sich in ihren Eigenschaften ähneln. Netflix und Co. beziehen das Nutzerverhalten und viel mehr Eigenschaften für ihre Empfehlungen.

## Anwendung
### Libraries Import
zuerst werden die relevanten Libraries importiert
- pandas
- numpy
- matplotlib
- seaborn
### Daten Import und Überprüfung
dann werden die Daten importiert und überprüft
- Anzeigen der Daten
- Information der Daten
- Beschreibung der Daten
## Datenvorbereitung
Gruppierung von Titeln und Ratings um die Anzahl an Bewertungen zum Data Frame hinzu zu fügen.
### Explorative Datenanalyse
Verwendung unterschiedlicher Visualisierungen um die Daten zu erforschen
- Histogramm
- Jointplot
## Anwenden der Empfehlung
- Erstellung einer Matrix mit den Bewertungen pro Nutzer pro Film
- Um eine Empfehlung anzuwenden werden nun Referenzfilme ausgewählt (hier: 2)
- Auf diese Filme wird über corrwith() die Korrelation zwischen den Filmen mit der Pandas Serie untersucht
- Im Anschluss werden die Null-Werte für die DataFrames mit den Korrelationen zum Film gelöscht
- Dann werden diejenigen Filme eliminiert, welche weniger als 100 Bewertungen haben
Anschließend erhält man eine Liste mit Filmen, welche am besten zu dem Referenzfilm passen.

## Ergebnisse
- bei dem Beispiel mit Star Wars hat ein weiterer Film aus der Reihe die höchste Korrelation (Empire Strikes Back 74%). Das spricht für die Vorhersagekraft des Modells
