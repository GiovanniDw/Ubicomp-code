## Introductie
Na het installeren van Arduino en het aansluiten van de hardware kun je op deze plek voorbeelden vinden van kant en klare code. Hierboven zie je twee verschillende setjes code: "Basics-components" en "Basics-interactions". Onder Basics-interactions staat voorbeeldcode waarbij combinaties zijn gemaakt tussen sensoren en actuatoren (output). Wil je een andere sensor gebruiken of meersere soorten output aan een sensor hangen? Dan kun je code gebruiken uit 'basics-components'. In de code voorbeelden staat ook hoe je de sensoren en actuatoren (output) kunt aansluiten. Wil je een sensor herkennen? Dan kun je hieronder een verwijzing vinden met het overzicht van alle sensoren.

![](https://github.com/harmsel/Ubicomp-code/blob/main/imagesGit/board.png)

### Installeren arduino Mac
Volg deze HELLO WORLD video: https://youtu.be/C6NZ1WOGFKw 
Let op: sommige Arduino boards hebben een rode led in plaats van een groene

### Installeren arduino windows
Soms herkent windows je arduino board niet en moet je, na het volgen van deze video: https://youtu.be/C6NZ1WOGFKw onderstaand artikel doornemen: https://electronics-project-hub.com/arduino-not-detected-and-driver-issues-solved/.


### Installeren van libraries
Sommige sensoren of actuatoren gebruiken libraries om de code eenvoudiger leesbaar te houden. Als dit nodig is staat dat in de voorbeeldcode. Het installeren van een library doe je zo:

Ga naar Sketch > Include Library > Manage Libraries…

![](https://github.com/harmsel/Ubicomp-code/blob/main/imagesGit/libman1.png)

Zoek naar de naam van je component of library

![](https://github.com/harmsel/Ubicomp-code/blob/main/imagesGit/libman2.png)


* Klik “install” (voor onze projecten is de versie niet van groot belang)
* Sluit Library Manager
* Check of je de library echt hebt toegevoegd:
* Ga naar File > Examples
* Scroll helemaal naar beneden
* Controleer of er voorbeelden bij zijn gekomen met de naam van je sensor of actuator

### Sensoren
Afstand sensor

![Afstand sensor](https://m.media-amazon.com/images/I/51ugwbd5ynL._SL160_.jpg)

Servo

![](https://silicio.mx/media/catalog/product/cache/1/small_image/195x195/5e06319eda06f020e43594a9c230972d/r/o/rob08211p/Grove---Servomotor-21.jpg)

Led strip

![](https://i1.wp.com/www.esp8266learning.com/wp-content/uploads/2016/09/neopixel.jpg)

Lichtsensor

![](https://www.filipeflop.com/wp-content/uploads/2017/08/9SS88_1-180x180.jpg)

Temperatuur en luchtvochtigheid
![](https://github.com/harmsel/Ubicomp-code/blob/main/imagesGit/temphu.png)

Blauwe LED en Drukknop
![](https://github.com/harmsel/Ubicomp-code/blob/main/imagesGit/ledknop.png)

Accelerometer - Bewegingsmeter
![](https://github.com/harmsel/Ubicomp-code/blob/main/imagesGit/acceler.png)

Een apart document met alle sensoren: https://docs.google.com/document/d/1kRWXyL-nMneFP8WJKPnR6a4RMJA-kljxb1RygZhN2KE/edit#

### Fouten oplossen

#### Code uploaden lukt niet
Krijg je na het uploaden onderstaande melding in de  oranje balk?

![](https://docs.m2stud.io/cs/arduino/images/%28Arduino_Tutorials%29_Arduino_Upload_Fail.png)


1. Open een lege sketch (File > New) en upload deze lege sketch 
2. Ga naar tools > Port
3. Selecteer de juiste Port ”/dev/cu.usbserial**’MAC of com (Windows) 
4. Staat deze Port er niet bij? Ruil dan je hardware (en kabel) even met je Buur
5. Je kunt ook proberen de Arduino opnieuw aan je Laptop aan te sluiten (als je geen buur hebt)
6. Kijik nogmaals naar https://youtu.be/C6NZ1WOGFKw ) 


##### Andere foutmelding (code problemen)
Upload een lege sketch. Krijg je in de oranje balk "Problem Uploading..." dan is het een probleem met verbinden/drivers. Krijg je een andere foutmelding dan zit het probleem in de Sketch (code).
Kijk rondom welke regel het fout gaat (is roze en regel staat in de foutmelding)
De meeste foutmeldingen gaan over fout plaatsen van { of } en een regel die niet eindigd met ;
