# Protokoll 3

## Aufgabenstellung

- Take the Classes from your domain model
- Start developing them in Scala
- Use Behaviour Driven Development
- Use ScalaTest
- Write a Spec using WordSpec 
- Use the IDEA ScalaTest Runner 
- Achieve 100% code coverage. And maintain it! 


### Grundbegriffe
- domain model = Das Thema/Spiel, das man als Klassen im Code abbildet (z.B die Klassen Figuren, Spieler etc. nennt man zusammen Domain Model)

- behaviour driven development = man beschreibt, was passieren soll, man schreibt einen Test und programmiert solange, bis der Test grün wird

- Spec = Dokument mit Tests

- WordSpec = Stil, wie man Tests schreiben kann

- 100% Code Coverage = Jede Zeile Code wurde mindestens einmal getestet


------------
## Domain Model

- Abstrakte Oberklasse: Feld
    - Unterklassen:
        - StartFeld
        - NormalesFeld
        - ZielFeld
        - HeimatFeld


- Spieler
    - ID
    - Name
    - Farbe
    - 4 Figuren
    - Zugriff auf eigene Heimat und Zielfelder


- Figur
    - ID (1-4)
    - Farbe
    - Zustand (zu Hause, auf dem Brett, im Ziel)


- Spielbrett
    - enthält alle Felder
    - methoden

- Spielzustand
    - Spieler
    - Spielbrett
    - Wer ist dran?
    - wie war der letzte Wurf?
    - ist das Spiel vorbei?




Vorgehen:


Diese Zeilen in die BuildFIle einfügen

libraryDependencies += "org.scalactic" %% "scalactic" % "3.2.14",
libraryDependencies += "org.scalatest" %% "scalatest" % "3.2.14" % Test




1) Klassen schreiben ohne Methoden, nur die Daten
2) "Was soll mein Code können?" z.b ein spieler hat genau 4 figuren, ein heimatfeld darf nur von eigener farbe betreten werden, eine figur startet im Heimatfeld etc in Worten aufscchreiben
3) WordSpec-Test schreiben = Datei erstellen in src/test/Scala, man muss scalatest + wordspec wie in der VL benutzen
4) Methoden oder Datenkonstruktor so schreiben, dass er vom Test gebraucht wird
5) Test mit IDEA ScalaTest Runner starten
6) für jedes Verhalten wiederholen
7) Scoverage installieren?










