# Informatik Projekt 1
*von Julian und Benedict, 12e*

[Projektseite in der App Inventor Galerie](http://ai2.appinventor.mit.edu/?galleryId=5079043700555776)

## Inhaltsverzeichnis
* [Projekt](#Projekt)
  * [Spiel](#Idee)
  * [App Inventor 2](#ai2)
* [Aufbau](#Aufbau)
  * [Oberfläche](#Oberfläche)
  * [Blöcke](#Blöcke)
* [Stundenlog (*seperate Datei*)](https://github.com/StormarnJB/Unterricht1/blob/master/STUNDENLOG.md)



## Das Projekt <a name="Projekt"></a>

#### Das Spiel <a name="Idee"></a>

Das Spiel „zwei“ ist angelehnt an das von Atari im Jahre 1976 herausgebrachte Arcade Spiel „Breakout“. In dieser Version gibt es allerdings nur zwei Blöcke, die immer wieder auftauchen. Es geht darum möglichst viele Punkte zu sammeln. Man bekommt jedes Mal 10 Punkte, wenn der Ball der sich am Anfang des Spiels in der Mitte des Bildschirms befindet (und durch wischen des Spielers einen Startimpuls bekommt), einen der beiden Blöcke berührt und somit zerstört, die dann sofort an anderer Stelle wiederauftauchen. Der Ball prallt von jeder Kante, sowie von den Blöcken und dem beweglichen Balken, ab. Trifft er allerdings auf die untere Kante ist das Spiel vorbei. Dies kann durch bewegen des Balkens verhindert werden, der sich allerdings nur horizontal bewegen lässt. Nach Spielende kann man seinen Namen eingeben und die erreichten Punkte in der Bestenliste automatisch eintragen lassen und einfach mit Freunden vergleichen, da nur das beste Ergebnis eines Spielers angezeigt wird, sofern er den gleichen Namen eingibt. Es können „unendlich viele“ Spieler in die Bestenliste aufgenommen werden, die sich aber auch ohne weiteres zurücksetzten lässt. Außerdem gibt es ein Einstellungsmenü in dem Hintergrundmusik und Geräusche (welche jedes Mal ertönt wenn der Ball einen Block oder den Balken trifft) unabhängig voneinander ein- und ausgeschaltet werden können. Zudem gibt es ein Pausenmenü.

#### App Inventor 2 <a name="ai2"></a>

"App Inventor" ist eine frei-zugängliche Online-Entwicklungsumgebung für Android Apps, diese wurde ursprünglich von *Google Inc.* entwickelt und bereitgestellt, wird jedoch seit 2012 von dem *Massachusetts Institute of Technology* betrieben und weiterentwickelt.
Die Entwicklungsumgebung ermöglicht es einem, ohne große Vorkenntnisse, schnell und einfach eine eigene Android-App zu entwickeln. Sie besitzt 2 Ebenen, den "Design Editor" und den "Blocks Editor". Im Designmodus kann man die Oberfläche gestalten und festlegen welche Sensoren und andere Elemente des Zielgeräts im Blockeditor zur Verfügung stehen. Im Blockmodus kann man das Verhalten der App beziehungsweise ihrer Elemente programmieren.
*Quelle:* [*Wikipedia*](https://de.wikipedia.org/wiki/App_Inventor)

## Aufbau <a name="Aufbau"></a>

### Oberfläche <a name="Oberfläche"></a>
##### Screen1
![Screen1](https://raw.githubusercontent.com/StormarnJB/Unterricht1/master/Screenshots/DesignScreen1.png)

`Screen1` ist der Haupt- und Startbildschirm des Spiels. Auf der linken Seite kann man eine Vorschau des Designs sehen. An oberster Stelle befindet sich die `TopBar`, sie beinhaltet den Pausenknopf `Pause`, eine Anzeige für die Zeit und die aktuelle Punktzahl und den Knopf durch den man in das Einstellungsmenü gelangt. Dieses ist in der Vorschau nicht zu sehen, da es standardmäßig versteckt ist. Das Einstellungsmenü `Settingsbar` beinhaltet jeweils eine Checkbox um jeweils die Musik und die Geräusche ein-/auszuschalten, diese sind standardmäßig deaktiviert. Das Canvas `Canvas1` bildet das Gerüst für die Spielfläche. In ihr befinden sich `Block1` und `Block2`, welche man während des Spielens mit dem Ball `Ball1` treffen soll. Das letzte Element innerhalb des Canvas ist die untere Leiste `Leiste`. Unterhalb der Vorschau werden die nicht sichtbaren Komponenten der App angezeigt. `Clock1` gibt sekündlich ein Signal aus, welches im Blockeditor abgerufen wird, mit `Player1` kann die Musik abgespielt werden und mit `Hit` ein einzelnes Geräusch.

##### GameOver
![GameOver](https://raw.githubusercontent.com/StormarnJB/Unterricht1/master/Screenshots/DesignGameOver.png)

Der GameOver Bildschirm öffnet sich sobald der Ball bei `Screen1` auf die untere Bildschirmkante trifft und ermöglicht einen Neustart des Spiels und eine Bestenliste. Um die Bestenliste anzuzeigen wird das `HighScoreListView` benutzt. Auf der unteren Seite befinden sich der `ResetButton` mit dem die Bestenliste zurückgesetzt werden kann und der `RestartButton` mit dem das Spiel neugestartet werden kann. Zusätzlich existiert die Datenbank `TyniDB1` um die Daten für die Bestenliste auch nach Beenden der App zu speichern. Der `NameNotifier` fragt beim Öffnen des Bildschirms nach dem Namen und der `ResetNotifier` fordert eine Bestätigung nach dem Drücken des `ResetButton`.


### Blöcke <a name="Blöcke"></a>
##### Screen1

![Teil 1](https://raw.githubusercontent.com/StormarnJB/Unterricht1/master/Screenshots/Screen1Blocks1.PNG)

`Screen1` ist bei AppInventor immer der Startbildschirm und lässt sich nicht umbenennen. Sobald dieser gestartet wird werden die 3 Variablen `paused`, `seconds` und `flung` initialisiert, zusätzlich wird der Text `Loading`versteckt, da erst nach einer Layoutänderung alle Elemente richtig angezeigt werden. Durch diese Änderung beginnt der Ball sich zu bewegen, deshalb wird seine Geschwindigkeit auf '0' gesetzt. Die Leiste wird in ihre Ausgangsposition versetzt. Sobald `Clock1` gestartet wird, beginnt sie sekündlich ein Signal auszugeben, wodurch der Timer aktualisiert wird. Die Variable `seconds` wird jeweils um '1' erhöht, anschließend wird diese durch '60' geteilt (und abgerundet) um die Minutenzahl zu ermitteln. Um die Sekundenzahl zu ermitteln wird der Teilungsrest ermittelt. Aus ästhetischen Gründen wird dieser falls er niedriger als '10' ist von einer "0" angeführt.

![Teil 2](https://raw.githubusercontent.com/StormarnJB/Unterricht1/master/Screenshots/Screen1Blocks2.PNG)

In diesem Teil wird das Verhalten der verschiedenen Elemente im Canvas festgelegt. Sobald `Ball1` vom Spieler über den Bildschirm gezogen wird (`Ball1.Flung`) wird dies gespeichert, dem Ball eine Geschwindigkeit und ein Aktualisierungsintervall gegeben, seine Richtung angepasst und der Timer gestartet. Da der Ball nur zu Beginn des Spiels direkt bewegt werden darf, wird überprüft ob `flung` 'true' ist. Trifft der Ball nun auf eine Kante von `Canvas1` prallt er, solange es sich nicht um die untere Kante handelt, von dieser ab. Handelt es sich jedoch um die untere Kante, wird der Ball und die Musik gestoppt, der Bildschirm geschlossen und der `GameOver` Bildschirm unter Weitergabe der Punktzahl geöffnet. Aufgrund von Beschränkungen durch App Inventor lässt sich ein Bildschirm nicht schließen und gleichzeitig ein anderer öffnen, da das aber zu Problemen mit der Leistungen führen kann und auch zu einem nervigen Fehler führte, werden die Befehle einzeln auf die gezeigte Weise ausgeführt.
Kollidiert der Ball mit einem Objekt `other` wird überprüft ob es sich bei diesem Objekt um `Leiste` handelt, tut es dass wird die Richtung des Balls gedreht. Wenn die Leiste sich aber wie ein Spiegel verhält wäre das Spiel alleine durch den Startimpuls entschieden, um dem vorzubeugen wird die Richtung des Balls um bis zu 15 Grad zufällig verändert. Falls erwünscht, wird unabhängig von `other` ein Geräusch abgespielt.
Wenn es sich bei `other` nicht um die Leiste handelt, es also zwingend einer der Blöcke ist, wird die Punktzahl erhöht, die Richtung des Balls geändert und der Block an eine zufällige Stelle im oberen Drittel von `Canvas1` gesetzt. Dabei kann es jedoch vorkommen, dass die Blöcke übereinander liegen, ist dies der Fall wird die Position des Blockes erneut geändert.
Die Leiste lässt sich durch den Spieler verschieben, dieser kann das aber nur auf der x-Ebene tun.

![Teil 3](https://raw.githubusercontent.com/StormarnJB/Unterricht1/master/Screenshots/Screen1Blocks3.PNG)

Die `pause`-Funktion wird immer dann aufgerufen, wenn das Spiel pausiert werden soll. Ist `paused` 'false', das Spiel also nicht pausiert, wird `paused` auf 'true' gesetzt, der Ball gestoppt, die Leiste blockiert und dem Spieler visualisiert, dass das Spiel pausiert ist. Wird `pause` aufgerufen, während `paused` 'true' ist, wird dieses auf 'false' gesetzt, dem Ball erneut die Geschwindigkeit 10 zugewiesen und der Hintergrund wieder zur Standardfarbe geändert. Um zu verhindern, dass der Ball sich bewegt, bevor das Spiel gestartet wird, wird dies überprüft und falls nötig die Geschwindigkeit auf '0' gesetzt.
Drückt man auf `Pause`, den (meist physischen) Zurückknopf auf dem Gerät oder auf `Settings` wird die `pause`-Funktion aufgerufen. Um zu verhindern, dass das Spiel nach dem klicken von `Settings` weiterläuft wird `paused` auf 'false' gesetzt und die `Settingsbar` wird agezeigt, die `Topbar` wird versteckt. `Settingsback` tut das genaue Gegenteil. Innerhalb des Einstellungsmenüs befindet sich auch `CheckBoxMusic`, mit welcher man auf Wunsch Musik abspielen und beenden kann. 

##### GameOver

![Teil 1](https://raw.githubusercontent.com/StormarnJB/Unterricht1/master/Screenshots/GameOverBlocks1.PNG)

Nach dem Öfnnen von `GameOver` werden die Variablen `score` und `highscore` initialisiert. Score wird auf den Punktestand (`start value`) gesetzt und der NameNotifier fordert den Nutzer auf einen Namen für die Eintragung in die Bestenliste einzugeben. Sobald ein Name eingegeben wurde, wird die Bestenliste angezeigt. Diese kann über den `ResetButton` zurückgesetzt werden. Um ein ungewünschtes Löschen zu verhindern wird ein Dialog über den `ResetNotifier` geöffnet, der um Bestätigung bittet. Wird 'Ja' gewählt, wird die TinyDB1 geleert und die `showScores`-Funktion aufgerufen. Der `RestartButton` öffnet den Spielbildschirm.

![Teil 2](https://raw.githubusercontent.com/StormarnJB/Unterricht1/master/Screenshots/GameOverBlocks2.PNG)

Sobald `NameNotifier` eine Eingabe erhalten hat, wird der Name mit der Punktezahl gespeichert. Vor dem Einspeichern wird überprüft ob das Textfeld vom `NameNotifier` leer gelassen wurde. Bei dem Einspeichern wird zusätzlich überpüft ob unter dem gleichen Namen bereits ein besserer Wert eingespeichert wurde, falls ja wird dieser beibehalten. Nach dem Einspeichern wird die `showScores`-Funktion aufgerufen, welche die Bestenliste sortiert und anzeigt.
Am Anfang wird eine Liste mit dem Element 'Nulll: 0' erstellt, welches am Ende wieder entfernt wird. Nachdem die Liste erstellt wurde wird über die Elemente von TinyDB1 iteriert. `itemdb` stellt den Namen (`tag`) und `itemdb_value` den zugehörigen Punktestand (`value`) dar. Diese beiden Werte werden jeweils an die `putinlist`-Funktion weitergegeben.
Die `putinlist` beinhaltet erneut eine Schleife. Diese iteriert über die Elemente der Liste `highscore`, diese muss deshalb am Anfang mindestens ein Element beinhalten. Innerhalb der einzelnen Elemente der Liste werden die einzelnen Werte (Namen und Punkte) durch ": " getrennt. Innerhalb der Schleife werden diese Werte dann wieder aufgetrennt, um die Punkte miteinander ergleichen zu können. Die Schleife wird solange ausgeführt bis ein `Value` (also der Wert aus` TinyDB1`), den Wert `item_value`, welcher gerade von der zweiten Schleife aufgerufen wird, übersteigt oder entspricht. Sobald dies der Fall ist werden `Tag` und `Value` in die Liste an der Stelle `index` eingespeichert (wobei die erste Stelle der Liste den index '1' besitzt) und die Schleife beendet. Da das letzte Element ('Nulll: 0') den Punktestand '0' beinhaltet und negative Punktzahlen nicht möglich sind, wird kein Element von `TinyDB1` übersprungen.
In der `showScores`-Funktion werden nun die von `HighscoreListView` anzuzeigenden Elemente auf die Liste `highscore` festgelegt.


#### [Zum Stundenlog](https://github.com/StormarnJB/Unterricht1/blob/master/STUNDENLOG.md)
