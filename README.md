## Introductie
Na het installeren van Arduino en het aansluiten van de hardware kun je op deze plek voorbeelden vinden van kant en klare code. Hierboven zie je twee verschillende setjes code: "Basics-components" en "Basics-interactions". Onder Basics-interactions staat voorbeeldcode waarbij combinaties zijn gemaakt tussen sensoren en actuatoren (output). Wil je een andere sensor gebruiken of meersere soorten output aan een sensor hangen? Dan kun je code gebruiken uit 'basics-components'. In de code voorbeelden staat ook hoe je de sensoren en actuatoren (output) kunt aansluiten. Wil je een sensor herkennen? Dan kun je hieronder een verwijzing vinden met het overzicht van alle sensoren.

![](https://github.com/harmsel/Ubicomp-code/blob/main/imagesGit/board.png)

### Installeren arduino Mac
Volg deze HELLO WORLD video: https://youtu.be/C6NZ1WOGFKw 
Let op: sommige Arduino boards hebben een rode led in plaats van een groene

### Installeren arduino windows
Volg deze video (voor Mac): https://youtu.be/C6NZ1WOGFKw, LET OP: windows vraagt je soms zaken goed te keuren (dit zie je niet in de video). 
Soms herkent windows je arduino board niet en moet je, na het volgen van deze video:  onderstaand artikel doornemen: https://electronics-project-hub.com/arduino-not-detected-and-driver-issues-solved/.


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

| naam | Sensor   | functie   |
| :---:   | :---: | :---: |
| Afstand sensor| ![Afstand sensor](https://m.media-amazon.com/images/I/51ugwbd5ynL._SL160_.jpg)  | Deze afstandsmeting stuurt een een ultrasoon geluidssignaal uit en ontvangt deze als het geluid weerkaatst is. De tijd tussen versturen en ontvangen is afhankelijk van de afgelegde weg van het geluidssignaal. Zo wordt de afstand tot het object berekend. Deze sensor zit ook in auto’s als parkeersensor. |
| Led Strip | ![](https://github.com/harmsel/Ubicomp-code/blob/main/imagesGit/ledstrip.png)   | Elke led kan je individueel aansturen in alle RGB kleuren. Er zit een plakrand aan zodat je hem makkelijk kunt verwerken in je project (dus beschadigen). Gebruik je deze plakrand of verwerkt je hem in je project? Dat geen probleem maar je moet hem dan kopen (5 euro per strip). Dan kunnen we nieuwe kopen voor de aankomende studenten |
| Lichtsensor | ![](https://github.com/harmsel/Ubicomp-code/blob/main/imagesGit/licht.png) | De Grove - lichtsensor heeft een analoge output. Hoe feller het licht is, des te hoger de waarde. Je sluit de lichtsensor aan op het A0 stekkertje. |
| Temp. en vocht | ![](https://github.com/harmsel/Ubicomp-code/blob/main/imagesGit/temphu.png)   | Deze meet de temperatuur van de lucht en de hoeveelheid vocht in de lucht. Test en demo de werking met blazen in de sensor, liever niet met een aansteker ;-)  |
| Blauwe LED en Drukknop | ![](https://github.com/harmsel/Ubicomp-code/blob/main/imagesGit/ledknop.png)    | Dit component bevat een LED lampje en een drukknop. Deze kun je onafhankelijk van elkaar aansturen of uitlezen.   |
| Accelerometer - Bewegingsmeter 1.5g | ![](https://github.com/harmsel/Ubicomp-code/blob/main/imagesGit/acceler1.5.png)  | LET OP! Zoek bij deze sensor de 1.5g code. Dit is een sensor die beweging en stand weergeeft over drie assen (x, y en z). Een soortgelijke sensor zit ook in je telefoon. Je kunt ‘m ook programmeren om gebaren en bewegingen te herkennen, of te herkennen als er op getikt wordt.
| Accelerometer - Bewegingsmeter 16g | ![](https://github.com/harmsel/Ubicomp-code/blob/main/imagesGit/acceler16.png)  | LET OP!  Zoek bij deze sensor de 16g code. Dit is een sensor die beweging en stand weergeeft over drie assen (x, y en z). Een soortgelijke sensor zit ook in je telefoon. Je kunt ‘m ook programmeren om gebaren en bewegingen te herkennen, of te herkennen als er op getikt wordt.
| Servo | ![](https://silicio.mx/media/catalog/product/cache/1/small_image/195x195/5e06319eda06f020e43594a9c230972d/r/o/rob08211p/Grove---Servomotor-21.jpg) | De as van dit ‘motortje’ kan draaien over 180 graden en in elke gewenste positie worden geplaatst. Je kunt ook beweging prototypen door de motor heen en weer te laten draaien. Tip: draai de servo niet helemaal in zijn uiterste van het bereik om te voorkomen dat deze gaat trillen.   |
| Trilmotor | ![](https://github.com/harmsel/Ubicomp-code/blob/main/imagesGit/tril.png) | Deze vibratiemotor (ook wel haptic motor) wordt gebruikt in smartphones en wearables. Je kunt hiermee informatie voelbaar doorgeven. Je kunt hier ook hoorbare feedback mee maken, door het motortje tegen hard materiaal te laten trillen. Hang je hem bijvoorbeeld tegen een glas, dan heb je een bel.|
| Chainable LED | ![](https://github.com/harmsel/Ubicomp-code/blob/main/imagesGit/chainled.png) | Dit component bevat een RGB LED. Je kunt de kleur en de helderheid instellen. In een aantal gevallen is de Ledstrip een makkelijkere keuze. De RGB led is wel fijn om in te bouwen in je prototype. Je kunt deze led doorverbinden, dus als je 4 leds wilt hebben, dan maak je een ketting (OUT naar IN). Vandaar de naam Chainable led.|

### Fouten oplossen

#### Code uploaden lukt niet
Krijg je na het uploaden onderstaande melding in de  oranje balk? Dan lukt het uploaden niet, dit komt niet door foute code.

![](https://docs.m2stud.io/cs/arduino/images/%28Arduino_Tutorials%29_Arduino_Upload_Fail.png)


1. Open een lege sketch (File > New) en upload deze lege sketch (zo weet je zeker dat het geen code probleem is)
2. Ga naar tools > Port
3. Selecteer de juiste Port ”/dev/cu.usbserial**’MAC of com (Windows) 
4. Staat deze Port er niet bij? Ruil dan je hardware (en kabel) even met je Buur
5. Je kunt ook proberen de Arduino opnieuw aan je Laptop aan te sluiten (als je geen buur hebt)
6. Kijik nogmaals naar https://youtu.be/C6NZ1WOGFKw ) 


##### Andere foutmelding (code problemen)
Upload een lege sketch. Krijg je in de oranje balk "Problem Uploading..." dan is het een probleem met verbinden/drivers. Krijg je een andere foutmelding dan zit het probleem in de Sketch (code).
Kijk rondom welke regel het fout gaat (is roze en regel staat in de foutmelding)
De meeste foutmeldingen gaan over fout plaatsen van { of } en een regel die niet eindigd met ;
