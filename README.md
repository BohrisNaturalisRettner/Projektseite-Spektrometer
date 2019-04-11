# Projektseite Spektrometer
von Tim Wähner und David Rettmann                                                                                              
Stormarnschule Ahrensburg                                                                                                              
Klasse 12e                                                                                                                             
Schuljahr 2018/19                                                                                                                      
                                                                                                                                      
                                                                                                                                       
# Inhalt 

## [1. Das Spektrometer](#1)
<details>
  <summary>Genauer</summary>
  
### [Was ist ein optisches Spektrometer?](#1a)

### [Warum haben wir uns für ein optisches Spektrum als Projekt entschieden?](#1b)

</details> <hr>

## [2. Der Arduino](#4)
<details>
  <summary>Genauer</summary>
  
</details> <hr>

## [2. Der Aufbau](#2)
<details>
  <summary>Genauer</summary>
  
### [Anschalten](#2a)
### [Bewegung](#2b)
### [Licht](#2c)
### [Lichtmessung](#2d)
### [Anzeige](#2e)

</details> <hr>

## [3. Die Funktionsweise](#3)
<details> 
  <summary>Beispielversuch</summary>
  
### [Versuchsvorbereitung](#3a)                                                                                          
### [Versuchsdurchführung](#3b)
### [Versuchsnachbereitung / Resultat](#3c)
 </details> <hr>

# 1. Das Spektrometer<a name="1"></a>

## Was ist ein optisches Spektrum?<a name="1a"></a>

Ein optisches Spektrum dient der Wellenlängenbestimmung einer einfallenden Strahlung. Dazu wird die Strahlung an einem Gitter gebrochen und bildet somit ein Interferenzmuster. Das Spektrometer dient nun der Winkelbestimmung der Maxima des Interferenzmusters. Aus den Winkeln der Maxima lässt sich so die Wellenlänge der Strahlung bestimmen und somit auch der Stoff, der die Strahlung emittiert hat. 

## Warum haben wir uns für ein optisches Spektrum als Projekt entschieden?<a name="1b"></a>


# 2. Der Aufbau<a name="2"></a>

## Anschalten<a name="2a"></a>

Will man das Spektrometer einschalten, während es für das Monitoring und die Stromversorgung an den Computer angeschlossen ist und die externe Stromversorgung über eine Steckdose gesichert ist, so genügt es den Schalter an der Vorderseite des Kastens, in dem sich der Aufbau befindet, zu betätigen. Daraufhin wird die blaue LED daneben als Bestätigung für das Laufen des Spektrometers leuchten. Sowohl Schalter als auch LED befinden sich in einem Stromkreis mit dem Arduino über den Anschluss "Analog 1" für die Signalübertragung, und den Anschluss "5V", über den der Stromkreis mit dem benötigten Strom versorgt wird. Vor der LED befindet sich selbstverständlich ein Widerstand. 

// Bild Schaltkreis, Bild aus Kasten

## Bewegung<a name="2b"></a>

Nachdem das Gerät über den Schalter eingeschaltet wurde, beginnt das Spektrometer eine kreisförmige Bewegung um 90° und wieder zurück.. Angetrieben wird der sich bewegende Schwenkarm über einen Steppermotor, der auf einem Holzaufbau befestigt ist, damit er sich auf der richtigen Höhe befindet. Der Motor wird gesteuert über einen Motor-Driver, der direkt am Holzaufbau sitzt und an den Arduino über die digitalen Anschlüssen 8-11 angeschlossen ist. Über den Motor-Driver läuft außerdem die externe Stromversorgung, die benötigt wird um den Motor zu betreiben, da der Arduino nicht in der Lage ist die benötigte Spannung zu liefern. 

// Bild Motor und Schaltkreis

Der Schwenkarm besteht aus einer länglichen Metallplatte, an dessen Ende ein Rad sitzt, dass eine sichere und stabile Drehung sicher stellt. Die Verbindung zur Motorwelle ist über eine Zange gesichert, welche ihrerseits mit Kabelbindern am Dreharm befestigt ist. Um stets sicherstellen zu können, dass der Schwenkarm bei 0° beginnt, da sonst das Messergebnis verfälscht werden würde, gibt in der Grundposition des Schwenkarms einen Winkel, der als Stopper dient. 

// Bild Schwenkarm(Zange), Bild Stopper 
  
## Licht <a name="2c"></a>

Das mit dem Spektrometer zu untersuchende Licht liefert in unserem Aufbau ein monochromatischer Laser, der an den 3,3V Anschluss des Arduino verbunden ist und ebenso wie der Motor über den Schalter aktiviert wird. Der Laser ist in einer Holzplatte befestigt, damit dieser fest steht. Ausgerichtet ist der Laser in Richtung des Schwenkarms, sodass der Laserstrahlung in Ruhestellung mittig über dem Schwenkarm steht. Zuvor passiert dieser ein Gitter, welches gemeinsam mit dem Laser und seiner Halterung an einem Winkel befestigt ist. Das Gitter muss dabei genau über dem Drehpunkt des Motors stehen. Zu diesem Zweck ist der Winkel mit Laser und Gitter auf einem kleinen "Tisch", der über dem Holzaufbau des Motors sitzt und an ihm mit weiteren Winkeln befestigt ist. 

// Bild Laser/Gitter, // Bild Stromkreis 

## Lichtmessung<a name="2d"></a>

Die Lichtmessung erfolgt am Ende des Schwenkarms mit ei Photosensor, der sich in einer Verteilerbox befindet, die auf dem Dreharm fest über einen Winkel sitzt, damit auch diese gerade ist. Der Photosensor selber ist über Widerstände an den "Analog 0" Anschluss des Arduino angeschlossen. Vor dem Photosensor befindet sich befestigt in einer Holzplatte ein kurzes Rohr mit einem Spalt an der Vorderseite.
  LIcht aufnehmen
  - Photosensor(Analog0 und Widerstände) in Box auf Dreharm 
  - Rohr mit Spalt (Holzplattenbefestigung) 
  
## Anzeige<a name="2e"></a>
  Anzeige 
  - 2LED (12,13 mit Widerstände) an Arduino nach außen

# 3. Die Funktionsweise<a name="3"></a>


## Funktionsweise

Der Laser is an den 3.3V Anschluss des Arduino angeschlossen. Das emittierte Licht ist monochromatisch und fällt durch das Gitter mit 1000 Strichen pro mm. Das Licht wird durch das Huygensche Prinzip gebrochen und interferiert nach dem Gitter. Es entsteht ein Hauptmaximum und links und rechts davon jeweils ein Maximum erster Ordnung (Gangunterschied = nlamda).Mit dem Spektrometer messen wir nun diesen Winkel und bestimmen damit die Wellenlänge des Lichtes des Lasers. Zum messen dient ein Photorsensor, der die Lichteinstrahlung als analoges Signal an den Arduino weitergibt. Der Lichtsensor befindet sich auf einem Dreharm, der von einem Steppermotor konstant gedreht wird. Der Sensor bewegt sich also in konstanter Winkelgeschwindigkeit um 90° von dem Hauptmaximum aus und durchläuft damit ein Nebenmaximum. Damit das Ergebnis genauer ist, befindet sich eine Rhe mit zwei Schlitzen vor dem Sensor, damit nur ein kleiner Bereich des Lichtes einfällt. Im Arduino fällt nun die Information der Zeit mit der Lichtintensität zusammen. Je nachdem in welcher Zeit die Lichtintensität ein gewisses Maß überschreitet, merkt sich der Arduino durch eine Variable diese Stelle. Diese können durch den Monitor angezeigt und so ausgelesen werden. Eingeteilt ist das Intervall in 2x 128 schritte. Da es sich dabei um 90° pro Weg handelt können die Schritte x90/128 gerechnet werden um den Winkel zu erhalten. Mit der Bragg Gleichung lässt sich aus sin() von dem Winkel x die Gitterkonstante 1/1000000 die Wellenlänge des Lichtes errechnen. In unserem finalen Aufbau beleuchten wir den Versuch von der anderen Seite und überprüfen die Funktionsweise unseres Versuches, indem wir mit dem Literaturwert der Wellenlänge (350nm) die Counter bestimmen die die korrekte Wellenlänge ergeben würden. Somit leuchtet die eine Led wenn der Bereich getroffen wurde und die andere wenn außerhalb des Bereiches kein erhöter Lichtausschlag gemessen wurde. Leuchten also beide Lampen war der Versuch erfolgreich.
