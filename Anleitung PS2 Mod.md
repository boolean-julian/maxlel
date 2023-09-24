# Aufrüsten einer PS2 zum Betrieb mit einer Festplatte
## Vorwort
Alles Gute zum Geburtstag, lieber Max! Du hattest dir ja eine Anleitung für einen PS2 Mod gewünscht und die sollst du auch kriegen. Du benötigst lediglich eine Fat PS2, aber die hast du ja. Ich weiß nicht, ob grundsätzlich alle Modelle gehen. Ansonsten brauchst du noch einen Schraubenzieher (SL reicht aus). Wenn du es richtig ernst meinst, kannst du natürlich noch paar andere Dinge modden, z.B. den Fan, oder deine PS2 auch mal von innen reinigen, aber das ist ganz dir überlassen. Wie für ältere Geräte üblich: Für einige Menschen ist das ein "blank canvas".

> Information: Die PS2 benutzt ein proprietäres Festplattenformat. Wenn du dachtest, dass du Dateien und Ordner mit Drag and Drop auf das Gerät schieben kannst, dann muss ich dich hier leider enttäuschen. Dafür haben wir den HDL Batch Installer. Das wird dann erklärt, wenn es Zeit dafür ist.

## 1. Materialbeschaffung
Zunächst einmal brauchen wir einen Haufen China-Müll.
![](https://i.ibb.co/xYHbg3d/photo1695572012.jpg)
### 1.1. AliExpress - Hardware für die PS2
#### 1.1.1. Memory Card 64MB mit FMCB v1.966 mit OPL für die PS2
FreeMCBoot (FMCB) wird benötigt, um die PS2 mit einer anderen Firmware zu booten, die es erlaubt die Software OpenPS2Loader (OPL) zu starten. OPL wird benötigt um Spiele über den IDE Bus zu laden, statt wie üblich über das DVD-Laufwerk. Grundsätzlich kann man auch seine eigene Memory Card modden, aber das ist eher aufwändig und birgt wenig Mehrwert, da man sowieso ein paar Teile bestellen muss und das hier das günstigste ist. 

>* Kostenpunkt ca. 5€
>* Beispiel: https://de.aliexpress.com/item/1005004259245989.html?spm=a2g0o.cart.0.0.591e4ae4APPYDB&mp=1&gatewayAdapt=glo2deu

#### 1.1.2. IDE auf SATA Adapter für die PS2
Mit der PS2 kann man im Netzwerk spielen. Dafür wurde ein damals standardmäßiger Anschluss benutzt -- IDE. Sony wollte bisschen extra Mula machen und hat eine überteuerte Netzwerkkarte (IDE auf RJ45) verkauft. Durch frei verfügbare Leiterplattendesigns der Modcommunity kann man statt des mittlerweile antiken IDE einen heute standardmäßigen SATA Anschluss benutzen. Auf AliExpress finden sich für ein solches Bauteil mit Case unzählige und willige Halsabschneider. Der Leistungsflaschenhals auf der PS2 ist der IDE-Bus, das heißt du erwartest keinen Leistungsschub durch dieses Bauteil. Aber immerhin kannst du viel leichter und schneller Spiele auf die Festplatte schieben.

>* Kostenpunkt ca. 20€.
>* Beispiel: https://de.aliexpress.com/item/1005006008849774.html?spm=a2g0o.cart.0.0.591e4ae4APPYDB&mp=1&gatewayAdapt=glo2deu

### 1.2. Amazon: Hardware für den Computer
#### 1.2.1. Interne SSD
Hier schlafen deine Spiele nachts. Die hier ist vielleicht Overkill, aber damit ist bisschen gemütlicher, weil sie echt schnell ist. 
>* Kostenpunkt ca. 20€ bis 100€
>* Beispiel: https://www.amazon.de/gp/product/B0B7VM4SRX/ref=ox_sc_act_title_1?smid=A3JWKAKR8XB7XF&psc=1

#### 1.2.2. USB C auf SATA Adapter
Um Spiele vom Computer auf die PS2 Festplatte zu ziehen
>* Kostenpunkt ca. 15€ bis 20€
>* Beispiel: https://www.amazon.de/gp/product/B00D1E6RMW/ref=ox_sc_act_title_1?smid=A3JWKAKR8XB7XF&psc=1

## 2.	FMCB Test an der PS2
1.	Falls vorhanden: DVD aus dem Laufwerk entfernen 
2.	Memory Card mit FMCB in Memory Card Slot 2 stecken
3.	PS2 einschalten
4.	Gucken ob es geglückt ist

> Siehst du etwas andere Menüoptionen als im üblichen Bildschirm, hat es geklappt. Ansonsten probiere einen Reset, Netzteil an/aus oder normales Ausschalten

## 3. Beschaffung von Spielen bzw. Images
1. Mach einen Account auf https://startgame.world/
2. Mach dir einen 1fichier Premium Account
3. Guck hier https://startgame.world/sony-playstation-2/
3. Enjoy

## 4. Installation "HDL Batch Installer" auf dem Computer
1.	HDL Batch Installer herunterladen und ihm was spenden wenn du es auch so toll findest wie ich
    * Download: https://github.com/israpps/HDL-Batch-installer/releases
	* Spende: https://www.paypal.com/paypalme/ElisraPS2
2. Entpacken und da speichern wo du installierte Programme speicherst
3. Ausnahme hinzufügen für Antivirus (direkter Zugriff auf Festplattenformate die Windows nicht kennt)

Für den Windows Defender geht Schritt 3 so (Standard Antivirus in Win11):
 1. "Start" 
 2. "Windows Sicherheit" suchen & Anklicken
 3. "Viren und Bedrohungsschutz"
 4. "Einstellungen verwalten" unter "Einstellungen für Viren- und Bedrohungsschutz"
 5. Ganz runter scrollen, "Ausschlüsse" und den Ordner hinzufügen unter dem du HDL Batch Installer gespeichert hast

## 5. Vorbereiten der Festplatte
![](https://i.ibb.co/wWvWxHR/Bild-2023-09-24-182045142.png)
1. SSD Festplatte anschließen mit dem SATA/USB Adapter
2. Jegliche Optionen die Windows dir als Autostart anbietet vermeiden
3. HDL-Batch-installer.exe starten
4. Festplatte formatieren:
	* "Main" 
	* "Format HDD"
	* Extrem wichtig: Die PS2 Festplatte identifizieren und auswählen
	* "Format" > "Ja" > "Ja" > "Ja" > "Ja" > "OK"
5.	Überprüfen mit "Search ps2 HDDs":
	* Wenn eine gefunden wird, ist dir alles geglückt!
	* Es wird eine gefunden, wenn rechts daneben etwas im Drop-Down-Menü erscheint
	* Bei mir steht dann da "hdd2:"

## 6. Installation von Spielen
1. Im HDL Batch Installer unter dem "Install"-Reiter kannst du "Search Games" anklicken
2. Wähle dann alle Spiele aus, die du installieren willst. Integritätsprüfung dauert
3. "Install" -- Das dauert je nach Menge eine ganze Weile.
4. (Optional) Überprüfe Liste der Spiele unter dem Reiter "Browse"
5. Schließen und das Medium auswerfen (wie bei einem USB Stick)

## 7. Hardwareinstallation
1.	Netzteil auf 0, alle Kabel abklemmen
2.	Memory Card mit FMCB in Memory Card Slot 2 stecken
3.	SSD in IDE/SATA Adapter stecken
4.	IDE/SATA Adapter in den IDE Slot der PS2 stecken und festschrauben
5.	PS2 an Strom und Bildschirm anschließen, Netzteil einschalten

![](https://i.ibb.co/pb4nD8T/123.jpg)

## 8.	Benutzung
1.	Die fertig zusammengebaute PS2 wie in Sektion 3 ("FMCB Test an der PS2") hochfahren
2.	OpenPS2Loader (OPNPS2LD) auswählen
3.	Was aus der Spieleliste aussuchen und spielen!
4.	Spätere Installation von Spielen:
	1. 	Festplatte ausbauen und am PC anschließen
	2.	HDL Batch Installer starten
	3.	"Search ps2 HDD's", unter "Browse" gucken ob alles gut ist
	4.	Wie vorher eigentlich weiter installieren
5.  Ausschalten wie gehabt!

## 9.	Sonstiges
### 9.1.	Fan Mod
Einige PS2 Modelle sind ganz schön laut, darunter meins. Online gibt's unzählige Tutorials wie man das beheben kann.
	
### 9.2	SSD Mounting Bracket
Die SSD hängt da recht lose in der PS2 wie du sicherlich feststellen wirst, hat bei mir aber nie Probleme gegeben, da das Eigengewicht der 2.5" SSD ein paar Gramm beträgt. Wenn du eine 3.5" SSD einbaust, könnte es sein, dass du so eine Mounting Bracket kaufen musst. Gibt es auch bei AliExpress.

### 9.3 Mehr Software
Die PS2 Community hat einen recht großen Softwarestack geschaffen. Leider ist nicht alles kompatibel miteinander, also ist alles mit großer Vorsicht zu genießen. Du kannst zB deinen Spielen auch Metadaten (Cover Art, Beschreibung, ...) hinzufügen. Ist aber egal für jetzt.