# CS 1 Task 2: SE Process

## Plan-driven

### Pros
* Wir vermeiden unnötige Kundeninteraktionen (Lange Sitzungen, etc.)
* Wir haben klare Zielvorgaben mit fixen Projektphasen
* Gewichtung auf Spezifikationen und Anforderungen zu Beginn
* Eine genaue Kostenabschätzung kann abgegeben werden

### Cons
* Wenig und späte Kundeninteraktion/Feedback
* Schwierig und umständlich auf Changes zu reagieren (Träge)
* Späte Änderungen sind teuer
* Hoher Aufwand für das Requirements Engineering

## Agile

### Pros
* Nachträgliche Änderungen und Anforderungen sind einfacher umzusetzen
* Konzeptionsphase zu Beginn kurz, man ist schneller in der Umsetzung (Entwicklung)
* Schnelle Ergebnisse für den Kunden sichtbar
* Laufendes Feedback durch den Kunden
* Unserer Code wird bei jedem Commit kontinuierlich getestet (Continuous integration)
* Laufendes Deployment für den Kunden

### Cons
* Unnötige Komplexität bei vielen Änderungen
* Unsere Ressourcen können schneller ausser Kontrolle geraten (Zeit und Kosten)
* Mehr Aufwand für den Kunden, Ressourcen müssen immer bereitstehen

## Decision

Startphase: Plan-driven, danach Übergang in die Agile Entwicklung

## Process Model Decision

Wir haben uns entschieden eine Mischform der beiden Prozessmodelle (Plan-Driven, Incremental) zu verwenden.
Aufgrund unseres eher geringen Wissens im Bereich des Spitalwesens, ist es für uns wichtig, bereits im Voraus einen Plan zu erstellen und die Bedürfnisse detailiert zu erfassen, damit wir nicht in eine komplett falsche Richtung starten.
Dies ist mit dem Plan-Driven Ansatz optimal umsetzbar.

Andererseits wollen wir uns nicht die Möglichkeit nehmen, während dem Implementationsprozess auf weitere Kundenwünsche einzugehen und diese flexibel umzusetzen.
Mit einem inkrementellen und agilen Ansatz ist dies bereits im Prozess integriert.

Aus dem Plan-Driven Modell wollen wir folgende Aspekte verwenden:

* Voranalyse des Projekts
* Requirements mit den Kunden aufnehmen
* Gesamtplanung des Projekt

Aus dem Inkrementellen und Agilen Modell wollen wir die folgende Aspekte verwenden:

* Regelmässigen Kontakt mit den Kunden (Reviews)
* Dynamische auf Kundenwünsche reagieren
* Code wird laufend gerefactored
* Funktionsfähige Zwischenreleases können dem Kunden zeitnah verteilt werden (User Acceptance)

### Vorgaben während der Entwicklung

* Jeder muss seinen Stand am Ende des Tages committen / Jeder Commit buildet und ist getestet
* Jeder Check-in ist ein potentieller Release Jeder Check-in löst auf dem CI-Server einen Build aus, welcher Unit- und Integrations-Tests beinhaltet. Bei jedem grünen Build entsteht ein Release Kandidat, der potentiell in die Produktion gelangen kann. 
* Kein Check-in auf einem roten Build! Wenn nach einem Check-in der Build fehlschlägt, so ist dies umgehend zu korrigieren. Ein grüner Build ist oberste Priorität.
* Vor einem Check-in alle Tests (Unit/Integration) ausführen Bevor ein Check-in gemacht wird, müssen alle Unit- und Integration-Tests lokal ausgeführt werden. 
* Defect Driven Testing: Zu jedem Bug sind geeignete Unit- und Integrationstests zu erstellen (automatisierte Regressionstests). 
* Code Reviews: 4 Augen Prinzip. Mögliche Ansätze: Pull Requests, Pair Programming 
* Test Driven Development (TDD) Vor der Implementierung des eigentlichen Features werden Unit- und Integration-Tests für dieses Feature erstellt. Das ist die einzig erfolgreiche Strategie, um eine hohe Testabdeckung zu erreichen. 
* Kleine Check-ins (baby steps) Check-ins sollten so klein wie möglich sein. Falls ein Feature nicht abgeschlossen werden kann, so ist dies auf einem Branch zu entwickeln.
* Verantwortung für die eigenen Changes übernehmen. Wenn andere Tests aufgrund einer eigenen Code-änderung fehlschlagen, so liegt es in der eigenen Verantwortung, diese Tests anzupassen. 
* Keine Tests auskommentieren Tests, die fehlschlagen sollten nicht auskommentiert oder ignoriert werden. 

## Taskliste

### Aktivität_00_Voranalyse

| Aufgabe Nr. | Aufgabe                            | Ziel    | Potentieller Output  |
| -------- | -------------------------------------- | --------- | ------------ |
| 01       |  Umgebung des Kunden analyisieren | Informationsbeschaffung für Gesamtplanung      | Machbarkeitsstudie          |
| 02       |  Vorbesprechung mit Kunden  | Momentane Bedürfnisse erkennen      | Aktuelle Stimmung und Probleme dokumentieren         |
| 03       |  Daily Business Analyse | Aktuelle Arbeitsweise festhalten | Bestehende Prozesse und Software kennen |
| 04       |  Terminwünsche aufnehmen | Gemeinsame Terminvorstellungen | Terminwünsche |

### Aktivität_01_Requirements Engineering

| Aufgabe Nr. | Aufgabe                            | Ziel    | Potentieller Output  |
| -------- | -------------------------------------- | --------- | ------------ |
| 01       |  Bedürfnisse mit dem Kunden identifizieren | Bedürfnisse kennen      | Liste der Bedürfnisse          |
| 02       |  Priorisierung der Bedürfnisse  | Wichtigkeit der Bedürfnisse kennen     | Priorisierte Liste der Bedürfnisse       |
| 03       |  Voranalyse einfliessen lassen | Machbarkeit bekannt | Machbarkeitsstudie kompletiert |
| 04       |  Grafische Oberfläche skizzieren und besprechen | Kunde und Entwickler haben eine Vorstellung der Oberfläche | Mock-Ups |

### Aktivität_02_Gesamtplanung des Projekts

| Aufgabe Nr. | Aufgabe                            | Ziel    | Potentieller Output  |
| -------- | -------------------------------------- | --------- | ------------ |
| 01       |  Projektrahmen definieren | Grobplanung bekannt  | Grobplanung          |
| 02       |  Kompetenzregelung | Jeder kennt seine Aufgaben und Verantwortungen | Kompetenzliste |
| 03       |  Hürden identifizieren  | Kritische Faktoren und Risiken bekannt     | Risikoanalyse       |
| 04       |  Detailplanung | Meilensteine festlegen | Detailplanung |
| 05       |  Requirements in Tasks umformulieren | Aufgaben für Projektmitarbeiter bekannt | priorisierte Taskliste |
| 06       |  Design der Applikation definieren | Implementationsgrundlage schaffen | UML/ERD-Diagramme |

### Iterative Aktivitäten

Diese Tasks wiederholen regelmässig (Sprints), jeden Tag wird ein Meeting
durchgeführt, an dem über den aktuellen Stand und Probleme gesprochen wird.

| Aufgabe Nr. | Aufgabe                            | Ziel    | Potentieller Output  |
| -------- | -------------------------------------- | --------- | ------------ |
| 01       |  Tasks in Stories umformulieren und einplanen | definierte Stories mit Abnahmekriterien  | Sprintplanung          |
| 02       |  Entwickler zerlegt Stories in kleine Tasks | Projektmitarbeiter kennt seine Aufgaben | Taskliste für Projektmitarbeiter  |
| 03       |  Entwicklung | Software entwickeln/Unit Tests schreiben| getestete Software |
| 04       |  Dokumentieren | Software ist stets aktuell dokumentiert | dokumentierte Software |
| 05       |  Review durch Team | Software ist durch 4 Augen-Prinzip validiert | stabile Software |
| 06       |  Review durch Kunde| Kunde sieht und kommentiert Produkt, allfällige Verbesserungen und Wünsche werden aufgenommen | Feedback durch Kunde |
| 07       |  Retrospektive | Team analysiert eigene Leistung und verbessert sich kontinuierlich | Leistung des Teams wird kontinuierlich besser |
