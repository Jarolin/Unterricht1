# Informatik Projekt 1
*von Julian und Benedict, 11e*
[Projektseite in der App Inventor Galerie](http://ai2.appinventor.mit.edu/?galleryId=5079043700555776)

## Inhaltsverzeichnis
* [Projekt](#Projekt)
  * [Idee](#Idee)
  * [App Inventor 2](#ai2)
* [Aufbau](#Aufbau)
  * [Oberfläche](#Oberfläche)
* [Stundenlog (*seperate Seite/Datei*)](https://github.com/StormarnJB/Unterricht1/blob/master/STUNDENLOG.md)



## Das Projekt <a name="Projekt"></a>

#### Die Idee <a name="Idee"></a>

Das Spiel „zwei“ ist angelehnt an das von Atari im Jahre 1976 herausgebrachte Arcade Spiel „Breakout“. In dieser Version gibt es allerdings nur zwei Blöcke, die immer wieder auftauchen. Es geht darum möglichst viele Punkte zu sammeln. Man bekommt jedes Mal 10 Punkte, wenn der Ball der sich am Anfang des Spiels in der Mitte des Bildschirms befindet (und durch wischen des Spielers einen Startimpuls bekommt), einen der beiden Blöcke berührt und somit zerstört, die dann sofort an anderer Stelle wiederauftauchen. Der Ball prallt von jeder Kante, sowie von den Blöcken und dem beweglichen Balken, ab. Trifft er allerdings auf die untere Kante ist das Spiel vorbei. Dies kann durch bewegen des Balkens verhindert werden, der sich allerdings nur horizontal bewegen lässt. Nach Spielende kann man seinen Namen eingeben und die erreichten Punkte in der Bestenliste automatisch eintragen lassen und einfach mit Freunden vergleichen, da nur das beste Ergebnis eines Spielers angezeigt wird, sofern er den gleichen Namen eingibt. Es können „unendlich viele“ Spieler in die Bestenliste aufgenommen werden, die sich aber auch ohne weiteres zurücksetzten lässt. Außerdem gibt es ein Einstellungsmenü in dem Hintergrundmusik und Geräusche (welche jedes Mal ertönt wenn der Ball einen Block oder den Balken trifft) unabhängig voneinander ein- und ausgeschaltet werden können. Zudem gibt es ein Pausenmenü.

#### App Inventor 2 <a name="ai2"></a>

"App Inventor" ist eine frei-zugängliche Online-Entwicklungsumgebung für Android Apps, diese würde ursprünglich von *Google Inc.* entwickelt und bereitgestellt, wird jedoch seit 2012 von dem *Massachusetts Institute of Technology* betrieben und weiterentwickelt.
Die Entwicklungsumgebung ermöglicht es einem, ohne große Vorkenntnisse, schnell und einfach eine eigene Android-App zu entwickeln. Sie besitzt 2 Ebenen, den "Design Editor" und den "Blocks Editor". Im Designmodus kann man die Oberfläche gestalten und festlegen welche Sensoren und andere Elemente des Zielgeräts im Blockeditor zur Verfügung stehen. Im Blockmodus kann man das Verhalten der App beziehungsweise ihrer Elemente programmieren.
*Quelle:* [*Wikipedia*](https://de.wikipedia.org/wiki/App_Inventor)

## Aufbau <a name="Aufbau"></a>

### Oberfläche <a name="Oberfläche"></a>
##### Screen1
![Screen1](https://raw.githubusercontent.com/StormarnJB/Unterricht1/master/Screenshots/DesignScreen1.png)

`Screen1` ist der Haupt- und Startbildschirm des Spiels. Auf der linken Seite kann man eine Vorschau des Designs sehen. An oberster Stelle befindet sich die `TopBar`, sie beinhaltet den Pauseknopf `Pause`, eine Anzeige für die Zeit und die aktuelle Punktzahl und den Knopf durch den man in das Einstellungsmenü gelangt. Dieses ist in der Vorschau nicht zu sehen, da es standardmäßig versteckt ist. Das Einstellungsmenü `Settingsbar` beinhaltet jeweils eine Checkbox um jeweils die Musik und die Geräusche ein-/auszuschalten, diese sind standardmäßig deaktiviert. Das Canvas `Canvas1` bildet das Gerüst für die Spielfläche. In ihr befinden sich `Block1` und `Block2`, welche man während des Spielens mit dem Ball `Ball1` treffen soll. Das letzte Element innerhalb des Canvas ist die untere Leiste `Leiste`. Unterhalb der Vorschau werden die nicht sichtbaren Komponenten der App angezeigt. `Clock1` gibt sekündlich ein Signal aus, welches im Blockeditor abgerufen wird, mit `Player1` kann die Musik abgespielt werden und mit `Hit`ein einzelnes Geräusch.

##### GameOver
![GameOver](https://raw.githubusercontent.com/StormarnJB/Unterricht1/master/Screenshots/DesignGameOver.png)

Der GameOver Bildschirm öffnet sich sobald der Ball bei `Screen1` auf die untere Bildschirmkante trifft. 
