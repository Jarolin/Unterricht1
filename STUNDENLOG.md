# Informatik - Stundenlog

## *Inhalt:* <a name="Inhalt"></a>
1. [August](#August)
2. [September](#September)
3. [Oktober](#Oktober)
4. [November](#November)


## August <a name="August"></a>
### 21. August - Einführung

In unser ersten Informatikstunde, am 21. August erhielten wir eine Einführung in die Abläufe des Informatikunterrichts. Wir überlegten uns einige Projektideen, hatten jedoch noch keine genaue Vorstellung was wir machen wollen und womit wir arbeiten möchten.
Da es im Computerraum zu wenige Computer für einen so großen Kurs gab, entschieden wir uns in dem Unterricht an unserem eigenen Laptop zu arbeiten, da wir so freier in der Umsetzung und Bearbeitung sind. 


### 27. August - Einrichtung

Am 27. August versuchten wir ohne Erfolg in das Netzwerk der Schule zu kommen. Währenddessen überlegten wir uns wie wir weiter fortfahren können und beschlossen einige Kenntnisse durch Anleitungen für Anfänger zu sammeln.


### 28. August - Einrichtung und Aneignung erster Erfahrungen

Nachdem wir uns erfolgreich in das Schulnetzwerk eingeloggt haben, begannen wir damit uns die ersten Kenntnisse anzueignen. Wir fingen an uns mit einer kleinen Einführung auf Code.org auseinanderzusetzen und schrieben dort auch unser erstes (sehr) kleines Programm.
Zusätzlich erstellten wir uns einen eigenen Github Account, auf dem wir unseren zukünftigen Projektfortschritt dokumentieren und die finale Version von diesem zu präsentieren.


## September <a name="September"></a>
### 10. September - Beginn mit App Inventor

Am 10. September beschlossen wir unser Projekt mit App Inventor durchzuführen und lernten uns in die Bedienung von eben diesem ein. Da wir noch keine feste Vorstellung von der benötigten Zeit von einem Projekt bei App Iventor hatten, begannen wir damit einen sehr simplen Taschenrechner zu entwickeln.
![](https://raw.githubusercontent.com/StormarnJB/Unterricht1/master/Screenshots/Screenshot%202018-09-11%20at%2015.09.03.png)


### 11. September - Beginn von finalem Projekt

Am 11. September beschlossen wir nach unserer ersten Erfahrung mit dem Taschenrechner ein umfangreicheres Projekt ins Auge zu fassen. Wir beschlossen ein dem von Atari veröffentlichten Spieleklassiker "Breakout" ähnliches Projekt.
![https://en.wikipedia.org/wiki/File:Breakout2600.svg](https://upload.wikimedia.org/wikipedia/en/thumb/2/2b/Breakout2600.svg/640px-Breakout2600.svg.png)

Original Atari Breakout - [Bild von WikiMedia](https://en.wikipedia.org/wiki/File:Breakout2600.svg)

### 17. September - Aufbau des Grundgerüsts (inkl. Steuerung über Bewgungssensor)

Am 17. September begannen wir dann damit das Grundgerüst der App zu designen und eigneten uns Kenntnisse über das Arbeiten mit Canvas an. Anfangs beschlossen wir die Steurung nicht über den Touch-Bildschirm zu gestalten, sondern über den Gyroskopsensor unseres Smartphones. Wir versuchten den unteren Balken durch die Rotation des Smartphones zu steuern. Zeitbedingt konnten wir dies jedoch nicht mehr testen und nahmen uns das für die nächste Stunde vor.
![](https://github.com/StormarnJB/Unterricht1/blob/master/Screenshots/17-09-1.png)
Erste Versuche eine Bewegungssteuerung einzurichten


### 18. September - Fertigstellung des Grundgerüsts und der Steuerung

Am 18. September stellten wir das Grundgerüst für die App fertig und einigten uns auf eine endgültige Spielidee. ZUsätzlich richteten wir einen "GameOver Screen" ein. Am Ende der Stunde besaßen wir die erste tatsächliche spielbare Version. Beim Testen stellten wir fest, dass die Steuerung über den Bewegungssensor sich als nicht sehr komfortabel und genau gestaltet und beschlossen diese durch eine "Touch-Steuerung" zu ersetzen.
![](https://raw.githubusercontent.com/StormarnJB/Unterricht1/master/Screenshots/Screenshot%202018-09-18%20at%2015.17.45.png)
Version mit (*in diesem Bild nicht funktionsfähiger*) Bewegungssteuerung

![](https://raw.githubusercontent.com/StormarnJB/Unterricht1/master/Screenshots/Screenshot%202018-09-18%20at%2016.27.46.png)
Version mit "Touch-Steuerung"


## Oktober <a name="Oktober"></a>
### 22. Oktober - Fehlerbehebung

Am 22. September bearbeiteten wir den "GameOver" Bildschirm, sodass dort die erreichten Punkte angezeigt werden können, zusätzlich fügten wir einen "Neu starten" Knopf ein. Dabei machten wir jedoch einen Fehler, sodass sich dieser in kürzester Zeit immer wieder öffnete. Wir hatten jedoch keine Idee woher dieses Problem kam und wie wir es lösen können.


### 23. Oktober - Erstellen eines Einstellungsmenüs und weitere Fehlerbehebungen

Anfangs in der Entwicklung fügten wir einen Einstellungsknopf hinzu, dieser konnte jedoch noch nichts. Zusätzlich fanden wir nach einigem Rumprobieren den Fehler, der Ball bewegte sich auch nach dem Öffnen des neuen Screens weiter und kollidierte so häufiger mit der unteren Bildschirmkante, was in dem häufigen Öffnen des "GameOver-Screens" resultierte. Um das zu verhindern setzen wir die Geschwindigkeit des Balls auf 0 und schließen den Hauptbildschirm.
![](https://raw.githubusercontent.com/StormarnJB/Unterricht1/master/Screenshots/Screenshot%202018-10-23%20at%2016.25.23.png)
Das aktuelle Aussehen der App


### 29. Oktober - Überarbeiten des Pausemenüs

Am 29. Oktober eigneten wir uns Wissen über Prozeduren an und führten eine Pauseprozedur ein, da wir die gleichen Befehle bereits an bei dem Klicken des Pauseknopfes, dem Öffnen des Einstellungsknopfes und dem Berühren des Android-Zurückknopf ausführen.
![](https://raw.githubusercontent.com/StormarnJB/Unterricht1/master/Screenshots/Screenshot%202018-10-29%20at%2011.16.20.png)
Der aktuelle Code mit der neuen Pauseprozedur


### 30. Oktober - Hinzufügen von Hintergrundmusik

Am 30. Oktober fügten wir Hintergrundmusik und Soundeffekte hinzu. Diese lassen sich über zwei Checkboxen im Einstllungsmenü ein-/ausschalten. Außerdem fügten wir einen Timer hinzu der bei dem Spielebildschirm die Dauer einer Runde anzeigt.
Außerdem haben wir unsere Notizen von der Wikiseite auf die "Readme.md" (jetzt "STUNDENLOG.md") verschoben.
![](https://raw.githubusercontent.com/StormarnJB/Unterricht1/master/Screenshots/Screenshot%202018-10-30%20at%2016.17.51.png)

Die Timer Funktion


## November <a name="November"></a>
### 6. November - Beginn von einer Bestenliste
Bereits am Anfang wollten wir eine Bestenliste in unser Projekt einbauen, uns fehlte jedoch ein Ansatz dies auch umzusetzen. Da unser Spiel bereits fast alle von uns gewünschten Funktionen beinhaltete, begannen wir uns mit der Bestenliste auseinanderzusetzen. Wir begannen damit, indem wir uns über die verschiedenen Wege mit App inventor Daten zu speichern informierten. Die Bestenliste sollte zusätzlich zu den Punkten natürlich auch einen Namen zu dem Spieler anzeigen. Das alles gestaltete sich jedoch komplizierter als wir zuerst gedacht hatten und so schafften wir es nicht im Zeitrahmen der Stunde eine funktionale Version zu erstellen.


### 12. November - Überarbeitung des Stundenlogs #1

Da der Zeitraum für unser Projekt sich dem Ende zuneigt und wir unser Stundenlog größtenteils noch nicht ausformuliert hatten, unsere app aber fast fertig war, entschieden wir uns dies während den noch ausstehenden Stunden zu erledigen. 
Also begannen wir damit unsere Aufzeichnungen in ganzen Sätzen auszuformulieren und in Zusammenhang zu unseren Screenshots zu bringen und entschieden uns welche davon am besten geeignet sind um unsere Fortschritte zu dokumentieren.


### 13. November - Überarbeitung des Stundenlogs #2

Weil wir am vorherigen Tag nicht mit dem STundenlog fertig geworden sind haben wir daran weitergearbeitet. Wir haben entschieden die Bestenlistenfunktion zuhause zu vervollständigen und haben hierzu konkrete Pläne gefasst. Während wir unser Stundenlog schrieben testeten wir die App ausgiebig auf Fehler um diese vor der Abgabe zu beheben. Wir konnten einige Dinge feststellen, an denen wir noch nachbessern konnten/mussten. So wird zum Beispiel die Flugbahn des Balls nicht mehr genau um 180° gedreht, sondern um einen zufälligen Wert von 175°-195° um den Spielspaß zu erhöhen.


### 20. November - Überarbeitung des Stundenlogs #3

Da unser Spiel mittlerweile fertiggestellt war, unser Stundenlog jedoch noch ausbaufähig war arbeiteten wir an diesem weiter. Wir entschieden uns das Stundenlog aufgrund der Übersichtlichkeit auf eine eigene Datei zu verschieben und auf der Hauptdatei (Readme.md) unser Projekt ausführlich vorzustellen.



[Zurück zum Anfang](#Inhalt)
