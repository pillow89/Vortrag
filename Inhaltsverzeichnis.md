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
	<li><strong>modified</strong> &nbsp;&nbsp;&nbsp;-> geänderte Datei</li>
	<li><strong>stage</strong> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-> vorgemerkte Dateien</li>
	<li><strong>commited</strong> &nbsp;-> im lokalen Server gespeicherte Dateien</li>
</ul>

<h2 align="center">Git Ordnerstruktur und wichtige Befehle</h2>

<h3>Ordner</h3>
<ul>
	<li><strong>.git</strong> Unterverzeichnis mit allen relevanten</li>
	<li><strong>.gitignore</strong> Verzeichnis um Dateien und Ordner zu ignorieren</li>
</ul>

<code>
<h3>Hilfe und Status Funktionen</h3>
<ul>
	---- zeigt die Hilfe an ----
	<li><strong>$git help</strong></li>
	<li><strong>$git –help</strong></li> 
	<li><strong>$git help config</strong></li>
	---- 
	<li><strong>$git status</strong> --> zeigt den jetzigen Status an. Wurden Dateien verändert?</li>

</ul>

<h3>Branch Funktionen</h3>
<ul>

	<li><strong>$git init</strong> --> legt ein neues Repository an</li>
	<li><strong>$git branch</strong> --> zeigt an welche Branches vorhanden sind.</li>
	<li><strong>$git branch -d (name)</strong> --> löscht folgenden Branch</li>
	<li><strong>$git checkout (name)</strong> --> wechselt zu folgendem Branch</li>
	<li><strong>$git checkout -b (name)</strong> --> erstellt folgenden Branch</li>
	<li><strong>$git checkout -f </strong> --> setzt alle commited files zurück</li>
	
</ul>

<h3>Allgemeine Funktionen zum Entwickeln</h3>

<ul>
	<li><strong>$git pull origin master</strong> --> holt sich alle Informationen vom Server unter Branch master</li>
	<li><strong>$git add (filename)</strong> --> fügt Datei zum bevorstehenden commit hinzu. (. nimmt alle Dateien)</li>
	<li><strong>$git commit -am "message"</strong> --> schiebt alle zuvor hinzugefügten veränderte Dateien auf den lokalen Server</li>
	<li><strong>$git push origin (name)</strong> --> schiebt alle commited files zu diesem Branch auf den Server</li>
</ul>

</code>

<h2 align="center">Anwendungsbeispiele:</h2>

Zwei Programmierer bearbeiten ein Projekt. Programmierer A soll das Design
der index Seite verändern. Programmierer B soll die Logik verändern.
Als Resultat wird die erweiterte Indexpage entstehen.

Folgende Dateien sind vorhanden:

<pre>
Project/
	Grafik/
		index
		ersteSeite
	Module/
		indexModul
		ersteSeiteModul
</pre>


          

Programmierer A bearbeitet die Grafiken. Und verändert die indexseite.

<p align="center">
<pre>
$git add .
$git commit -am „changed the indexpage“
$git push origin BranchA
</pre>
</p>

Der Admin überprüft die Veränderung und merged es mit dem master

<pre>
$git merge -m „changed the indexpage“ BranchA
</pre>


Nun möchte Programmierer B in seinen Modulen etwas ändern, aber braucht die aktuelle Grafiken dazu:

<pre>
$git pull origin master
</pre>

Er verändert seine Dateien

<pre>
$git add .
$git commit -am „changed the indexmodule“
$git push origin BranchB
</pre>

Der Admin überprüft die Veränderung und merged

<pre>
$git merge -m „changed the indexmodule“ BranchB
</pre>


<h2>show</h2>

<ul>
	<li>create a repository</li>
	<li>clone a repository</li>
	<li>pull</li>
	<li>commit</li>
	<li>push</li>
	<li>set new branches</li>
	<li>advantages of creating new branches(switching very fast)</li>
	<li>merge</li>
	<li>conflict</li>
	<li>admin interface</li>
	<li>pull request</li>
	<li>history</li>
	<li>differences to svn</li> 
</ul>