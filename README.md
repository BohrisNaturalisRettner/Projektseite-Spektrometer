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

<p align="center"><img width="600" src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Aufbau%201.JPG"></p>


## Anschaltmechanismus<a name="3a"></a>

Angeschaltet wird das Spektrometer durch den Schalter an der Außenbox. dieser ist über einen Widerstand (STROMSTÄRKE SENKEN) mit einer blauen Led verbunden. Angeschossen ist das System an den 5V Anschluss (rot) des Arduino und eine Erdung (blau). Außerdem geht ein Kabel in den Analogen Anschluss 1 des Arduino (gelb)

<p align="center"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Anschalt%201.JPG" alt="image" width="600"></p>
<p align="center"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Anschalt%202.JPG" alt="image" width="600"></p>


## Maximaproduktion<a name="3b"></a>

Das Licht wird durch einen an den 3,3V Anschluss des Arduino angeschlossenen Laser produziert. davor befindet sich ein Gitter der Konstante 1/1.000.00.

<p align="center"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/MAxima%201.JPG" alt="image" width="600"></p>

Der Laser und das Gitter befinden sich auf einem „Holztisch“, welcher mit einem Winkel gehalten wird und werden durch Holz und Isolierband zusammengehalten. Dabei wird versucht den Laser möglichst senkrecht auf das Gitter auszurichten. Ein Winkel zwischen beiden Elementen, der auf den Holztische geschraubt ist, gibt die Ausrichtung vor und garantiert die senkrechte Position.

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Maxima%202.JPG" alt="image" width="420">   <img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Maxima%203.JPG" alt="image" width="420">


## Weniger Licht<a name="3c"></a>

Damit von außen weniger Licht unser Lichtverhältnis stört und damit der genauigkeit des Versuches schadet, befindet sich der ganze Versuch in einer Holzbox. Lichtquellen innerhalb dieserBox sind nach Möglichkeit mit Tape zugeklebt.

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Weniger%201.JPG" alt="image" width="420"> <img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Weniger%202.jpg" alt="image" width="420">


## Lichtmessung<a name="3d"></a>

Zur Lichtmessung ist ein Photosensor über einen Widerstand an die 5 V Ausgabe des Arduino angeschlossen.
Zusätzlich geht ein analoges Signal von dem Sensor in den Analogen Eingang 0 des Arduino.

<p align="center"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Lichtmessung%201.JPG" alt="image" width="700"></p>

Damit das Licht richtig gemessen werden kann, befindet sich der Sensor in einer Kabelbox um Licht von den anderen Seiten abzufangen. Die Kabel werden durch ein möglischst kleines Loch aus der Box geführt.


<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Lichtmessung%202.JPG" alt="image" width="420"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Lichtmessung%203.JPG" alt="image" width="420"> 

In Richtung des Lasers ist ein Rohr vor die Photozelle gesetzt, damit das Licht gebündelt aufgefangen werden kann. Der Eingang des Rohres ist mit einem Plastikdeckel und Klebeband zu einem Schlitz geformt, damit der Bereich des Lichtes so klein wie möglich ist. Das Rohr wird mit einem Holzstück vor der Photozelle in Position gehalten.

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Lichtmessung%205.JPG" alt="image" width="420"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Lichtmessung%204.JPG" alt="image" width="420">


## Bewegung<a name="3e"></a>

Um den Messapperat zu bewegen ist der unipolare Steppermotor „28BYJ-48“ über ein Motordriverboard an die Anschlüsse 8-11 des Arduino geschlossen, über die er die Informationen über die Bewegung erhält. Die 5V Stromversorung erhält der Steppermotor nicht über den Arduino sondern durch ein externes Kabel, das ebenfalls an das Driverboard angeschlossen ist.

<p align="center"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Bewegung%201.JPG" alt="image" width="800"></p>

<p align="center"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Bewegung%202%20STromversorgung.JPG" alt="image" width="600"></p>

<p align="center"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/BEwegung%203%20MotorDriverBoard.JPG" alt="image" width="600"></p>

Der Motor selbst ist auf zwei Holzblöcke mit dem Drehpunkt genau unter dem Gitter geschraubt. Die Holzblöcke sind durch einen Winkel mit der Bodenplatte verbunden.
Die Motorwelle ist über eine Zange mit dem Dreharm verbunden, sodass dieser sich bei Drehung des Motors mitdreht.

<p align="center"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/BEwegung%204%20Motorhalter.JPG" alt="image" width="600"></p>

Der Dreharm besteht aus einer Metallplatte, an die die Zange befestigt ist, um die Drehung zu übertragen. Das Ende der Platte befindet sich auf einem Rad, um möglichst wenig Reibung zu erzeugen.

<p align="center"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/BEwegung%205.JPG" alt="image" width="600"></p>

Links von dem Dreharm befindet sich ein Winkel, um die Startposition des Drehapperates festzulegen.

<p align="center"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/BEwegung%206.JPG" alt="image" width="600"></p>

Ein weiterer Dünner Winkel ist auf den Dreharm gesteckt. An ihm ist der Messapperat mit Tape angebracht, so dass dieser sich bei Drehung des Motors dreht.

<p align="center"><img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/BEwegung%207.JPG" alt="image" width="600"></p>
  

## Anzeige<a name="3f"></a>

Um am Ende das Ergebnis auszulesen, gibt es den Monitor im Arduino Editor. Um einfach nur zu sehen ob der Versuch erfolgreich war, dienen eine rote und eine grüne LED an der Außenwand der Box.

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Anzeige%201.JPG" alt="image" width="420">  <img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/Anzeige%202.JPG" alt="image" width="420">

Die LEDs sind an die Ausgänge 12 und 13 des Arduino und jeweils über einen 100 &Omega; Widerstand an eine gemeinsame Erdung angeschlossen.

<img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/ANzeige%203.JPG" alt="image" width="420"> <img src="https://github.com/BohrisNaturalisRettner/Projektseite-Spektrometer/blob/master/ANzeige%204.JPG" alt="image" width="420">


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

Funktionsweise



Beim Anschalten durch den Schalter, wird der Stromkreislauf geschlossen. Dadurch leuchtet die blaue LED und zeigt somit an, dass das System eingeschaltet ist. Zusätzlich ist wie vorher erwähnt ein Kabel an den analogen Anschluss A1 geschlossen. Fließt Strom an dieser Stelle kein Strom ist das Signal gleich 0. Fließt Strom, wird ein Signal größer als 0 aufgenommen. Daher gibt es in der Loop Funktion vor allem 2 Bereiche. 1. Den Bereich A1=0 und den Bereich A1>0. wird A1 größer als 0 wahrgenommen, fängt eine Variable in der Loop Funktion hochzuzählen. Das sind die „steps“. Gleichzeitig beginnt sich der Motor und damit auch der Dreharm und der daran festgemachte Lichtapperat zu drehen.
durch die gleichförmige bewegung des motors ist in diesem Versuch steps eine anzeige für zeit und Schritte. Da sich der Drehpunkt des Motors genau unter dem Gitter befindet, kann so aus der Stepanzahl auch der Winkel berechnet werden.

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

Dieser misst dabei das von dem laser emitierte Licht, dass durch das Gitter mit 1000 Striche pro mm fällt. an diesem Gitter bilden sich nach dem Huygenschen Prinzip neue Elementarwellen, die sich kreisförmig ausbreiten - Das Licht wird gebeugt.
bild huygensches Prinzip

Durch die verschiedeen Richtungen der Wellen, interferieren sie miteinadner. Dabei werden die Auslenkungen der Wellen an jedem Punkt addiert. Entscheident für den Phasenunterschied der Wellen ist der Gangunterschied. Wenn der Gangunterschied eine ganze Wellenlängenanzahl beträgt, trifft immer ein Berg auf einen Berg und ein Tal auf ein Tal und es gibt somit die maximale Auslenkung. Es herrscht konstruktive Interferenz. Der Gangunterschied beträgt immer: g*sina.
Skizze gangunterschied

Da für konstruktive Interferenzen der gangunterschcied eine ganze Anzahl an Wellenlängen betragen muss, gilt also nlamda= g* sina. Dementsprechend gibt es für eine Wellenlänge nur bestimmte Winkel in denen konstruktive Interferenz herrscht. In den Restlichen Winkeln löschen sich die Wellen destruktiv aus. In unserem Versuch beträgt die Wellenlänge des Lasers 350nm. Es befindet sich also ein Maximum erster Ordnung bei a= °. dieses ist auch in beide Richtungen im Kasten klar zu sehen.

Bild Maxima
In diesem Versuch wird dieser Winkel des ersten Maximums gemessen und daraufhin Rückschlüsse auf die Wellenlänge des Lasers gezogen.

der Lichtsensor misst dauerhaft die Lichtintensität durch den Photoelektrischen Effekt, auf den wir an dieser Stelle aber nicht weiter eingehen. jedoch gibt es eine Spannungsveränderung im Stromkreislauf, die mit dem Kabel in den Analogen Eingang 0 Weitergegeben wird. so wird mit dem befehl

```
int sensorPin = A0;
int sensorValue = 0;

loop
sensorValue = analogRead(sensorPin); // read the value from the sensor
```

mit jedem durchlauf die Lichtintensität gemessen. der Motor dreht sich nun wie gesagt. durch die counter wird die zeitliche komponente mit dem Lichtsignal verknüpft. ein counter beschreibt zum beispiel:
wenn also in diesem zeitlichen intervall ein erhötes Lichtsignal aufgenommen wird, wird der counter = eine höhere Zahl als 0 gesetzt. Diese bleiben so bis zum ende erhalten und können auch nachträglich ausgelesen werden. Die Anzahl der Steps die eine ganze Umdrehung des Motors dauert ist als STEPsPEROUTREV/4 festgehalten und beträgt 512 steps.

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
counter67 = 67;
}
if (66 < steps && 68 > steps) {
counter68 = 68;
}
if (67 < steps && 69 > steps) {
counter69 = 69;
}
if (68 < steps && 70 > steps) {
counter70 = 70;
}
```

Wenn die Anzahl der Steps = STEPS PEROUTREV/16 also = 128 ist, hat sich der Motor um 90 ° gedreht und dreht sich nun in die gegenrichtung

```
if (sensorValue2 > 0) {
if (STEPS_PER_OUT_REV / 8 > steps && STEPS_PER_OUT_REV / 16 <= steps) {
steppermotor.step(-StepsRequired);
steps = steps + 1;
}
```

Für den Versuch sind aber nur die ersen 90° entscheident, da der Sensor in diesem Bereich das Maximum schon einmal durchläuft. für jeden der 128 steps gibt es einen counter, der am ende anzeigt, dass in diesem bereich mehr licht gemssen wurde.

wenn steps= SPETSPER OUT REV/8 befindet sich der Motor wieder in der Ausgangsposition und die Geschwidnigkeit auf 0 gesetzt. Die grüne und die rote LED zeigen nun an ob der Versuch funktioniert hat. Leuchtet die gründe Led heißt das, dass in einem Bereich von 10% Abweichng nahc oben und nach unten für die korrekte Wellenlänge eine erhöhte Lichtintensität gemessen wurde. Leuchtet die rote LED, wurde in dem Bereich um dieses Intervall kein Ausschlag gemessen. Leuchten beide ist also sichergestellt, dass Licht in dem Bereich aufgenommen wurde und somit kein fehler in der Bewegung vorliegt und dass auch der ichtsensor richtig kalibriert ist und er nicht mit einer zu geringen oder zu hohen Sensibilität eingestellt wurde.

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

will man die genauen Messwerte erhalten muss man aber den Monitor im Editor benutzen. Der einfachheit halber werden die counter auf den wert gesetzt, wecher counter sie sind. Sprich wird im Bereich von counter 69 ein Signal aufgeommen beträgt der wert des counters 69. diese werte werden sowie die steos anzahl und die Lichtintensität im Monitor angezeigt.

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

So muss man aber nicht mehr durchzählen welcher counter ausgelöst wurde sondern kann glleich die zahl auslesen. da die counter bei counter1 =0 steps beginnen muss der counterbetrag - 1 gerechnet werden um die stepanzahl zu erhalten. die 90° Bewegung sind in 128 steps aufgeteilt sodass sich der Faktor 90/128 ergibt um die stepanzahl in die Gradzahl umzuwandeln. Mit der oben erarbeiteten Formel kann durch einsetzen des Winkels a die aus dem gemessenen Winkel resultierende Wellenlänge lamda errechnen.

Beendet wird der Versuch indem der Schalter wieder umgelegt wird. wenn das Signal bei A1=0 ist und die Stepanzahl bei 256 (STEWOS/8) erlöschen alle LEDs und alle counter werden zurückgesetzt. Nun kann durch erneutes Umlegen des Schalters der Versuch von neuem beginnen.

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
