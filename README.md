# Binder Badge
https://mybinder.org/v2/gh/eddide/mybinder_k-means/HEAD

# Dokumentation zur Ausführung
1. Aktivieren des Links zu Binder
2. Öffnen des Python-Notebooks "Installationen"
3. In der Toolbar unter "Kernel" "Restart & Run All" aktivieren. --> Bestätigen des Pop-up Fensters mit "Restart and Run All Cells"
4. Nach der erfolgreichen Ausführung Schließen des Python-Notenooks "Installationen"
5. Öffnen des Pyhton-Notebooks "K_Means Clustering"
6. In der Toolbar unter "Kernel" "Restart & Run All" aktivieren. --> Bestätigen des Pop-up Fensters mit "Restart and Run All Cells"
7. Ergebnisse mit den unten beschriebenen Ergebnissen abgleichen

# K Means Clustering

Für dieses Projekt werden wir versuchen K Means Clustering zu verwenden, um Universitäten in den USA in zwei Gruppen zu unterteilen: Private und öffentliche.

*Ein wichtiger Hinweis gleich zu beginn: Für diese Universitäten wissen wir die tatsächliche Zuordnung und finden sie im Datensatz. Wir werden sie aber ignorieren da K Means Clustering ein Unsupervised Learning Algorithmus ist.*

Normalerweise verwendet man den K Means Clustering Algorithmus für Daten, deren Zugehörigkeit zu einem Cluster man nicht kennt. In diesem Fall verwenden wir die Zuteilung, um beurteilen zu können, wie gut der Algorithmus performt. Da das in echten Anwendungen nicht möglich ist sind Confusion Matrix und Classification Report am Ende des Projekts nur theoretische Auswertungen.

## Die Daten

Wir verwenden einen DataFrame mit 770 Beobachtungen und den folgenden 18 Variablen:

* Private: Dummy Varaible mit "Yes" für private und "No" für öffentliche Einrichtungen
* Apps: Anzahl an erhaltenen Bewerbungen
* Accept: Anzahl an angenommenen Bewerbungen
* Enroll: Anzahl neu eingeschriebener Studenten
* Top10perc: Prozent der neuen Studenten der Top 10% einer High School Klasse
* Top25perc: Prozent der neuen Studenten der Top 25% einer High School Klasse
* F.Undergrad: Anzahl an Vollzeitstudenten
* P.Undergrad: Anzahl an Teilzeitstudenten
* Outstate: Gebühr für Studenten, die aus einem anderen Staat kommen
* Room.Board: Kosten für Räume und Mitarbeiter
* Books: Geschätze Kosten für Bücher
* Personal: Geschätzte persönliche Ausgaben
* PhD: Prozent der Fakultäten mit Ph.D.'s
* Terminal: Prozent der Fakultäten mit Terminal Degree
* S.F.Ratio: Rate der Studenten pro Fakultät
* perc.alumni: Prozent der Alumni die spenden
* Expend: Verwaltungskosten pro Student
* Grad.Rate: Abschlussrate

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
### Explorative Datenanalyse
Verwendung unterschiedlicher Visualisierungen um die Daten zu erforschen
- Scatterplot
- Histogramm
## Datenvorbereitung
Anpassung falscher Werte

## K Means Cluster erstellen
Anwendung des K Means Clustering
- Festlegung der zu erwartenden Cluster (hier: 2)
- fitten des Modells auf die Daten
### Evaluation der Vorhersage
Evaluierung über den classification report.
Es sollten ähnliche Ergebnisse wie diese angezeigt werden:
- accuracy: 22%
- reall: 65 und 6%
- f1-score: 31 und 10 %

Das Modell liegt mit 65% bei der vorhersage richtig, dass ein eine Universität öffentlich ist.
Bei der Vorhersage einer privaten Hochschule liegt das Modell nur zu 6% richtig und ist damit nicht gut geeignet.
