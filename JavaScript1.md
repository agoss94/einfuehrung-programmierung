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
	  	console.log("Hallo Welt!");
	  </script>
	</body>
	</html>
	
Wenn wir nun in den Developer Tools die Konsole aufrufen, dann könenn wir dort unsere Textausgabe sehen. Mit Hilfe des `window.alert("Hallo Welt!");` Befehls könenn wir uns den Text auch direkt in einem Popup Fenster anzeigen lassen. Gratulation wir haben unser erstes JavaScript Programm geschrieben!
