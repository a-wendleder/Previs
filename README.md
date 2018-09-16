# Previs

Knuth Möde\
Akademischer Mitarbeiter Szenografie/VFX\
Filmuniversität Potsdam Babelsberg

# Lösungsentwurf für ein VR gestütztes Pre-Visualisierungssystem (VIVE, Unreal Umgebung) im kreativen Kontext der Filmuniversität

Im Folgenden soll der Versuch unternommen werden ein System der Pre-Visualisierung zu erschaffen welches möglichst viele Aspekte der realen Filmproduktion am Set berücksichtigt.
Es handelt sich hierbei um eine Sammlung von Rechercheergebnissen Ideen und Fragestellungen.
Ziel sollte sein eine möglichst komplette Simulation der Drehumgebung zu erschaffen, die hilft,  ökonomische, künstlerische und organisatorische Probleme zu lösen. Oder zu erleichtern. Grundvoraussetzung ist die Zusammenarbeit infrage kommender Studienzweige um die Anforderungen der jeweiligen Fachrichtungen erfüllen zu können. Es könnte eine Plattform geschaffen werden aus der jeder einen Mehrwert ziehen kann.
Zur allgemeinen Erklärung: der die Bediener/in steht im virtuellen Set und bewegt und steuert mit Hilfe der Controller seine Umgebung. Er/Sie kann sich dabei frei im Raum bewegen und mit der Umgebung interagieren. Der User/in ist dabei nicht an die Schwerkraft gebunden und kann sich mittels „beamen“ an jede Stelle und Höhe im Set bewegen. Die Controller dienen dabei als Zeige- und Bewegungswerkzeug.
Die Benutzung des Systems von zwei Usern/innen gleichzeitig ist möglich. Durch die Einbindung des resultierenden Bildes aus der VR-Umgebung in eine Online-Umgebung wäre es möglich im Team zu arbeiten.
Im Einzelnen geht es um die möglichst Wirklichkeitsnahe Simulation von:
Licht, Kamera (Optik), Rigs, Set-Teilen, gescannter Setarchitektur sowie Standin's von Schauspielern

## Recherche:
* Welche Elemente einer Location lassen sich unter welchen Einschränkungen erschaffen
* Welche Möglichkeiten gibt es, bestehende Drehlocations (sets und props) in die VR-Umgebung zu integrieren (Laserscans, Photogrammetrie, in 3D Software erstellte Props)
* Welche Rendermethodik sollte verwendet werden um die Darstellung möglichst fotorealistisch zu erstellen (GI, PBR unter Echtzeitbedingungen)

## Programmieraufwand:
* Ermittlung der Methoden zur „instant“ Importierung von sets und props
* Autmatische Erstellung von Geometrie aus gescannten Punktwolken
* Automatsche Erstellung von Albedo-, Normal- und Specular Texturen sowie deren Zuweisung der neu erstellten Geometrie
* Welche Methoden gibt es ermittelte Bemaßungen aus der realen Welt in die virtuelle Umgebung zu übernehmen
* Welche automatischen Bemaßungstechniken gibt es im VR-Raum (es sollte eine intuitive Möglichkeit gefunden werden Bemaßungen im VR Editor zu erstellen und zu ändern
* Eine einfache Platzierung der einzelnen Elemente im VR Raum sollte durch 3D Raster und selbstdefinierte Hilfslinien möglich sein
* Interaktive Umschaltung von metrisch auf angloamerikanisches System
* Erstellung von ausblendbaren Konstruktions- und Bemaßungs-Layern sollte möglich sein
* Oben genanntes System würde eine „Durchdringung“ von Bauelementen sowie Lichtern, Rigs und Kameras  automatisch verhindern
* Möglichkeit des Imports von Geometrie und entsprechenden Texturen / Shadern (OSL) aus Maya oder anderen 3D Programmen
* Angestrebt werden sollte eine komplett interaktive Arbeitsumgebung im VR Editor nach automatischem Import von Geometrie und dazugehörigen Texturen und Shadern
* Wichtig ist die intuitive Benutzerführung des Anwenders durch eine klare Erstellungspipeline zur Vermeidung von Fehlern (“Wizard-Guide“)
* Möglichkeit des Imports von Vector oder Raster basierten Konstruktionsplänen und Grundrissen zur Platzierungshilfe sowie der Export von Plänen die durch die Anordnung von Setelementen und Props entstanden sind (Schnittdarstellung in allen Koordinatenachsen durch das Set incl. Bemaßungen

## Kamera:

* Darstellung von gebräuchlichsten Kameramodellen und zugehörigen Rigs inklusive der Simulation von Freiheitsgraden dazugehöriger Stative, Dolly etc. (Recherche im Studiengang Kamera über Einsatz und Leistung verschiedener Objektive und digitaler Aufnahmverfahren
* Möglichkeit der Einblendung von Storyboards zum Szenen basierten Arbeiten
* Simulation der Kameraoptik und interaktiver Arbeit mit Blenden und Brennweiten
* „Virtueller Blick“ durch den Viewfinder incl. Interaktion      
* Möglichkeit des „Einleuchtens“ durch den Sucher der Kamera (GI Lichtsimulation, Interaktion mit Scheinwerfern)
* Möglichkeit der Platzierung von Set-Elementen unter Berücksichtigung von Brennweite und Bildausschnitt
* Aus jedem User/in-Blickwinkel im Set sollte sich per Knopfdruck eine virtuelle Kamera erstellen lassen
* Tiefenschärfesimulation
* Entfernungsmessung und Speicherung durch den Sucher
* Animation und Speicherung von Kamerabewegungen zur Weitergabe an die VFX (unter zu Hilfenahme moderner Roboter- und oder Rig-Lösungen (motion control, stop motion)

## Beleuchtung:

* Recherche der gängigsten Beleuchtungsmittel am Set
* Für jeden Beleuchtungskörper sollten entsprechende Stative und Traversen vorhanden sein, die durch ein einfaches „point and click“ Verfahren im Raum platziert werden können
* Die Beleuchtungsstärke (Lichtausbeute, Wattzahl) sollte dabei den realen Scheinwerfern so nahe wie möglich sein um eine realistisch anmutende Ausleuchtung des sets zu gewährleisten
* Speicherung verschiedener Lichtsetups zum Test im virtuellen Studio
* Es sollte die Möglichkeit bestehen alle Lichtpositionen und Typen abzuspeichern, um diese dann als Tabelle oder Zeichnung an das Lichtdepartment weitergeben zu können
* Durch die erhaltenen Informationen lässt sich auch eine noch genauere Lichtsimulation „offline“ erstellen welche unter zu Hilfenahme eines Pathtracers erreicht werden könnte (Arnold, Octane, Maxwell, Vray) die Hires-Lichtsimulation kann dann wieder als „gebakte Texturlösung) in den VR Raum zurückgeführt werden
* Ein Vorteil ist die Möglichkeit der Übergabe von erarbeiteten und getesteten Lichtdaten an das VFX Department
* Auch eine Berechnung der nötigen Watt-Zahl ist möglich
* Die Darstellung von Reflektoren und Gobos 
* Durch den Einsatz von vorher aufgenommenen HDRI´s ist auch der Test von verschiedenen Tageslicht- und Uhrzeit-Situationen möglich
* Der „Blick“ durch den zu setzenden Spot würde die Lichtgestaltung erheblich vereinfachen
* Auch eine „reverse“ Lichtsetzung währe nur in dieser virtuellen Umgebung möglich (s.h. ein virtueller Belichtungsmesser wird am zu beleuchtenden Objekt angebracht und die gewünschte Helligkeit eingestellt – die Scheinwerfer werden entsprechend automatisch platziert und in ihrer Stärke justiert

## Datennutzung, -auswertung, -aufarbeitung:
Am Ende des Prozesses steht die logische Weiterführung des Systems, nämlich die Auswertung und Nutzung der gewonnenen Daten. Es bestehen mehrere Möglichkeiten mit den gewonnenen Setdaten am realen Set weiterzuarbeiten :

* AR-Einspielung direkt vor Ort mit Hilfe von iPad, iPhone, HoloLens, Magic Leap würde eine große Hilfe bei der Set-Einrichtung -Konstruktion bieten (setzen von Markern mit Hilfe in VR gewonnener Proportionen und Abmessungen
* Mit Hilfe eines Beamers ließen sich voreingestellte Kameraperspektiven in den realen Raum projezieren um die virtuellen Platzierungsdaten der Geometrie anzuzeigen (incl. Dargestellter Bemaßung)
* Baupläne und Rißzeichnungen ständen für Weiterbearbeitung verschiedener Gewerke und in Szenografie zur Verfügung
* Ein 3D Abgrenzungsgitter ließe sich einblenden um den Schauspielern im green screen eine erleichterte Bewegung im nichtvorhandenen Set zu erleichtern (bei später in der VFX erstelltem set) 
* Eine Zuspielung des aufgenommen virtuellen Sets in die reale Kamera beim Dreh um Positionierungen zu überprüfen

Stand September 2018
