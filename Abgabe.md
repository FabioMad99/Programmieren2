## Lesson 1: Git Basics, Gradle

## Aufgabe 1: Git status erklären

```
pm-lecture % git status
On branch b03

Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git restore <file>..." to discard changes in working directory)
modified:   CONTRIBUTING.md
modified:   homework/b03.md

Untracked files:
(use "git add <file>..." to include in what will be committed)
foo.java

no changes added to commit (use "git add" and/or "git commit -a")
```

Bei der oben beschriebenen Fehler meldung gibt es mehrere Fehler.
1. Die files die geändert wurden, wurden nicht zum stage hinzugefügt
```
modified:   CONTRIBUTING.md
modified:   homework/b03.md
```
2. Es gibt eine untracked file die bei Git noch nicht existiert, aber lokal vorhanden ist. Mit **git add foo.java** würde man diese datei stagen und dann mit git commit commiten.
3. Die letzte Zeile ```no changes added to commit (use "git add" and/or "git commit -a")``` sagt nur, dass nichts mit git add hinzugefügt wurde und der commit nichts commiten kann.


## Aufgabe 2: Git-Spiel

Zunächste habe ich mit **git log --oneline --decorate --graph** die ganzen commits als oneliner an. Somit kann ich zwischen den Tagen besser hin und her springen.

# Aufgabe 2.1
- An Tag 01 stürzte sich der furchtlose Held Markus in einen gefährlichen Dungeon. Obwohl es voll mit Monster lauert, ist der Held entschlossen das Amulet zu finden.
- Der Held hatte an Tag1 4 EXP zuerst erreicht beim Erlegen einer Ratte.
- Tag2 hatte der Held zum ersten mal 10 Hungerpunkte.
- Insgesamt erhielt der Held 2 Heiltränke. Tag3 an einem Shop und Tag4 von einer Gerippe
- Er hat ein Zwergenbrot und ein Heiltrank mit seinen talentierten Verhandlungen für 10, statt 16 Gold bezahlt. (Brot von 6 zu 5. Heiltrank von 10 zu 5)
- Zwischen Tag 3 und 4 wurden folgende Sachen geändert: 
  - rucksack.md wurde mehrfals geändert. -5Gold +1Brot. -5Gold +1Heiltrank. -1Brot -1Heiltrank
  - Beim verschwinden vom Brot/Heiltrank in rucksack.md wird in stats.md health auf 10 gesetzt und hunger auf 0
- Direkt nach dem Shop (Tag3) sein Brot. (Als Getränk den Heiltrank)

# Aufgabe 2.2
Ich hatte leider Probleme mit dem Klonen und die Commits sind dann verloren gegangen. (selbst mit git reflog --all) 
4.5 mit "git commit --amend" kann ich leider nur beschreiben.
- In der stats.md die EXP auf 42 gesetzt und mit "git commit --amend" den letzten commit (Tag 4.5) als Basis genommen und diese commitet.

4.6-4.8 sind als commits da
Ich entschuldige mich dafür

# Aufgabe 2.3

Meiner Meinung nach...

**Commit 46530b6:**
- Rebase nicht als Commit-msg dokumentieren
- spotlessApply anders schreiben (chore: code formatiert) wobei das auch überflüssig ist
- EntetiyController wird auch angepasst aber nicht dokumentiert

**Commit 3e37472:**
- etwas verständlicher
- "add some on use methods" = some ist unpräzise und *welche Methoden*?
- "use new item onUse signature" würde das "use new" umändern zu update / refactor

