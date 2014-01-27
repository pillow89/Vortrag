<h1 align="center">Git</h1>


<h2>Was ist Git und warum sollte man es benutzen?</h2>

Git ist ein Versionskontrollprogramm, welches genutzt wird um Projekte besser zu koordinieren.
Da große Projekte mit vielen Mitarbeitern sehr schwer zu überschauen sind, ist es notwendig den Überblick zu behalten.

Mit Git ist es möglich, viele Prozesse gleichzeitig verwalten zu können.
Es gibt exakte Zugriffsrechte. Eine große History, die anzeigt, welche Person welche Dateien verändert hat und auch wann.

Wichtige Punkte zu Git:
Geschwindigkeit 
Einfaches Design 
Gute Unterstützung von nicht-linearer Entwicklung (tausende paralleler Branches, d.h. verschiedener Verzweigungen der Versionen) 
Vollständig verteilt 
Fähig, große Projekte wie den Linux Kernel effektiv zu verwalten (Geschwindigkeit und Datenumfang) 

Git Grundlagen

Git speichert lokal. Damit alles schnell geht speichert es bei commits nur veränderte Dateien. Und lädt jene auch zum Server hoch. Also nicht das komplette Projekt
Snapshots

Der lokale Server reicht aus um alle Veränderungen überprüfen zu können. Man muss also nicht auf den externen Server zugreifen.

Sicherheit

40 Zeichen HashTag SHA-1

Zustände
stage, commited, modified

Git Befehle.

$git help
$git –help 
$git help config

$git init

.git Unterverzeichnis mit allen relevanten 

$git branch
$git branch -d <name>

$git checkout -b <name>

$git pull origin master
$git push origin <name>

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

$git add .
$git commit -am „changed the indexpage“
$git push origin BranchA

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
