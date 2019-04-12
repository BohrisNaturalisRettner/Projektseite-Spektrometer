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
* ### [Warum haben wir uns für ein optisches Spektrometer als Projekt entschieden?](#1b)
</details> <hr>

## [2. Der Arduino](#2)
<details>
  <summary>Genauer</summary>

* ### 
* ### 
</details> <hr>

## [3. Der Aufbau](#3)
<details>
  <summary>Genauer</summary>
  
* ### [Anschaltmechanismus](#3a)
* ### [Maximaproduktion](#3b)
* ### [Weniger Licht](#3c)
* ### [Lichtmessung](#3d)
* ### [Bewegung](#3e)
* ### [Anzeige](#3f)
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

## Warum haben wir uns für ein optisches Spektrometer als Projekt entschieden?<a name="1b"></a>


# 2. Der Arduino<a name="2"></a>


# 3. Der Aufbau des Spektrometers<a name="3"></a>

Den Aufbau des Spektrometers erläutern wir anhand der folgenden sechs Bereiche:
- Anschaltmechanismus, 
- Maximaproduktion, 
- Abschirmung von anderen Lichtquellen
- Messen der Lichtintensität, 
- Bewegung des Lichtmessers und 
- Anzeige der Ergebnisse.

<p align="center"><img width="600" src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Aufbau%201.JPG"></p>


## Anschaltmechanismus<a name="3a"></a>

Angeschaltet wird das Spektrometer durch einen Schalter an der Außenbox. Dieser ist über einen Widerstand (STROMSTÄRKE SENKEN) mit einer blauen LED verbunden. Das System ist an den 5V Anschluss (rot) des Arduino und eine Erdung (blau) angeschlossen. Außerdem führt ein Kabel in den analogen Anschluss 1 des Arduino (gelb).

<p align="center"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Anschalt%201.JPG" alt="image" width="600"></p>
<p align="center"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Anschalt%202.JPG" alt="image" width="600"></p>


## Maximaproduktion<a name="3b"></a>
d
Das Licht wird durch einen Laser produziert, der mit dem 3,3V Anschluss des Arduino verbunden ist. Vor dem Laser befindet sich ein Gitter der Konstante 1/1.000.00.

<p align="center"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/MAxima%201.JPG" alt="image" width="600"></p>

Der Laser und das Gitter werden durch Holz und Isolierband zusammengehalten und sind auf einem „Holztisch“ installiert, der durch einen Winkel gehalten wird. Bei dem Aufbau wurde darauf geachtet, den Laser möglichst senkrecht auf das Gitter auszurichten. Hierfür sorgt ein Winkel zwischen beiden Elementen, der auf den Holztisch geschraubt ist. Dieser gibt die Ausrichtung vor und garantiert die senkrechte Position.

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Maxima%202.JPG" alt="image" width="420">   <img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Maxima%203.JPG" alt="image" width="420">


## Abschirmung von anderen Lichtquellen<a name="3c"></a>

Damit möglichst nur das Licht des Lasers aufgezeichnet wird und Lichtquellen von außen die Versuchsergebnisse so wenig wie möglich beeinflussen, befindet sich der Versuchsaufbau in einer Holzbox. Lichtquellen innerhalb dieser Box sind nach Möglichkeit mit Tape zugeklebt.

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Weniger%201.JPG" alt="image" width="420"> <img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Weniger%202.jpg" alt="image" width="420">


## Messen der Lichtintensität<a name="3d"></a>

Zur Lichtmessung ist ein Photosensor über einen Widerstand an die 5 V Ausgabe des Arduino angeschlossen.
Zusätzlich geht ein analoges Signal von dem Sensor in den analogen Eingang 0 des Arduino.

<p align="center"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Lichtmessung%201.JPG" alt="image" width="700"></p>

Damit das Licht richtig gemessen werden kann, befindet sich der Sensor in einer Kabelbox, was wiederum dem Ziel dient, störende andere Lichtquellen abzuschirmen. Aus dem gleichen Grund werden die Kabel  durch ein möglischst kleines Loch aus der Box geführt.


<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Lichtmessung%202.JPG" alt="image" width="420"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Lichtmessung%203.JPG" alt="image" width="420"> 

In Richtung des Lasers ist ein Rohr vor die Photozelle gesetzt, dessen Eingang mit einem Plastikdeckel und Klebeband zu einem Schlitz geformt ist, damit der Bereich des Lichteinfalls so klein wie möglich ist. Das Rohr wird mit einem Holzstück vor der Photozelle in Position gehalten.

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Lichtmessung%205.JPG" alt="image" width="420"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Lichtmessung%204.JPG" alt="image" width="420">


## Bewegung des Lichtmessers<a name="3e"></a>

Um den Messapperat zu bewegen, ist der unipolare Steppermotor „28BYJ-48“ über ein Motordriverboard an die Anschlüsse 8-11 des Arduino angeschlossen, über die die Bewegungsinformationen an den Motor gegeben werden. Die 5V Stromversorung erhält der Steppermotor nicht über den Arduino, sondern durch ein externes Kabel, das ebenfalls an das Driverboard angeschlossen ist.

<p align="center"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Bewegung%201.JPG" alt="image" width="800"></p>

<p align="center"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Bewegung%202%20STromversorgung.JPG" alt="image" width="600"></p>

<p align="center"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/BEwegung%203%20MotorDriverBoard.JPG" alt="image" width="600"></p>

Der Motor selbst ist in der Weise auf zwei Holzblöcke geschraubt, dass sich der Drehpunkt genau unter dem Gitter befindet. Die Holzblöcke sind durch einen Winkel mit der Bodenplatte verbunden.
Die Motorwelle ist mittels einer Zange an dem Dreharm befestigt, sodass dieser sich bei Drehung des Motors mitdreht.

<p align="center"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/BEwegung%204%20Motorhalter.JPG" alt="image" width="600"></p>

Der Dreharm besteht aus einer Metallplatte, an der die Zange befestigt ist (s.o.), und einem Rad unter dem Ende der Metallplatte, das der Vermeidung von Reibung dient.

<p align="center"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/BEwegung%205.JPG" alt="image" width="600"></p>

Links von dem Dreharm befindet sich ein Winkel, um die Startposition des Drehapperates festzulegen.

<p align="center"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/BEwegung%206.JPG" alt="image" width="600"></p>

Ein weiterer dünner Winkel ist auf den Dreharm gesteckt. An ihm ist der Messapperat mit Tape angebracht, so dass dieser sich bei Drehung des Motors dreht.

<p align="center"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/BEwegung%207.JPG" alt="image" width="600"></p>
  

## Anzeige der Ergebnisse<a name="3f"></a>

Eine rote und eine grüne LED an der Außenwand der Box dienen der Information darüber, ob der Versuch erfolgreich durchgeführt wurde. Das genaue Ergebnis der Lichtmessung wird in dem Monitor im Arduino Editor angezeigt. 

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Anzeige%201.JPG" alt="image" width="420">  <img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Anzeige%202.JPG" alt="image" width="420">

Die LEDs sind an die Ausgänge 12 und 13 des Arduino und jeweils über einen 100 &Omega; Widerstand an eine gemeinsame Erdung angeschlossen.

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/ANzeige%203.JPG" alt="image" width="420"> <img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/ANzeige%204.JPG" alt="image" width="420">


# 4. Die Funktionsweise<a name="4"></a>

## Funktionsweise und Code<a name="4d"></a>

Durch das Betätigen des Schalters wird der Stromkreislauf geschlossen. Dadurch leuchtet die blaue LED, die somit anzeigt, dass das System eingeschaltet ist. Zusätzlich ist, wie vorher erwähnt, ein Kabel an den analogen Anschluss A1 angeschlossen. Fließt an dieser Stelle kein Strom ist das Signal gleich 0. Fließt Strom, wird ein Signal größer als 0 aufgenommen. Daher gibt es in der Loop-Funktion insbesondere zwei Bereiche: Zum einen den Bereich A1=0 und zum anderen den Bereich A1>0. Wird A1 größer als 0 wahrgenommen, beginnt eine Variable in der Loop Funktion hochzuzählen. Das sind die „steps“. Gleichzeitig beginnen sich der Motor und damit auch der Dreharm und der daran festgemachte Lichtmessapparat zu drehen.
Durch die gleichförmige Bewegung des Motors lassen sich in diesem Versuch anhand der "steps" Zeit und Weg der Bewegung des Dreharms bestimmen. Da sich der Drehpunkt des Motors genau unter dem Gitter befindet, kann so aus der Stepanzahl auch unmittelbar der Drehwinkel berechnet werden.

```
int sensorPin2 = A1;
int sensorValue2 = 0;

#include

// Define Constants

// Number of steps per internal motor revolution
const float STEPS_PER_REV = 32;

// Amount of Gear Reduction
const float GEAR_RED = 64;

// Number of steps per geared output rotation
const float STEPS_PER_OUT_REV = STEPS_PER_REV * GEAR_RED;

// Define Variables

// Number of Steps Required
int StepsRequired;
int steps = 0;

// Create Instance of Stepper Class
// Specify Pins used for motor coils
// The pins used are 8,9,10,11
// Connected to ULN2003 Motor Driver In1, In2, In3, In4
// Pins entered in sequence 1-3-2-4 for proper step sequencing

Stepper steppermotor(STEPS_PER_REV, 8, 10, 9, 11);

loop
StepsRequired = 4;
if (sensorValue2 > 0) {
if (steps < STEPS_PER_OUT_REV / 16) {
steppermotor.setSpeed(25);
steppermotor.step(StepsRequired);
steps = steps + 1;
}

sensorValue2 = analogRead(sensorPin2);
```

Der Lichtmessapparat misst während seiner Bewegung das Interferenzmuster des Laser-Lichtes, welches durch das Gitter mit 1000 Strichen pro mm entsteht.

In unserem Versuch beträgt die Wellenlänge des Lasers &lambda; = 650nm. Es befindet sich also ein Maximum erster Ordnung bei 
α = 40,54°. Dieses ist auch in beiden Richtungen im Kasten klar sichtbar.

//Bild Maxima

In diesem Versuch wird eben dieser Winkel des ersten Maximums bestimmt und daraus Rückschluss auf die Wellenlänge des Lasers gezogen.

Der Lichtsensor misst dauerhaft die Lichtintensität durch den photoelektrischen Effekt, auf den wir an dieser Stelle aber nicht weiter eingehen. Eine Änderung der Lichtintensität wird durch eine Spannungsveränderung im Stromkreislauf an den analogen Anschluss A0 weitergegeben. So wird mit dem Befehl

```
int sensorPin = A0;
int sensorValue = 0;

loop
sensorValue = analogRead(sensorPin); // read the value from the sensor
```

in jedem Durchlauf die Lichtintensität gemessen. Durch "counter" werden die zeitliche Komponente und das Lichtsignal verknüpft. Ein "counter" beschreibt zum Beispiel:


```
int counter1;
int counter2;

…

int counter128;
int counter129;

loop
if (sensorValue > 620) {
if (43 < steps && 45 > steps) {
counter45 = 45;
}
if (44 < steps && 46 > steps) {
counter46 = 46;
}
if (45 < steps && 47 > steps) {
counter47 = 47;
}
if (46 < steps && 48 > steps) {
counter48 = 48;
}
…
if (64 < steps && 66 > steps) {
counter66 = 66;
}
if (65 < steps && 67 > steps) {
counter67 = 67;if (66 < steps && 68 > steps) {
counter68 = 68;
}
if (67 < steps && 69 > steps) {
counter69 = 69;
}
if (68 < steps && 70 > steps) {
counter70 = 70;
}
```

Wenn also in diesem zeitlichen Intervall ein erhöhtes Lichtsignal über einer festen Schwelle von 620 aufgenommen wird, wird der counter gleich einer höheren Zahl als 0 gesetzt. Diese bleiben so bis zum Ende erhalten und können auch nachträglich noch ausgelesen werden. Die Anzahl der steps, die der Motor für eine ganze Umdrehung benötigt, ist dadurch, dass der Motor bei einem step intern vier SChritte geht, als "STEPsPEROUTREV/4" festgehalten und beträgt 512 steps.

Wenn die Anzahl der steps = STEPS PEROUTREV/16 also = 128 ist, hat sich der Motor um 90 ° gedreht und dreht sich daraufhin in die Gegenrichtung zurück.

```
if (sensorValue2 > 0) {
if (STEPS_PER_OUT_REV / 8 > steps && STEPS_PER_OUT_REV / 16 <= steps) {
steppermotor.step(-StepsRequired);
steps = steps + 1;
}
```

Für den Versuch ist aber nur der "Hinweg" entscheidend, da der Sensor in diesem Bereich das Maximum schon einmal durchlaufen hat. Auf dem "Rückweg" findet keine Messung statt. 
Für jeden der 128 steps der ersten 90° des Hinwegs gibt es einen Counter. Am Ende des Rückwegs werden alle diejenigen Counter mit ihrem Wert angezeigt, bei denen der Sensorwert von 620 überschritten wurde und somit dort ein Maximum liegt. 

Wenn steps= STEPSSPEROUTREV/8 ist, befindet sich der Motor wieder in der Ausgangsposition und die Geschwindigkeit des Motors wird auf 0 gesetzt. An der grünen und der roten LED kann man nun den Erfolg des Versuch ablesen: Leuchtet die rote LED, bedeutet dies, dass in einem Bereich von 10% Abweichung nach oben und nach unten von der Wellenlänge eine erhöhte Lichtintensität gemessen wurde. Leuchtet die grüne LED, wurde im Umfeld dieses Intervalls keine erhöhte Intensität wahrgenommen. Leuchten beide, ist also sichergestellt, dass Licht nur in diesem Intervall aufgenommen wurde und somit kein Fehler in der Bewegung vorliegt und dass auch der Lichtsensor auf die richtige Sensibilität kalibriert ist. Man hat also ein Resultat mit einer Abweichung von höchstens 10% von dem Literaturwert erreicht. 
```
int ledrot = 12;
int ledgruen = 13;

loop

if (sensorValue2 > 0) {
if (steps >= STEPS_PER_OUT_REV / 8) {
steppermotor.setSpeed(0);
if (counter52 == 52 || counter53 == 53 || counter54 == 54 || counter55 == 55 || counter56 == 56 || counter57 == 57 || counter58 == 58 || counter59 == 59 || counter60 == 60 || counter61 == 61 || counter62 == 62 || counter63 == 63 || counter64 == 64 || counter65 == 65) {
digitalWrite(ledrot, HIGH);
}
if (counter50 == 0 || counter51 == 0 || counter66 == 0 || counter67 == 0) {
digitalWrite(ledgruen, HIGH);
}
}
}
```

Um die genauen Messwerte zu erfahren, muss man den Monitor im Arduino Editor benutzen. Der Einfachheit halber werden die counter auf den Wert ihrer Position gesetzt. Zum Beispiel: Wird im Bereich von counter 69 ein Signal aufgenommen, beträgt der Wert des counters ebenso 69. Diese Werte werden sowie die Anzahl der steps und die Lichtintensität am Photosensor im Monitor angezeigt.

```
setup
Serial.begin(9600); //sets serial port for communication

setup

Serial.println(steps);
Serial.println(sensorValue);//prints the values coming from the sensor on the screen
Serial.println(counter44);
Serial.println(counter45);
Serial.println(counter46);

…

Serial.println(counter69);
Serial.println(counter70);
Serial.println(counter71);
```

Hierdurch muss man nicht mehr durchzählen, welcher counter ausgelöst wurde, sondern kann gleich die Zahl des counters auslesen. Da die counter bei counter1 = 0 steps beginnen, muss vom Counterbetrag 1 abgezogen werden, um die Stepanzahl zu erhalten. Die 90° Bewegung findet in 128 steps statt, sodass sich der Faktor 90/128 ergibt, um von der Stepanzahl auf die Gradzahl der Drehung zu kommen. Mit der eingangs erarbeiteten Formel kann durch Einsetzen des Winkels α die aus dem gemessenen Winkel resultierende Wellenlänge &lamda; errechnet werden.

Beendet wird der Versuch, indem der Schalter wieder umgelegt wird. Wenn das Signal bei A1=0 und die Stepanzahl bei 256 (STEPSPEROUTREV/8) ist, erlöschen alle LEDs und sämtliche counter werden zurückgesetzt. Nun kann durch erneutes Umlegen des Schalters der Versuch von Neuem beginnen.

```
if (sensorValue2 == 0 && steps >= STEPS_PER_OUT_REV / 8) {
steps = 0;
digitalWrite(ledrot, LOW);
digitalWrite(ledgruen, LOW);
counter1 = 0;
counter2 = 0;
counter3 = 0;
counter4 = 0;
…
counter126 = 0;
counter127 = 0;
counter128 = 0;
}
```


## Beispielversuch<a name="4e"></a> 

Im Folgenden werden ein Versuch und seine Auswertung beschrieben, wie er mit unserem Spektrometer durchgeführt wurde. 


### Versuchsdurchführung<a name="4a"></a>

Vor der eigentlichen Durchführung des Versuches werden einige Vorbereitungen getroffen. Zum einen wird der Arduino an den Computer über das USB Typ-B-Kabel angeschlossen, um im Arduino Editor das Monitoring aufzurufen. Außerdem wird die Stromversorgung des Motors über eine Steckdose hergestellt. Zusätzlich dazu wird sichergestellt, dass der Dreharm sich wirklich auf der Ausgangsposition bei 0° befindet. Zuletzt wird die Box wieder "lichtdicht" verschlossen. Nach Abschluss dieser Vorbereitungen wird der Versuch begonnen.

Dafür wird lediglich der Schalter auf der Vorderseite umgelegt. Die blaue Leuchte beginnt zu leuchten. Am Ende des Versuchs zeigen die rote und grüne LED den erfolgreichen Abschluss des Versuchs an. Im Monitor werden nun die Counter 59 & 60 als Ausschläge ausgewiesen. 

// Bild/Video Versuch Schalter und LED 


### Versuchsnachbereitung / Resultat<a name="4c"></a>

Zur Auswertung der Counter wird zunächst der Durchschnitt der ausgeschlagenen Counter berechnet. Dieser beträgt bei unserem Versuch mit dem Laser 59,5. Dieser Wert wird in eine vorbereitete Excel-Tabelle eingetragen, die automatisch den Winkel des Ausschlags und daraus die Wellenlänge des Lasers berechnet. Zusätzlich dazu wird die Abweichung vom Literaturwert der Wellenlänge des Lasers berechnet. Bei einem Durchschnitt vom 59,5 beträgt der Winkel 41,13° und somit die Wellenlänge &lambda; = 657,8nm. Damit hat unser Wert eine Abweichung von 1,2% vom Literaturwert &lamba; = 650nm. 

// Bild ExcelTabelle und Monitor

