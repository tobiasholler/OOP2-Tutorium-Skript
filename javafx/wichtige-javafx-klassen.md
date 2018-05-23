# Wichtige JavaFX Klassen und deren Methoden
### die meiner Meinung nach Wichtig für die Prüfung sind

## javafx.application.Application
Die Klasse von der wir erben, wenn wir ein JavaFX programm erstellen. Siehe Grundgerüst.

## javafx.stage.Stage
Die Klasse die unser Fenster repräsentiert. Wenn wir ein JavaFX-Programm erstellen, welches von der 
`Application`-Klasse erbt, wird unsere Stage automatisch erstellt und uns in der `start`-Methode übergeben.
#### Wichtige Methoden:
- `setScene(Scene value)`
    - Setzt die Szene für die Stage. Siehe JavaFx Aufbau.
- `setTitle(String value)`
    - Setzt den Fenstertitel
- `getTitle()`
    - Liefert den Fenstertitel zurück
- `show()`
    - Zeigt das Fenster auf dem Bildschirm an. Diese Methode sollte nach guten Programmierpraktiken immer erst nach dem erstellen der Benutzeroberfläche aufgerufen werden. Meistens ist sie der letzte Methodenaufruf in der `start`-Methode
- `setResizable(boolean value)`
    - Ändert die Eigenschaft, ob das Fenster vom Benutzer in der Größe verändert werden kann.