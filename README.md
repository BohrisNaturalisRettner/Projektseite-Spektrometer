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

## Warum haben wir uns für ein optisches Spektrum als Projekt entschieden?<a name="1b"></a>

# 2. Der Aufbau<a name="2"></a>

  
  Anschalten
  - Schalter (5V)
  - blaues Licht zur Bestätigung (5V)Analog 1
  
  Bewegung 
  - Motor mit Aufhängung und Stromversorgung
  - Motorboard Steuerung
  - Dreharm mit Zange 
  - Rad, Stopper 
  -> Code
  
  Licht
  - Laser (3,3V an Arduino) mit Holzplattenhalterung (Winkel) 
  - Gitter über Drehpunkt (Tisch mit Winkel)
  
  LIcht aufnehmen
  - Photosensor(Analog0 und Widerstände) in Box auf Dreharm 
  - Rohr mit Spalt (Holzplattenbefestigung) 
  
  Anzeige 
  - 2LED (12,13 mit Widerstände) an Arduino nach außen



# 3. Die Funktionsweise<a name="3"></a>


## Funktionsweise

Der Laser is an den 3.3V Anschluss des Arduino angeschlossen. Das emittierte Licht ist monochromatisch und fällt durch das Gitter mit 1000 Strichen pro mm. Das Licht wird durch das Huygensche Prinzip gebrochen und interferiert nach dem Gitter. Es entsteht ein Hauptmaximum und links und rechts davon jeweils ein Maximum erster Ordnung (Gangunterschied = nlamda).Mit dem Spektrometer messen wir nun diesen Winkel und bestimmen damit die Wellenlänge des Lichtes des Lasers. Zum messen dient ein Photorsensor, der die Lichteinstrahlung als analoges Signal an den Arduino weitergibt. Der Lichtsensor befindet sich auf einem Dreharm, der von einem Steppermotor konstant gedreht wird. Der Sensor bewegt sich also in konstanter Winkelgeschwindigkeit um 90° von dem Hauptmaximum aus und durchläuft damit ein Nebenmaximum. Damit das Ergebnis genauer ist, befindet sich eine Rhe mit zwei Schlitzen vor dem Sensor, damit nur ein kleiner Bereich des Lichtes einfällt. Im Arduino fällt nun die Information der Zeit mit der Lichtintensität zusammen. Je nachdem in welcher Zeit die Lichtintensität ein gewisses Maß überschreitet, merkt sich der Arduino durch eine Variable diese Stelle. Diese können durch den Monitor angezeigt und so ausgelesen werden. Eingeteilt ist das Intervall in 2x 128 schritte. Da es sich dabei um 90° pro Weg handelt können die Schritte x90/128 gerechnet werden um den Winkel zu erhalten. Mit der Bragg Gleichung lässt sich aus sin() von dem Winkel x die Gitterkonstante 1/1000000 die Wellenlänge des Lichtes errechnen. In unserem finalen Aufbau beleuchten wir den Versuch von der anderen Seite und überprüfen die Funktionsweise unseres Versuches, indem wir mit dem Literaturwert der Wellenlänge (350nm) die Counter bestimmen die die korrekte Wellenlänge ergeben würden. Somit leuchtet die eine Led wenn der Bereich getroffen wurde und die andere wenn außerhalb des Bereiches kein erhöter Lichtausschlag gemessen wurde. Leuchten also beide Lampen war der Versuch erfolgreich.
