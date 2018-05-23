<span style="font-size: 26px; color: red">Diese Seite ist noch nicht fertig!</span>

## Arrays mit For-Schleifen durchlaufen

Wir legen uns einen Array an, den wir dann mit einer For-Schleife durchlaufen wollen.
``` java
String[] unserArray = new String[] { "Apfel", "Birne", "Orange" };
```

Der 'klassische' Weg ein Array zu durchlaufen:
``` java
for (int i = 0; i < unserArray.length; i++) {
	String element = unserArray[i];
	// dein Code
}
```

Die Kurzform:
``` java
for (String element : unserArray) {
	// dein Code
}
```

Beide Code-Schnipsel machen genau das gleiche.