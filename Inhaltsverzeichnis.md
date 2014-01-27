<h1 align="center">Git</h1>


<h2 align="center">Was ist Git und warum sollte man es benutzen?</h2>

<p>
	Git ist ein Versionskontrollprogramm, welches genutzt wird um Projekte besser zu koordinieren.
	Da große Projekte mit vielen Mitarbeitern sehr schwer zu überschauen sind, ist es notwendig den Überblick zu behalten.
</p>

<p>
Mit Git ist es möglich, viele Prozesse gleichzeitig verwalten zu können.
Es gibt exakte Zugriffsrechte. Eine große History, die anzeigt, welche Person welche Dateien verändert hat und auch wann.
</p>

<p>
<strong>Wichtige Punkte zu Git:</strong>
<ul>
	<li>Geschwindigkeit</li>
	<li>Einfaches Design</li>
	<li>Gute Unterstützung von nicht-linearer Entwicklung (tausende paralleler Branches, d.h. verschiedener Verzweigungen der Versionen)</li>
	<li>Vollständig verteilt</li> 
	<li>Fähig, große Projekte wie den Linux Kernel effektiv zu verwalten (Geschwindigkeit und Datenumfang)</li>
</ul> 
</p>
<h2 align="center">Git Grundlagen</h2>
<p>
Git speichert lokal. Damit alles schnell geht speichert es bei commits nur veränderte Dateien. Und lädt jene auch zum Server hoch. Also nicht das komplette Projekt sondern nur Snapshots.
</p>

<p>
Der lokale Server reicht aus um alle Veränderungen überprüfen zu können. Man muss also nicht auf den externen Server zugreifen.
</p>

<h2 align="center">Sicherheit</h2>

Jeder commit wird verschlüsselt in einem 
40 Zeichen HashTag SHA-1 <br>
Beispiel: <strong>24b9da6552252987aa493b52f8696cd6d3b00373</strong>

<h2 align="center">Zustände der Dateien</h2>
<ul>
	<li>modified</li>
	<li>stage</li>
	<li>commited</li>
</ul>

<h2 align="center">Git Befehle</h2>

<ul>

	<li><strong>$git help</strong></li>
	<li><strong>$git –help</strong></li> 
	<li><strong>$git help config</strong></li>
	<li><strong>$git init</strong></li>

.git Unterverzeichnis mit allen relevanten 

	<li><strong>$git branch</strong></li>
	<li><strong>$git branch -d <name></strong></li>
	<li><strong>$git checkout -b <name></strong></li>
	<li><strong>$git pull origin master</strong></li>
	<li><strong>$git push origin <name></strong></li>

</ul>

Anwendungsbeispiele:

Zwei Programmierer bearbeiten ein Projekt.

Folgende Dateien sind vorhanden:

Project/
	Grafik/
		index
		ersteSeite
	Module/
		indexModul
		ersteSeiteModul


          

Programmierer A bearbeitet die Grafiken. Und verändert die indexseite.

<p align="center">
$git add .
$git commit -am „changed the indexpage“
$git push origin BranchA
</p>

Der Admin überprüft die Veränderung und merged es mit dem master

$git merge -m „changed the indexpage“ BranchA


Nun möchte Programmierer B in seinen Modulen etwas ändern, aber braucht die aktuelle Grafiken dazu:

$git pull origin master

Er verändert seine Dateien

$git add .
$git commit -am „changed the indexmodule“
$git push origin BranchB

Der Admin überprüft die Veränderung und merged

$git merge -m „changed the indexmodule“ BranchB
