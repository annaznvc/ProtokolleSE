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
















