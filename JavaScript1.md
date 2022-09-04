# JavaScript 

## JavaScript läuft im Browser
JavaScript ist eine Skriptsprache, welche entwickelt wurde um die Darstellung von Inhalten und Möglichkeiten für die Benutzerinterkation mit Webinhalten zu verbessern. Daher ist es wenig überaschend, dass JavaScript vorrangig im Webbrowser ausgeführt wird. Jede Website besteht auf unterster Ebene aus HTML (Hypertext Markup) Elementen, welche die prinzipielle Anordnung aller Elemente einer Website beschreibt. Diese Elemente sind in ener baumartigen hirarchischen Struktur angeordet. Jede HTML Website besteht aus einem `head` Element und einem `body` Element. 

	<!DOCTYPE html>
	<html>
	<head>
	  <meta charset="UTF-8">
	  <title>Meine erste Website</title>
	</head>
	<body>
	  Hier ist irgendein Text!
	</body>
	</html>
	
Jede Website besteht aus verschachtetelten und mitunter sehr komplizierten Kombinationen solcher HTML Tags. Wir können uns jede beliebige Website in dieser "rohen" Form anzeigen lassen, indem wir im Browser über die `F12` Taste die Developer Tools aufrufen. Um unser erstes HTML Dokument im Browser aufrufen zu können, müssen wir den obigen Code Abschnitt in ein eigenes HTML File speichern und dann lokal im Browser ausführen. Wir schreiben nun unser erstes JavaScript Programm innerhalb dieses HTML Dokuments. Dazu fügen innerhalb der `body` Sektion einen `script` Tag  wie folgt ein.

	<!DOCTYPE html>
	<html>
	<head>
	  <meta charset="UTF-8">
	  <title>Meine erste Website</title>
	</head>
	<body>
	  <script>
	  	console.log("Hallo Welt!"); //Hallo Welt 
	  </script>
	</body>
	</html>
	
Wenn wir nun in den Developer Tools die Konsole aufrufen, dann könenn wir dort unsere Textausgabe sehen. Mit Hilfe des `window.alert("Hallo Welt!");` Befehls könenn wir uns den Text auch direkt in einem Popup Fenster anzeigen lassen. Gratulation wir haben unser erstes JavaScript Programm geschrieben! Wir müssen unseren JavaScript Code nicht zwingend innerhalb des HTML Files angeben sondern können auch ein externes Skript verlinken. Dazu erstellt man im gleichen Ordner in dem auch die *index.html* liegt eine neue JabaScript Datei (beispielsweise *App.js*) und gibt den Pfad innerhalb des `<script src="App.js"></script>` an. Von nun an verweisen wir ausschließlich auf ein solches externes Skript, um uns den html boilerplate zu sparen. 

## Variablen in JavaScript
Es gibt mehrere verschieden Möglichkeiten eine Variable in JavaScript zu definieren. Im Folgendem gehen auf mehrere Varianten ein und erklären kurz die wichtigsten Unterschiede. Eine Variable können wir uns am besten als einen beschriftete Box vorstellen, welche irgendwelche Daten speichert, um später darauf zurückgreifen zu können. Nehmen wir zum Beispiel an wir wollen den Namen einer Person in einer Variable speichern. Dafür nutzen wir die Synthax `let name = "Bob"`. Die Zeile sieht auf den ersten Blick trivial aus führt aber bereits einige wichtige Prinzipien immer wieder relevant werden. Zuerst gehen wir auf `let` ein. Dieses ist ein **Schlüsselwort**, welche JavaScript mitteilt, dass wir eine Variable deklarieren wollen. Schlüsselwörter werden später noch sehr relevant sein und dürfen nur in ihrem jeweiligen Kontext verwendet werden. Nach dem `let` vergeben wir einen **Identifier** für die Variable. In unserem Fall ist dies `name`. Das ist der Name den wir auf unsere Box schreiben. Wir können nahezu beliebige Identifier vergeben, allerdings gibt es einige Regeln zu beachten. Es wird zwischen Groß- und Kleinschreibung unterschieden und ein Variablenname darf nicht mit einer Zahl beginnen. Das Gleichheitszeichen nach dem Identifier ist anders als in der Mathematik nicht als eine Aussage zu verstehen, sondern weist den Computer an der deklarierten Variable den Wert hinter dem Gleichheitszeichen zuzuordnen. Das Gleichheitszeichen ist ein **Operator** in JavaScript.  
Wir können nun auf diese Variable ganz einfach zugreifen in dem wir an geeigneten Stellen einfach den Identifier benutzen.

	let name = "Bob";
	console.log("Hallo " + name); //Hallo Bob

Erwähnenswert ist das wir in unserem letzten Codebeispiel einen weiteren Operator, den `+` Operator bentzt haben. Dieser hat je nach Kontext eine verschiedene Wirkunsgweise auf, welche wir später noch genauer eingehen werden. Wenn eine Variable einmal deklariert ist so kann ihr auch später ein anderer Wert zugeschrieben werden. Dazu weisen wir ihr einfach mit dem Zuweisungsoperator einen neuen Wert zu. 

	let name = "Bob";
	console.log("Hallo " + name); //Hallo Bob
	name = "Frank";
	console.log("Hallo " + name); //Hallo Frank

Wichtig ist, dass bei einer erneuten Zuweiseung das Schlüsselwort `let`nicht erneut aufgerufen werden darf, da die Variable name bereits initialisiert worden ist. Es ist auch möglich, die Initialisierung und Zuweisung von Variablen vollständig zu trennen. So ist 

	let name;
	name = "Bob";
	console.log("Hallo " + name); //Hallo Bob
 
 vollkommen äquivalent zu unserem ersten Beispiel. Es gibt noch zwei weitere Beipspiel für eine Variablendeklaration, welche der Vollständigkeit halber erwähnt werden sollte. Statt mit dem Schlüsselwort `let` können wir eine Variable auch mit `const` und `var` initialisieren. Da `var` mittlerweile veraltet ist und einige Nebeneffekte hat, sollte diese Art nicht mehr verwendet werden. Dahingegen ist `const` noch gebräuchlich und wird verwendet. Der Unterschied zu `let` ist, dass eine mit `const` zugewiesene Variable nicht wieder zugewiesen werden darf. Sie ist somit konstant mit einem Wert belegt. Anders als eine mit `let` initialisierte Variable muss eine Konstante auch direkt mit einem Wert belegt werden. 
 
	const name = "Bob";
	name = "Frank" // Stürzt mit einem TypeError "Assignment to constant variable." ab. 

## Mathematische Operatoren
Bisher haben wir in Variablen nur Text sogennante *Strings* gespeichert. Natürlich können wir aber auch Zahlen in Variablen speichern und mit Zahlen rechnen. Um mit Zahlen rechnen zu können brauchen wir Operatoren. Es gibt 8 mathematische Operatoren in JavaScript. 

|Operator | Beschreibung             | Beispiel                                                      |
|:-------:|--------------------------|---------------------------------------------------------------|
|   `+`   | Addition                 | `let result = 8 + 3; //result ist 11`                         |
|   `-`   | Subtrakion               | `let result = 5 - 11; //result ist -6`                        |
|   `*`   | Multiplikation           | `let result = 7 * 8; //result ist 42`                         |
|   `**`  | Exponentiation           | `let result = 2 ** 8; //result ist 254`                       |
|   `/`   | Division                 | `let result = 2 / 4; //result ist 0.5`                        |
|   `%`   | Modulo                   | `let result = 24 % 7; //result ist 3`                         |
|   `++`  | Inkrement                | <code>let result = 5; </br> result++; //result ist 6</code> |
|   `--`  | Dekrement                | <code>let result = 5; </br> result--; //result ist 4</code> |








