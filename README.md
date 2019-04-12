# Projektseite Spektrometer
von Tim Wähner und David Rettmann                                                                                              
Stormarnschule Ahrensburg                                                                                                              
Klasse 12e                                                                                                                             
Schuljahr 2018/19                                                                                                                      
                                                                                                                                      
                                                                                                                                       
# Inhalt 

## [1. Das Spektrometer](#1)
<details>
  <summary>Genauer</summary>
  
* ### [Was ist ein (optisches) Spektrometer?](#1a)
* ### [Warum haben wir uns für ein optisches Spektrum als Projekt entschieden?](#1b)
</details> <hr>

## [2. Der Arduino](#2)
<details>
  <summary>Genauer</summary>

* ### Funktion pipapo
* ### usw
</details> <hr>

## [3. Der Aufbau](#3)
<details>
  <summary>Genauer</summary>
  
* ### [Anschalten](#3a)
* ### [Bewegung](#3b)
* ### [Licht](#3c)
* ### [Lichtmessung](#3d)
* ### [Anzeige](#3e)
</details> <hr>

## [4. Die Funktionsweise](#4)
<details> 
  <summary>Genauer</summary>
  
* ### [Funktionsweise und Code](#4d) 
* ### [Beispielversuch:](#4e)                                                                                          
  + #### [Versuchsdurchführung](#4a)
  + #### [Versuchsnachbereitung / Resultat](#4c)
 </details> <hr>

# 1. Das Spektrometer<a name="1"></a>

## Was ist ein optisches Spektrometer?<a name="1a"></a>

Ein optisches Spektrometer dient der Wellenlängenbestimmung von Licht einer unbekannten Wellenlänge &lambda;. Dazu wird diese an einem Gitter gebeugt. Die entstandenen Elementarwellen interferieren miteinander und es entsteht ein von der Wellenlänge &lambda; abhängiges Interferenzmuster. Das Spektrometer dient nun der Bestimmung der Winkel in denen die Maxima auftreten, aus denen man schlussendlich die Wellenlänge des Lichts errechnen kann. 

## Warum haben wir uns für ein optisches Spektrometer als Projekt entschieden?<a name="1b"></a>


# 2. Der Arduino


# 3. Der Aufbau des Spektrometers<a name="3"></a>

Das Spektrometer setzt sich aus 6 Komponenten zusammen. Dem Vorgang zum Anschalten, dem Produzieren von den Maxima, der Abdunklung anderer Lichtquellen, dem Messen der Lichtintensität misst, der Bewegung des Lichtmessers und der Anzeige der Ergebnisse.

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Aufbau%201.JPG" alt="image" width="1500">


## Anschaltmechanismus<a name="3a"></a>

Angeschaltet wird das Spektrometer durch den Schalter an der Außenbox. dieser ist über einen Widerstand mit einer blauen Led verbunden. Angeschossen ist das System an den 5V Anschluss (rot) des Arduino und eine Erdung (blau). Außerdem geht ein Kabel in den Analogen Anschluss 1 des Arduino (gelb)

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Anschalt%201.JPG" alt="image" width="1500">

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Anschalt%202.JPG" alt="image" width="1500">


## Maximaproduktion<a name="3b"></a>

Das Licht wird durch einen an den 3,3V Anschluss des Arduino angeschlossenen Laser produziert. davor befindet sich ein Gitter der Konstante 1/1.000.00.

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/MAxima%201.JPG" alt="image" width="1500">

Der Laser und das Gitter befinden sich auf einem „Holztisch“, welcher mit einem Winkel gehalten wird und werden durch Holz und Isolierband zusammengehalten. Dabei wird versucht den Laser möglichst senkrecht auf das Gitter auszurichten. Ein Winkel zwischen beiden Elementen, der auf den Holztische geschraubt ist, gibt die Ausrichtung vor und garantiert die senkrechte Position.

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Maxima%202.JPG" alt="image" width="1500">

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Maxima%203.JPG" alt="image" width="1500">


## Weniger Licht<a name="3c"></a>

Damit von außen weniger Licht unser Lichtverhältnis stört und damit der genauigkeit des Versuches schadet, befindet sich der ganze Versuch in einer Holzbox. Lichtquellen innerhalb dieserBox sind nach Möglichkeit mit Tape zugeklebt.

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Weniger%201.JPG" alt="image" width="1500">

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Weniger%202.jpg" alt="image" width="1500">


## Lichtmessung<a name="3d"></a>

Zur Lichtmessung ist ein Photosensor über einen Widerstand an die 5 V Ausgabe des Arduino angeschlossen.
Zusätzlich geht ein analoges Signal von dem Sensor in den Analogen Eingang 0 des Arduino.

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Lichtmessung%201.JPG" alt="image" width="1500">

Damit das Licht richtig gemessen werden kann, befindet sich der Sensor in einer Kabelbox um Licht von den anderen Seiten abzufangen.

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Lichtmessung%202.JPG" alt="image" width="1500">

Die Kabel werden durch ein möglischst kleines Loch aus der Box geführt.

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Lichtmessung%203.JPG" alt="image" width="1500">

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Lichtmessung%204.JPG" alt="image" width="1500">

In Richtung des Lasers ist ein Rohr vor die Photozelle gesetzt, damit das Licht gebündelt aufgefangen werden kann. Der Eingang des Rohres ist mit einem Plastikdeckel und Klebeband zu einem Schlitz geformt, damit der Bereich des Lichtes so klein wie möglich ist. Das Rohr wird mit einem Holzstück vor der Photozelle in Position gehalten.

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Lichtmessung%205.JPG" alt="image" width="1500">


## Bewegung<a name="3e"></a>

Um den Messapperat zu bewegen ist der unipolare Steppermotor „28BYJ-48“ über ein Motordriverboard an die Anschlüsse 8-11 des Arduino geschlossen, über die er die Informationen über die Bewegung erhält. Die 5V Stromversorung erhält der Steppermotor nicht über den Arduino sondern durch ein externes Kabel, das ebenfalls an das Driverboard angeschlossen ist.

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Bewegung%201.JPG" alt="image" width="1500">

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Bewegung%202%20STromversorgung.JPG" alt="image" width="1500"> (Untertitel Stromversorgung)

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/BEwegung%203%20MotorDriverBoard.JPG" alt="image" width="1500"> (Untertitel Motor Driverboard)

Der Motor selbst ist auf zwei Holzblöcke mit dem Drehpunkt genau unter dem Gitter geschraubt. Die Holzblöcke sind durch einen Winkel mit der Bodenplatte verbunden.
Die Motorwelle ist über eine Zange mit dem Dreharm verbunden, sodass dieser sich bei Drehung des Motors mitdreht.

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/BEwegung%204%20Motorhalter.JPG" alt="image" width="1500">

Der Dreharm besteht aus einer Metallplatte, an die die Zange befestigt ist, um die Drehung zu übertragen. Das Ende der Platte befindet sich auf einem Rad, um möglichst wenig Reibung zu erzeugen.

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/BEwegung%205.JPG" alt="image" width="1500">

Links von dem Dreharm befindet sich ein Winkel, um die Startposition des Drehapperates festzulegen.

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/BEwegung%206.JPG" alt="image" width="1500">

Ein weiterer Dünner Winkel ist auf den Dreharm gesteckt. An ihm ist der Messapperat mit Tape angebracht, so dass dieser sich bei Drehung des Motors dreht.

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/BEwegung%207.JPG" alt="image" width="1500">


## Anzeige<a name="3f"></a>

Um am Ende das Ergebnis auszulesen, gibt es den Monitor im Arduino Editor. Um einfach nur zu sehen ob der Versuch erfolgreich war, dienen eine rote und eine grüne LED an der Außenwand der Box.

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Anzeige%201.JPG" alt="image" width="1500">

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Anzeige%202.JPG" alt="image" width="1500">

Die LEDs sind an die Ausgänge 12 und 13 des Arduino und jeweils über einen 100 &Omega; Widerstand an eine gemeinsame Erdung angeschlossen.

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/ANzeige%203.JPG" alt="image" width="1500">

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/ANzeige%204.JPG" alt="image" width="1500">


# 4. Die Funktionsweise<a name="4"></a>

## Funktionsweise und Code<a name="4d"></a>






## Beispielversuch<a name="4e"></a> 

Im Folgenden wird ein Versuch und seine Auswertung beschrieben wie er mit unserem Spektrometer durchgeführt werden kann. 

### Versuchsdurchführung<a name="4a"></a>

Vor der eigentlichen Durchführung des Versuches müssen einige Vorbereitungen getroffen werden. Zum einen muss der Arduino an den Computer über das USB Typ-B-Kabel angeschlossen werden, um im Arduino Editor das Monitoring aufzurufen. Außerdem gilt es die Stromversorgung des Motors über eine Steckdose herzustellen. Zusätzlich dazu muss sichergestellt werden, dass der Dreharm sich wirklich auf der Ausgangsposition bei 0° befindet. Zuletzt gilt es die Box wieder "lichtdicht" zu verschließen. Sind all diese Faktoren gegeben kann der Versuch begonnen werden.
Dafür wird lediglich der Schalter auf der Vorderseite umgelegt. Leuchtet nun die blaue Leuchte, läuft der Versuch. Er gilt als beendet und erfolgreich, wenn die rote und grüne LED leuchten. Im Monitor werden nun die Counter 59 & 60 angegeben als Ausschläge. 

// Bild/Video Versuch Schalter und LED 

### Versuchsnachbereitung / Resultat<a name="4c"></a>

Zur Auswertung der Counter wird zunächst der Durchschnitt der ausgeschlagenen Counter berechnet. Dieser beträgt bei unserem Versuch mit dem Laser 59,5. Dieser Wert wird in eine vorbereitete Excel-Tabelle eingetragen, die automatisch den Winkel des Ausschlags und daraus die Wellenlänge des Lasers berechnet. Zusätzlich dazu wird außerdem die Abweichung vom Literaturwert der Wellenlänge des Lasers berechnet. Bei einem Durchschnitt vom 59,5 beträgt der Winkel 41,13° und somit die Wellenlänge &lambda; = 657,8nm. Damit hat unser Wert eine Abweichung von 1,2% vom Literaturwert &lamba; = 650nm. 

// Bild ExcelTabelle und Monitor


## Funktionsweise

Der Laser is an den 3.3V Anschluss des Arduino angeschlossen. Das emittierte Licht ist monochromatisch und fällt durch das Gitter mit 1000 Strichen pro mm. Das Licht wird durch das Huygensche Prinzip gebrochen und interferiert nach dem Gitter. Es entsteht ein Hauptmaximum und links und rechts davon jeweils ein Maximum erster Ordnung (Gangunterschied = nlamda).Mit dem Spektrometer messen wir nun diesen Winkel und bestimmen damit die Wellenlänge des Lichtes des Lasers. Zum messen dient ein Photorsensor, der die Lichteinstrahlung als analoges Signal an den Arduino weitergibt. Der Lichtsensor befindet sich auf einem Dreharm, der von einem Steppermotor konstant gedreht wird. Der Sensor bewegt sich also in konstanter Winkelgeschwindigkeit um 90° von dem Hauptmaximum aus und durchläuft damit ein Nebenmaximum. Damit das Ergebnis genauer ist, befindet sich eine Rhe mit zwei Schlitzen vor dem Sensor, damit nur ein kleiner Bereich des Lichtes einfällt. Im Arduino fällt nun die Information der Zeit mit der Lichtintensität zusammen. Je nachdem in welcher Zeit die Lichtintensität ein gewisses Maß überschreitet, merkt sich der Arduino durch eine Variable diese Stelle. Diese können durch den Monitor angezeigt und so ausgelesen werden. Eingeteilt ist das Intervall in 2x 128 schritte. Da es sich dabei um 90° pro Weg handelt können die Schritte x90/128 gerechnet werden um den Winkel zu erhalten. Mit der Bragg Gleichung lässt sich aus sin() von dem Winkel x die Gitterkonstante 1/1000000 die Wellenlänge des Lichtes errechnen. In unserem finalen Aufbau beleuchten wir den Versuch von der anderen Seite und überprüfen die Funktionsweise unseres Versuches, indem wir mit dem Literaturwert der Wellenlänge (350nm) die Counter bestimmen die die korrekte Wellenlänge ergeben würden. Somit leuchtet die eine Led wenn der Bereich getroffen wurde und die andere wenn außerhalb des Bereiches kein erhöter Lichtausschlag gemessen wurde. Leuchten also beide Lampen war der Versuch erfolgreich.
