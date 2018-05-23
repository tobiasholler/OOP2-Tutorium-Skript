<span style="font-size: 26px; color: red">Diese Seite ist noch nicht fertig!</span>

# Wichtige JavaFX Klassen und deren Methoden
### die meiner Meinung nach Wichtig für die Prüfung sind

## javafx.application.Application
Die Klasse von der wir erben, wenn wir ein JavaFX programm erstellen. Siehe [Grundgerüst](../grundgeruest.md).

## javafx.stage.Stage
Die Klasse die unser Fenster repräsentiert. Wenn wir ein JavaFX-Programm erstellen, welches von der 
`Application`-Klasse erbt, wird unsere Stage automatisch erstellt und uns in der `start`-Methode übergeben.
#### Wichtige Methoden:
- `setScene(Scene value)`
    - Setzt die Szene für die Stage. Siehe [JavaFx Aufbau](javafx-aufbau.md).
- `setTitle(String value)`
    - Setzt den Fenstertitel
- `getTitle()`
    - Liefert den Fenstertitel zurück
- `show()`
    - Zeigt das Fenster auf dem Bildschirm an. Diese Methode sollte nach guten Programmierpraktiken immer erst nach dem erstellen der Benutzeroberfläche aufgerufen werden. Meistens ist sie der letzte Methodenaufruf in der `start`-Methode
- `setResizable(boolean value)`
    - Ändert die Eigenschaft, ob das Fenster vom Benutzer in der Größe verändert werden kann oder nicht.