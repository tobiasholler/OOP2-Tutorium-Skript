# Grundgerüst
## Kommandozeilen-Anwendung
``` java
class Klassenname {
	public static void main(String[] args) {
		// dein Code hier...
	}
}
```
### Kommentierte Version
Die Kommentare beschreiben immer die folgende Code-Zeile.

``` java
// Wir definieren eine Klasse mit einem beliebigen Namen
class Klassenname {
	/* Wir definieren die statische Methode 'main', welche beim Start des
	 * Programms ausgeführt wird. Sie bekommt den String-Array 'args' übergeben,
	 * in welchem die Argumente stehen, welche das Java-Programm über die
	 * Konsole gegeben bekommen hat.
	 */
	public static void main(String[] args) {
		// dein Code hier...
	}
}
```

## JavaFX-Anwendung (ohne SceneBuilder)
Als Layout benutzen wir hier die `BorderPane`, es kann jedoch auch jedes beliebige Layout benutzt werden.
``` java
package application;

import javafx.application.Application;
import javafx.stage.Stage;
import javafx.scene.Scene;
import javafx.scene.layout.BorderPane;

public class Main extends Application {
	@Override
	public void start(Stage primaryStage) {
		BorderPane root = new BorderPane();
		Scene scene = new Scene(root,400,400);
		primaryStage.setScene(scene);
		primaryStage.show();
	}
	public static void main(String[] args) {
		launch(args);
	}
}
```
### Kommentierte Version
Die Kommentare beschreiben immer die folgende Code-Zeile.
``` java
package application;
	
/* Hier importieren wir alle Klassen von JavaFX, die wir für unser kleines
 * Programm brauchen
 */
import javafx.application.Application;
import javafx.stage.Stage;
import javafx.scene.Scene;
import javafx.scene.layout.BorderPane;

/* Wir definieren die Klasse 'Main' welche von der Klasse 'Application' erbt.
 * Diese wird uns von JavaFX zur Verfügung gestellt und kümmert sich unter
 * anderem darum, dass ein Hauptfenster angelegt wird. Der Name der Klasse kann
 * Frei gewählt werden.
 */
public class Main extends Application {
	/* Mit @Override geben wir an, dass wir die folgende Methode überschreiben.
	 * Die Methode 'start' ist bereits in der Klasse 'Application' definiert.
	 */
	@Override
	/* Hier überschreiben wir die 'start'-Methode, dadurch ruft die
	 * 'Application'-Klasse nicht mehr ihre eigene 'start'-Methode auf, sondern
	 * unsere und übergibt das erzeugte Fenster an uns.
	 */
	public void start(Stage primaryStage) {
		/* Wir legen ein neues Layout, in diesem Fall ein 'BorderPane', an und
		 * speichern dies in der Variable 'root'. Wir brauchen dieses Layout
		 * damit die Controls, die wir hinzufügen wollen, eine Umgebung haben
		 * in welcher sie existieren können und von welcher sie angeordnet
		 * werden.
		 */
		BorderPane root = new BorderPane();
		/* Wir erstellen eine Scene welcher wir gleich das Layout als ersten
		 * Parameter übergeben. Die weiteren zwei Parameter sind die Breite und
		 * die Höhe der Scene. Diese sind optional. Die Scene füllt die
		 * komplette Stage.
		 */
		Scene scene = new Scene(root, 400, 400);
		/* Nun weisen wir der Stage die Scene zu
		 */
		primaryStage.setScene(scene);
		/* Und zeigen als letzten Schritt das Fenster auf dem Bildschirm an
		 */
		primaryStage.show();
	}
	/* Wie jedes vollstängie Java-Programm, besitzt unseres auch eine
	 * main-Methode. Diese existiert allerdings nur um die 'launch'-Methode,
	 * aufzurufen, welche wir von der Application-Klasse erben. Mit diesem
	 * Aufruf kümmert sich die Application-Klasse darum, dass die Stage erstellt
	 * wird und danach unsere 'start'-Methode aufgerufen wird.
	 */
	public static void main(String[] args) {
		/* Wir rufen die 'launch'-Methode auf und übergeben ihr die
		 * Kommandozeilenargumente, damit die Application-Klasse diese auf
		 * unseren Wunsch verarbeiten kann.
		 */
		launch(args);
	}
}
```