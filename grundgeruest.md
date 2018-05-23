## Grundgerüst
### Kommandozeilen-Anwendung
``` java
class Klassenname {
	public static void main(String[] args) {
		// dein code hier...
	}
}
```

### JavaFX-Anwendung (ohne SceneBuilder)
``` java
package application;

import javafx.application.Application;
import javafx.stage.Stage;
import javafx.scene.Scene;
import javafx.scene.layout.BorderPane;

public class Main extends Application {
	@Override
	public void start(Stage primaryStage) {
		try {
			BorderPane root = new BorderPane();
			Scene scene = new Scene(root,400,400);
			scene.getStylesheets().add(getClass().getResource("application.css").toExternalForm());
			primaryStage.setScene(scene);
			primaryStage.show();
		} catch(Exception e) {
			e.printStackTrace();
		}
	}
	public static void main(String[] args) {
		launch(args);
	}
}
```
#### Kommentierte Version
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
 * anderem darum, dass ein Hauptfenster angelegt wird.
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
		try {
			BorderPane root = new BorderPane();
			Scene scene = new Scene(root, 400, 400);
			scene.getStylesheets().add(getClass().getResource("application.css").toExternalForm());
			primaryStage.setScene(scene);
			primaryStage.show();
		} catch(Exception e) {
			e.printStackTrace();
		}
	}
	/* Wie jedes vollstängie Java-Programm, besitzt unseres auch eine
	main-Methode
	public static void main(String[] args) {
		launch(args);
	}
}
```