---
title: "Elektronische Prüfungen in der Informatik"
subtitle: "Ein Pilotversuch"
keywords: "elearning, ilias, elektronische prüfung, informatik, erfahrungsbericht"
---




# Ausgangssituation: Typisches Prüfungsszenario in der Informatik


## Klausuren in Programmierfächern

![Verteilung von Aufgabentypen in Programmierklausuren](figs/verteilung_typen)\

::: notes
Mix aus Aufgabentypen, darunter Multiple-Choice-Fragen, Code-Analysen, Lückentexte, Freitextaufgaben (Erklärungen, Programmieraufgaben) ...
:::


## Programmieren auf Papier ist praxisfremd

-   Keine Unterstützung durch IDE, Compiler/Interpreter und andere Tools
    ![Screenshot IDE](figs/screenshot_ide){width="62%"}\

    ::: notes
    -   keine generierten Rahmen (Importe, ...)
    -   kein Auto-Completion
    -   kein Syntax-Highlighting
    -   kein Refactoring
    -   kein Auto-Format
    -   keine Versionierung
    -   kein ...
    :::

\smallskip

-   Keine Hilfe aus dem Netz (Dokumentation, API, [Stack Overflow](https://stackoverflow.com), ...)


## Korrektur der Lösungen ist sehr aufwändig

-   Handschrift (!) [\blueArrow teilweise kaum noch lesbare Arbeitsblätter]{.notes}

-   Syntaxfehler: Grenze zw. noch akzeptabel und fehlerhaft

-   Oft "kreative" Lösungsansätze: Manuelles Nachprüfen am Rechner ...

\vfill

\blueArrow Typisch ca. 50..80 Teilnehmer mit ca. 15 Seiten pro Klausur




# Pilotversuch: Elektronische Prüfungen mit ILIAS


## Vorbereitung: Fragetypen im ILIAS

![Screenshot ILIAS: Fragetypen](figs/screenshot_iliasfragetypen)\
[Quelle: [docu.ilias.de](https://docu.ilias.de/ilias.php?ref_id=6024&obj_id=91118&cmd=layout&cmdClass=illmpresentationgui&cmdNode=2h&baseClass=ilLMPresentationGUI) (Zugriff 04.11.2019)]{.origin}


## Vorbereitung: Übertragen der Aufgaben

![Screenshot ILIAS: Bearbeitung einer Lückentextfrage](figs/screenshot_ilias_combined)\


::: notes
### Vorgehen

*   Papierklausur zunächst 1:1 in ILIAS übertragen
*   Mapping auf die ILIAS-Fragetypen [@ilias-tests]:
    -   MC-Fragen
    -   Lückentext-Aufgaben
    -   Freitext-Aufgaben
*   Problem: Ursprüngliche Frage mit mehreren Teilen (oder Fragetypen) \blueArrow Aufsplitten in einzelne ILIAS-Fragen

**Zusätzlich wurde im Vorfeld den Teilnehmern eine Demo mit ausgewählten Fragetypen zur Verfügung gestellt.**


### Erfahrung im Pilotversuch

Für die Erstellung der Klausur im ILIAS muss man ausreichend Zeit einplanen, selbst wenn man vorhandene Papierklausuren
direkt überträgt.

Die von ILIAS bereitgestellten Editoren sind teilweise stark gewöhnungsbedürftig und nur umständlich zu bedienen. Es lohnt
sich, im Vorfeld die vielfältigen von ILIAS angebotenen Fragetypen auf ihre Eignung zu prüfen.

Im Pilotversuch hat der Editor für Lückentextaufgaben wiederholt Probleme bereitet: Beim erneuten Editieren einer Aufgabe
geriet teilweise die intern genutzte HTML-Formatierung komplett durcheinander, was dann manuell in der HTML-Ansicht repariert
werden musste.

Außerdem kann je Frage immer nur ein Fragetyp abgebildet werden. Wenn in der ursprünglichen Klausur eine Frage aus mehreren
Abschnitten bzw. Teilfragen bestand, musste dies im ILIAS durch mehrere einzelne Fragen realisiert werden.

Zudem muss man immer die Monitorauflösungen im Prüfungsraum berücksichtigen. Anderenfalls kann dies dazu führen, dass
die Teilnehmer bei jeder Frage viel hin und her scrollen müssen und beispielsweise nur die Frage oder nur den Antwortbereich
auf einmal sehen können.
:::


## Durchführung der E-Klausur

*   Fragetypen-Demo für Teilnehmer (im Vorfeld)

\smallskip

*   Teilnehmer in speziellen ILIAS-Kurs eintragen
*   Test online schalten, wenn alle eingeloggt
*   Bearbeitungszeit lässt sich auf Server begrenzen

\bigskip

*   Ergebnis:
    -   Ausdrucken der (teilautomatisch bewerteten) Klausur (PDF) plus Deckblatt
    -   Teilnehmer unterschreiben ihre Klausur


## Korrektur und Bewertung

:::notes
ILIAS kann bei bestimmten Aufgabentypen die Antworten der Teilnehmer mit den hinterlegten
Lösungen abgleichen und somit die Klausuren zum Teil automatisiert korrigieren:
:::

:::::: columns
::: {.column width="40%"}
\vspace{10mm}

*   MC vollautomatisch

\bigskip

*   Lückentexte: teilautomatisch

    ::: notes
    Leider wird die Antwort der Teilnehmer 1:1 mit der vorgegeben Lösung gematcht.
    Man kann durch Vorgabe mehrerer alternativer Lösungen in gewissem Maße auf
    Lösungsvarianten reagieren, allerdings lassen sich so nicht alle Tippfehler etc.
    vorhersehen!

    Im Prinzip kann man auch mit der Levenshtein-Distanz arbeiten, aber selbst mit
    einer Distanz von 1 kann es passieren, dass somit auch ungültige Lösungen vom
    System akzeptiert würden.

    Im Prinzip müsste man hier mit **regulären Ausdrücken** arbeiten können!
    :::

\bigskip

*   Freitext: [manuelle Korrektur]{.alert}
:::
::: {.column width="50%"}
![Beispiel für halbautomatisch korrigierte Lückentextaufgabe](figs/screenshot_automatischekorrektur)\
:::
::::::

\vfill

\blueArrow Korrektur auf Ausdruck oder im ILIAS [(dann erneuter Ausdruck nötig für Archivierung im Prüfungsamt)]{.notes}


::: notes
### Erfahrung im Pilotversuch

Im Prinzip könnte man alle Klausuren direkt im ILIAS korrigieren, d.h. die vom System nicht bewerteten Aufgaben
manuell prüfen und bewerten. Neben den Punkten lässt sich auch eine Art kurzes Feedback hinterlegen. Bei einigen
automatisch korrigierten Aufgabentypen (etwa Lückentexten) kann man die automatisierte Bewertung noch manuell
überschreiben.

Im Anschluss würde allerdings ein neuer Ausdruck pro Teilnehmer notwendig, um die Archivierbarkeit im Prüfungsamt
zu gewährleisten. Das bedeutet typischerweise ca. 15 Seiten pro Teilnehmer bei typisch ca. 50 (und bis zu 80) Teilnehmern,
wobei durch die ungünstige Formatierung der generierten PDFs eher 20 bis 25 Seiten pro Teilnehmer zu erwarten sind ...

In der Praxis hat sich bisher bewährt, auf dem von den Teilnehmern unterschriebenen automatisch vorkorrigierten
Ausdrucken zu arbeiten. Man spart einen weiteren Ausdruck und kann ohne Probleme alle automatischen Korrekturen
manuell überschreiben (im Wortsinn).

Der Großteil der bisher verwendeten Aufgaben lässt eine automatische Bewertung durch ILIAS nicht (Freitext-Aufgaben)
oder nur eingeschränkt (Lückentext-Aufgaben) zu. Dennoch ist bereits die teilweise Bewertung durch ILIAS eine große
Unterstützung. Zusätzlich entfällt die Problematik der häufig nur schwer entzifferbaren Handschriften, was einen
weiteren deutlich spürbaren Zeitvorteil erbringt!

Die durch ILIAS generierten PDFs können selbst im besten Fall nur als suboptimal bezeichnet werden und enthalten sehr
viel "White Space", d.h. benötigen durch viel leeren Platz deutlich mehr Blatt Papier als die ursprüngliche Papierklausur ...
:::




# Zukunft: Konzeptskizze


## Konzept für Prüfungsumgebung für die Informatik

\bigskip

![Konzept für Prüfungsumgebung für die Informatik](figs/exam-net)\

::: notes
Diese Skizze für ein typisches Prüfungsszenario in der Informatik entstand im Sommersemester 2019 in der Diskussion mit
BC George und Lutz Westhäusser.

Dabei wird berücksichtigt, dass für praxisnahe Programmieraufgaben die Möglichkeiten von ILIAS nicht ausreichen. Außerdem
wird sehr viel Wert darauf gelegt, mögliche Täuschungsversuche weitestgehend zu vermeiden, beispielsweise indem die Teilnehmer
"frische" Accounts in der Prüfung zugeteilt bekommen.

Ebenso werden die Erfahrungen aus [@Dietz2018] berücksichtigt.

Bis auf den ILIAS-Anteil entspricht das vorgestellte System dem aktuellen Stand der Technik in der Softwareentwicklung,
so daß die Studierenden durch den Umgang mit diesem System quasi nebenbei aktuelle Techniken kennenlernen und einsetzen
lernen.


### Überblick

-   Alle Aufgaben der Prüfung werden im ILIAS gestellt

-   Bearbeitung der Aufgaben:
    -   Teilweise direkt im ILIAS (MC, Lückentext, Zuordnung)
    -   Teilweise als Programmieraufgabe

-   Programmieraufgaben:
    -   Bereitstellung von Vorgaben über ein VCS (*Version Control System*, etwa Gitlab)
    -   Bearbeitung mit üblichen Tools: IDEs (Eclipse, IntelliJ, Netbeans, VS Code, ...), Compiler/Interpreter, Bibliotheken (je nach Vorlesung)
    -   Abgabe per Upload ins ILIAS und VCS
-   Automatisierte Bewertung der Programmieraufgaben über eine CI/CD-Umgebung im Gitlab: Tests, Metriken, ...
-   Rückspielen der Bewertung ins ILIAS
-   Restliche Bewertung normal im ILIAS

-   Separate Benutzerverwaltung: Jeder Prüfling bekommt am Prüfungstag einen User+PWD zugewiesen (mit Zugriff auf Client, ILIAS und VCS)
-   Zugriff auf weitere (je Prüfung fest definierte) Internet-Ressourcen

-   Import der Aufgaben ins ILIAS aus strukturierten Dateien als Fernziel (der ILIAS-eigene Editor ist leider in der Benutzung eher umständlich und teilweise auch kaputt)
-   Export der Klausuren plus Bewertung als PDF: Funktioniert jetzt schon, aber das PDF ist ziemlich unsauber aufgebaut und enthält extrem viel "White Space"


### Erfahrung im Pilotversuch

Wir haben im Sommersemester 2019 das Szenario in der Virtualisierung im Studiengang Informatik partiell aufgebaut (grauer Kasten).
Dabei konnten die schwarz markierten Teile bereits realisiert werden, insbesondere wurden den Teilnehmern zu Beginn der Prüfung
anonyme, nur für diesen Zweck generierte Einmal-Benutzernamen plus -Passwörter zugeordnet, mit denen sie auf die Prüfungsumgebung
zugreifen konnten. Dort hatten sie Zugriff auf ausgewählte Internetressourcen (beispielsweise ILIAS). Darüber hinaus wurden
verschiedene verbreitete Programmierumgebungen (IDE) bereitgestellt sowie die in der jeweiligen Lehrveranstaltung benötigten Tools
(Compiler/Interpreter, Tests, Metriken, ...).

Der Aufbau wurde testweise in verschiedenen Praktika eingesetzt, wodurch wertvolle Erfahrungen bzgl. Lastausgleich, Verfügbarkeit,
Konfiguration etc. gesammelt werden konnten.

Die rot markierten Teile müssen noch schrittweise aufgebaut werden. Dazu müssen Personal- und ggf. Hardwaremittel eingeworben werden.


### Nötige Erweiterungen

Die folgenden Erweiterungen sind im obigen Konzept essentiell, um Programmieraufgaben und Lückentextaufgaben automatisiert
bewerten zu können.

#### Auslesen über API, externe Tools zur Bewertung

-   Reguläre Ausdrücke bei Lückentextaufgaben

    Bei Lückentexten würden reguläre Ausdrücke als Lösungsvorgabe das Problem mit den unterschiedlichen
    Schreibweisen und zulässigen Varianten einer Lösung die aktuelle Situation deutlich verbessern.
    Sofern die Auswertung nicht in ILIAS selbst realisierbar ist, könnte man darüber nachdenken, die
    Antworten der Teilnehmer sowie die vorgegebenen regulären Ausdrücke per API auszulesen, extern zu
    matchen und die resultierende Bewertung wieder über die API zurückzuschreiben.


-   Tests und Metriken für Freitextaufgaben (Programmieraufgaben)

    Dito bei Programmieraufgaben (Freitext): Hier könnten die Antworten der Teilnehmer über die API
    ausgelesen werden, extern durch geeignete Tools (Compiler, Test, Metriken, ...) bewertet werden
    und diese Bewertung samt ggf. Fehlerhinweisen (etwa Ausgabe der Testfälle) wieder über die API zurück
    geschrieben werden.


### Weitere wichtige Erweiterungen

Die folgenden Erweiterungen basieren auf den bisherigen Erfahrungen mit der Durchführung von Prüfungen mit ILIAS und
sollen die wichtigsten Schwachstellen adressieren.

#### Import von Aufgaben

Wenn man bisher Klausuren beispielsweise mit TeX erstellt hat, liegen die Aufgaben bereits in einem
gewissen strukturierten Format vor. Mit Hilfe eines noch zu erstellenden Import-Tools könnten diese
Beschreibungen über die API teilautomatisiert in ILIAS importiert werden.

#### Verbesserung PDF-Export

Derzeit kann man die Antworten der Teilnehmer mit und ohne automatische Korrektur als PDF
exportieren. Dabei wird allerdings sehr viel Platz verschwendet und große Teile einer Seite
bleiben dabei leider leer. Mit einem eigenen PDF-Exporter könnte man hier deutlich effizienter
arbeiten.

#### Elektronische Signaturen

-   Unterschrift Prüfling (Signieren der elektronischen Klausur im System)
-   Korrektur im ILIAS und Unterschrift Prüfer (Signieren der elektronischen Klausur im System)
-   Zentrale Archivierung der elektronischen Klausuren


### Sonstiges: Arbeiten mit Fragepools

Varianten:

-   themenbasiert
-   fragenbasiert

ILIAS erlaubt bei der Erstellung eines Tests (== Klausur), diesen aus mehreren Fragepools
zu speisen. Dabei kann man beispielsweise definieren, wie viele Fragen bzw. Punkte aus einem
Pool in den Test übernommen werden sollen. Dies kann für alle Teilnehmer einheitlich geschehen,
d.h. jeder Teilnehmer erhält die gleiche Klausur, oder sogar pro Test/Teilnehmer individuell, d.h.
jeder Teilnehmer erhält einen zufällig zusammengestellten Test nach den oben erwähnten Kriterien.

Damit könnte man themenbasierte Fragepools anlegen und in einem Test zufällig aus jedem
Themenpool einen bestimmten Anteil an Fragen zusammenstellen lassen.

Alternativ könnte man je ursprünglicher Frage (aus der Papierklausur) einen Fragepool anlegen mit
leichten Variationen derselben Frage und für jede individuelle Klausur dann zufällig eine Frage aus
jedem Pool ziehen (lassen). So erhält jeder Teilnehmer eine leichte Variation derselben Klausur
\blueArrow Vermeidung von "Abschreiben" bei gleichzeitig äquivalentem Schwierigkeitsgrad (dito Anzahl
und Inhalt der Aufgaben) ...
:::




::: slides
# Vielen Dank! Fragen?
:::




::: notes
# Bibliographie
<div id="refs" class="references">
<!-- XXX Platzhalter für Literaturliste (References/Bibliography) -->
</div>
:::
