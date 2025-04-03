Create a project on Github
Connect all team members to it
Push and Pull from all members
Merge changes
Try to cause a merge conflict and resolve it
Commit

--------------------------------
Für die Abgabe:
----------------------------------

    cd C:\Users\annaz\Desktop\Projekt\maedn


*********************************
MERGE changes
*********************************

eventuell branch erstellen
    git checkout -b <branch-name>


1) Vorhandene branches anzeigen lassen
git branch

2) Wechsel zu einem anderen Branch, der nicht main ist
git checkout <branch-name>

3) Führe eine Änderung im Code lokal durch während man NICHT im main Branch ist
git add src/main/scala/Main.scala
git commit -m "    "
git push

4) In das Hauptprojekt also main Brnach wechseln
git checkout main
git pull 

5) Branch mergen (der Name steht für meinen Branch)
git merge <branch-name>
git push



******************************
CREATE A MERGE CONFLICT (main Branch)
*******************************

1) Beide arbeiten imselben Branch (überprüfen!=
    git branch
    git checkout main
    git pull

2) Beide ändern dieselbe Zeile in der Datei
- z.B
// Kommentar von Anna
//Kommentar von Layth

3) Eine Person pusht zuerst (z.B Anna)
git add src/main/scala/Main.scala
git commit -m "
git push

4) Zweite Person versucht ebenfalls zu pushen
git add src/main/scala/Main.scala
git commit -m "
git push

5) Zweite Person macht git pull -> Konflikt entsteht
git pull

6) Konflikt lösen und entscheidne, welche Version bleibt und dann...
git add src/main/scala/Main.scala
git commit -m "Konflikt gelöst"
git push



****************************************************
CREATE MERGE CONFLICT (two different branches)
****************************************************
1) Beide Starten vom aktuellen Stand
git checkout main
git pull

2) Beide erstellen eigene Branches
git checkout -b branch-anna
git checkout -b branch-layth

3) Beide ändern dieselbe Zeile in derselben Dateu

4) Beide committen ihre Änderung im eigenen Branch

Anna:
    git add src/main/scala/Main.scala
    git commit -m "Anna: Kommentar eingefügt"

Layth: 
    git add src/main/scala/Main.scala
    git commit -m "Layth: Kommentar eingefügt"

5) Anna merged ihren Branch zuerst in main
git checkout main
git pull
git merge branch-anna
git push

6) Layth versucht ebenfalls zu mergen
git checkout main
git pull
git merge branch-layth

7) Merge Konflikt lösen
- für ne Lösung entscheiden
- dann...

git add src/main/scala/Main.scala
git commit -m "Konflikt gelöst"
git push













--------------------------
GRUNDBEGRIFFE
--------------------------


SNAPSHOT
sowas wie ein Schnappschuss des Zustands einer Datei
man kann jederzeit zurückspringen und nachvollziehen, wer wann was geändert hat
1) Änderung vornehmen 2) git add . 3)git commit -m “Erklärung, was geändert wurde”

PUSH
lokalen Commits zu GitHub schicken
1) Code committen 2)git push

PULL
aktuelle Änderungen vonGithub auf lokalen Computer holen
1) git pull

BRANCH
Wenn man ein Hauptprojekt hat und eine neue Funktion ausprobirren will, ohne das Hauptprojekt durcheinanderzubringen, erstelllt man einen Branch
Ein branch ist also ein getrennter Entwicklungszweig
startet vom Hauptprojekt aus, aber man arbeitet unabhängig datan und wenn man fertig ist, führt man den Branch mit dem Hauptprojekt wieder zusammen

MERGE
Änderungen aus verschiedenen Branches oder von versch. leuten zusammenführen
Wenn man einen neuen Branch programmiert hat und es mit dem Hauptprogramm vereinigen möchte, nennt man das merge
passiert oft automatisch, wenn man per pull request in github arbeutet und auf merge klickt
oder lokal 1) git merge <branch-name>

MERGE KONFLIKT
wenn 2 Personen dieselbe stelle in der gleichen Datei unterschiedlich geändert haben
Git weiss dann nicht, welche änderung es nehmen soll
Lösung: Git zeigt Stellen mit Mergekonflikt an, man wählt manuell eine Variante oder kombiniert beide Varianten, man entfernt Konflikt-Markierungen wie <<<<, ====, >>>>
1) git add datei 2) git commit -m "Konflikt gelöst"


-----------------------------------------------------------
SCHRITTE
-----------------------------------------------------------

- Git installieren ERLEDIGT
    https://git-scm.com/downloads

- Projekt auf Github anlegen ERLEDIGT

- Layth hinzufügen ERLEDIGT
    Settings > Collaborators

- Projekt auf meinen PC holen also klonen MARCO FRAGEN????
    auf projekt gehen
    auf geünen code button klicken
    > HTTPs kopieren
    Ein Terminal öffnen


        git clone https://github.com/annaznvc/MAEDN.git

        cd my-team-project (MAEDN)

- Git konfigurieren ERLEDIGT
        git config --global user.name "Anna Zynovchenko"
        git config --global user.email "annazynovchenko05@gmail.com"

- Änderung machen und pushen ERLEDIGT

                            git add README.md
                            git commit -m "Änderung am README"
                            git push

- Änderungen vom Team holen ERLEDIGT

    git pull


Merge Konflikt induzieren
wir beide ändern die gleiche stelle in der datei
die Person, die als Zweites git push macht, bekommt einen Fehler

git pull

manuell anpassen, speichern und dann

git add README.md
git commit -m "Konflikt gelöst"
git push





