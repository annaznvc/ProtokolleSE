
Install Scala
Install VS Code
Create a Scala Project using Giterate (g8)
	sbt new scala/scala3.g8

Generate the String output of a playing field on the Console


***********************************
Scala Projekt mit g8 erstellen:
***********************************

-
    cd C:\Users\annaz\Desktop\Projekt
    sbt new scala/scala3.g8
    name [Scala 3 Project Template]: maedn
    cd maedn
    code .


***************************************************
Im Terminal im Projektordner code ausführen
**************************************************

-

    cd C:\Users\annaz\Desktop\Projekt\maedn
    sbt run



-------------------------------------
Create a worksheet in your project
Create some basic data structures for your game in the worksheet
Access your data
Try to improve your implementation in small increments until your data and its access feel really good. Constantly test this.

In VS Code Worksheets have the ending worksheet.sc
------------------------------------

********************************
Worksheet ertsellen
****************************

Control + Shift + C in VS Code und Metals suchen, installieren
src > main > scala
neue Datei mit namen Name z.B: game.worksheet.sc

*****************************************
Basic data structures erstellen
*****************************************
Überlegungen:

Spieler hat…
-
- mehrere eindeutige Spielfiguren (4)
- Namen
- Spieler ID


Jede Spielfigur hat…
-
- mehrere Zustände (zu Hause, auf dem Brett, am Ziel) fest zugeordnet abhängig von Farbe
- Figur ID
- Position auf dem Feld (abhängig von x und y koordinaten)
- Farbe


Jedes Feld hat…
-
- eine Kategorie (Haus, Ziel, Brett)
- eine Position

Jede Position hat…
-
- x und y koordinaten



