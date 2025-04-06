

![img](pics/logo.jpg)

# JavaScript Workshop

Bei diesem Workshop verwenden wir die ***JavaScript* Bibliothek *p5.js***:

- ***JavaScript*** ist eine Programmiersprache.

  - Mit Programmiersprachen kann man Apps, Websites, Spiele, ... entwickeln.
  - *JavaScript* ist im Internet auf (fast) jeder Website im Einsatz!

- Eine **Bibliothek** ist wie ein Werkzeugkasten für Programmierer:innen
  - ***p5.js*** enthält z. B. fertige Zeichenfunktionen für Rechtecke, Kreise, ...

- Das **Koordinatensystem** eines Computers sieht etwas anders aus, als im Mathematik-Unterricht:

  ![img](pics/coordinategrid.png)



Ein *p5.js* Programm besitzt **zwei wichtige Funktionen**:

- **`setup()`**
  
  - Wird nur einmal (beim Programmstart) ausgeführt.
  - Darin wird z.B. das Spielfeld erstellt.
- **`draw()`**
  
  - Wird 60x pro Sekunde ausgeführt.
  - Darin werden z.B. die Spielfiguren gezeichnet.



**Unten siehst du den Code eines *p5.js* Programms (das du [hier](https://editor.p5js.org/) ausprobieren kannst):**

```js
// Anweisungen in setup() werden nur einmal (beim Programmstart) ausgeführt
function setup() {
  createCanvas(600, 400);     // erstellt eine Zeichenfläche mit 600x400 Pixeln
}

// Anweisungen in draw() werden 60x pro Sekunde ausgeführt
function draw() {
  background(255, 0, 255);    // färbt den Hintergrund magenta ein
  line(0, 400, 600, 0);       // zeichnet eine Linie
    
  if (mouseIsPressed) {       // wenn die Maustaste gedrückt ist
    fill(0, 255, 0);          // wird die Füllfarbe auf grün gesetzt,
  } else {                    // sonst
    fill(255, 255, 255);      // wird die Füllfarbe auf weiß gesetzt
  }
    
  circle(mouseX, mouseY, 50);   // zeichnet einen Kreis an die Position des Mauszeigers
}
```



**Und so sieht dieses Programm aus, wenn es ausgeführt wird:**

![img](pics/demo.gif)



**Jetzt bist DU an der Reihe selbst zu programmieren:**

- Am Beginn jeder Challenge siehst du, wie dein Programm am Ende aussehen soll.
- Darunter findest du eine Step-By-Step-Anleitung mit (hoffentlich) hilfreichen Tipps.
- Falls du einmal nicht mehr weiterkommst, findest du am Ende jeder Challenge eine mögliche Lösung.
  - "Schummeln" ist aber natürlich nur im Notfall erlaubt! 😉
- Wenn du alle Aufgaben geschafft hast, wartet am Ende noch die **Super Challenge**.
  - Hier gibt es keine detaillierte Anleitung und auch keine Musterlösung.



## Challenge 1: Alien On Earth

![img](pics/alien-on-earth.png)

1. Öffne den Web Editor auf https://editor.p5js.org/.

2. Kopiere folgendes Programm in den Editor.

   ```js
   function setup(){
     createCanvas(600, 400);
     rectMode(CENTER);
   }
   
   function draw(){
     // Hintergrund
     background(255, 255, 255);
       
     // Boden
     fill(255, 255, 255);
     rect(300, 360, 600, 80);
       
     // Körper
     fill(255, 255, 255);
     rect(300, 200, 40, 200);
       
     // Kopf
     fill(255, 255, 255);
     circle(300, 140, 120);
       
     // Linkes Auge 
     fill(255, 255, 255);
     ellipse(262, 140, 32, 64);
       
     // Rechtes Auge
     fill(255, 255, 255);
     ellipse(338, 140, 32, 64);
       
     // Beine
     line(280, 300, 260, 320);
     line(320, 300, 340, 320);
   }
   ```

3. Färbe den Boden grün.

   - Verwende dafür `(0, 255, 0)` als RGB-Code des ersten `fill()`
   - RGB ist eine Abkürzung für Rot-Grün-Blau.

4. Färbe das linke Auge rot.

   - Verwende dafür `(255, 0, 0)` als RGB-Code des dazugehörigen `fill()`. 

5. Färbe das rechte Auge blau.

   - Überlege, wie du den RGB-Code des dazugehörigen `fill()` anpassen musst.

6. Färbe den Kopf gelb.

   - Überlege, wie du den RGB-Code des dazugehörigen `fill()` anpassen musst.
   - Tipp: Gelb ist eine Mischung aus Rot und Grün.

7. Färbe den Körper magenta.

   - Überlege, wie du den RGB-Code des dazugehörigen `fill()` anpassen musst.
   - Tipp: Auch Magenta ist eine Mischung aus zwei Grundfarben.

8. Ändere die Hintergrundfarbe auf hellblau.

   - Verändere dafür den RGB-Code von `background()`.

   - Den RGB-Code von Hellblau kannst du mit einem [Colour Picker](https://g.co/kgs/GN5Bi2) herausfinden.

<details>
<summary>Lösung</summary>

```js
function setup(){
  createCanvas(600, 400);
  rectMode(CENTER);
}

function draw(){
  // Hintergrund
  background(66, 194, 245);
    
  // Boden
  fill(0, 255, 0);
  rect(300, 360, 600, 80);
    
  // Körper
  fill(255, 0, 255);
  rect(300, 200, 40, 200);
    
  // Kopf
  fill(255, 255, 0);
  circle(300, 140, 120);
    
  // Linkes Auge
  fill(255, 0, 0);
  ellipse(262, 140, 32, 64);
    
  // Rechtes Auge
  fill(0, 0, 255);
  ellipse(338, 140, 32, 64);
    
  // Beine
  line(280, 300, 260, 320);
  line(320, 300, 340, 320);
}
```

</details>



## Challenge 2: Sand Worm

![img](pics/sand-worm.gif)

1. Öffne den Web Editor auf https://editor.p5js.org/.

   - Falls du den Editor noch von der letzten Challenge geöffnet hast: Lade die Website neu!
2. Verändere die Größe der Zeichenfläche.

   - Breite: 600 Pixel
   - Höhe: 400 Pixel
3. Färbe in `draw()` den Hintergrund orange ein.

   - Den RGB-Code kannst du mit einem [Colour Picker](https://g.co/kgs/vGP3eQ) herausfinden.
   - RGB ist eine Abkürzung für Rot-Grün-Blau.
4. Zeichne in `draw()` einen Kreis in die Mitte der Zeichenfläche.

   -   Verwende: `circle(300, 200, 20);`
5. Vergrößere den Durchmesser des Kreises auf 80 Pixel.
6. Setze in `draw()` die Füllfarbe auf grau.

   - Rufe dafür `fill()` mit dem passenden RGB-Code auf.
   - Tipp: Der Aufruf von `fill()` muss vor dem Aufruf von `circle()` stattfinden!
7. Verwende als x-Koordinate des Kreises die Position des Mauszeigers.

   - Auf die x-Koordinate des Mauszeigers kannst du über die Variable `mouseX` zugreifen.
   - Der Kreis sollte sich jetzt waagrecht mit deiner Maus bewegen.
8. Verwende auch für die y-Koordinate des Kreises die Position des Mauszeigers.

   - Wie könnte die passende Variable heißen?
9. Rufe `background()` am Ende von `setup()` statt in `draw()` auf.

   - Wie wirkt sich diese Änderung aus?


<details>
<summary>Lösung</summary>

```js
function setup() {
  createCanvas(600, 400);
  background(235, 159, 52);
}

function draw() {
  fill(170, 173, 170);
  circle(mouseX, mouseY, 80);
}
```

</details>



## Challenge 3: Switch Colors

![img](pics/switch-colors.gif)

1. Öffne den Web Editor auf https://editor.p5js.org/.

2. Kopiere folgendes Programm in den Editor.

   ```js
   function setup() {
     createCanvas(600, 400);
   }
   
   function draw() {
     background(255, 255, 255);
     
     // Verzweigung
     
       
     line(300, 0, 300, 100);
     circle(mouseX, mouseY, 80);
   }
   ```

3. Ändere den Aufruf von `line()`, so dass die senkrechte Linie bis nach unten reicht.

4. Füge folgenden Verzweigung in `draw()` ein. Welche Auswirkung hat diese Änderung?

   ```js
   function draw() {
     ...
     // Verzweigung
     if (mouseX < 300) { 
       fill(255, 0, 0);
     } else {
       fill(0, 255, 0);
     } 
     ...
   }
   ```

5. Ändere in der Verzweigung auch die Hintergrundfarbe.

   - Wenn der Mauszeiger in der linken Hälfte ist, soll der Hintergrund grün sein.
   - Sonst soll der Hintergrund rot sein.
   - Der Hintergrund ist also immer anders eingefärbt als der Kreis. 😉

<details>
<summary>Lösung</summary>

```js
function setup() {
  createCanvas(600, 400);
}

function draw() {
  // Verzweigung
  if (mouseX < 300) { 
    fill(255, 0, 0);
    background(0, 255, 0);
  } else {
    fill(0, 255, 0);
    background(255, 0, 0);
  } 
  
  line(300, 0, 300, 400);
  circle(mouseX, mouseY, 80);
}
```

</details>



## Challenge 4: Falling Ball

![img](pics/falling-ball.gif)

1. Öffne den Web Editor auf https://editor.p5js.org/.

2. Kopiere folgendes Programm in den Editor.

   ```js
   let ballX = 300;
   let ballY = 0;
   
   function setup() {
     createCanvas(600, 400);
     fill(255, 255, 255);
   }
   
   function draw() {
     background(0, 0, 0);
   
     // Verzweigung in der nächsten Zeile einfügen
     
   }
   ```
   
3. Zeichne in `draw()` mithilfe des folgenden Befehls einen Ball (=Kreis) an der Position `ballX` und `ballY`.

   - Verwende: `circle(ballX, ballY, 20);`

4. Erhöhe in `draw()` den Wert der y-Koordinate um 1. Der Ball sollte jetzt nach unten fallen.

   - Verwende: `ballY = ballY + 1;`

5. Erhöhe die Geschwindigkeit des Balls, so dass er fünfmal so schnell nach unten fällt.

6. Füge in `draw()` die folgende Verzweigung ein.

   ```js
   if (ballY > height) {
   
   }
   ```

   - Die Variable `height` enthält die Höhe des Spielfelds.
   - So kannst du also prüfen, ob der Ball unten angekommen ist.

7. Setze, wenn der Ball am Boden auftrifft, die y-Koordinate auf 0 zurück.

   - Dadurch sollte ein "neuer" Ball von oben fallen.

8. Füge in der Verzweigung eine weitere Anweisung hinzu. 

   - Verwende: `ballX = random(600);`
   - Welche Auswirkung hat diese Änderung? 


<details>
<summary>Lösung</summary>

```js
let ballX = 300;
let ballY = 0;

function setup() {
  createCanvas(600, 400);
  fill(255, 255, 255);
}

function draw() {
  background(0, 0, 0);
  
  ballY = ballY + 5;
  circle(ballX, ballY, 20);

  if (ballY > height) {
	ballY = 0;
    ballX = random(600);
  }
}
```

</details>



## Challenge 5: Catch the Ball

![img](pics/catch-the-ball.gif)

1. Öffne den Web Editor auf https://editor.p5js.org/.

2. Kopiere folgendes Programm in den Editor.

   ```js
   let ballX = 300;
   let ballY = 0;
   
   function setup() {
     createCanvas(600, 400);
     fill(255, 255, 255);
     rectMode(CENTER);
   }
   
   function draw() {
     background(0, 0, 0);
     
     ballY = ballY + 5;
     circle(ballX, ballY, 20);
   
     if (ballY > height) {
   	ballY = 0;
       ballX = random(600);
     }
   }
   ```

3. Zeichne in `draw()` einen Fangkorb (=Rechteck).

   - Verwende: `rect(100, 200, 40, 20); `


4. Verwende als x-Koordinate des Fangkorbs die Position des Mauszeigers.

5. Positioniere den Fangkorb am unteren Rand des Spielfelds.

   - Verwende für die Berechnung der y-Koordinate den Wert der Variable `height` (=Spielfeldhöhe).
   - Tipp: Du musst von `height` noch etwas abziehen.

<details>
<summary>Lösung</summary>

```js
let x = 300;
let y = 0;

function setup() {
  createCanvas(600, 400);
  fill(255, 255, 255);
  rectMode(CENTER);
}

function draw() {
  background(0, 0, 0);
  
  y = y + 5;
  circle(x, y, 20);

  if (y > height) {
    y = 0;  
    x = random(600);
  }
  
  rect(mouseX, height - 10, 40, 20);  
}
```

</details>



## Challenge 6: Count Catches

![img](pics/count-catches.gif)

1. Öffne den Web Editor auf https://editor.p5js.org/.

2. Kopiere folgendes Programm in den Editor.

   ```js
   let ballX = 300;
   let ballY = 0;
   let counter = 10;
   
   function setup() {
     createCanvas(600, 400);
     fill(255, 255, 255);
     textSize(30);
     rectMode(CENTER);
   }
   
   function draw() {
     background(0, 0, 0);
     text(counter, 570, 40);
     
     ballY = ballY + 5;
     circle(ballX, ballY, 20);
   
     if (ballY > height) {
       // Verzweigung in der nächsten Zeile einfügen
   
       ballY = 0;  
       ballX = random(600);
     }
     
     rect(mouseX, height - 10, 40, 20);  
   }
   ```

3. Ändere den Startwert der Variable `counter` von 10 auf 0.

   - Mithilfe dieser Variable wollen wir später die gefangenen Bälle zählen.


4. Zeige den Wert von `counter` links oben (statt rechts oben) an.

5. Füge in `draw()` an der vorgesehenen Stelle die folgende Verzweigung ein.

   ```js
   if (ballX > mouseX - 10 && ballX < mouseX + 10) {
     
   } 
   ```

   - Mithilfe dieser Verzweigung kannst du überprüfen, ob der Ball gefangen wurde.

6. Erhöhe, falls der Ball gefangen wurde, den Wert der Variable `counter` um 1.

<details>
<summary>Lösung</summary>

```js
let ballX = 300;
let ballY = 0;
let counter = 0;

function setup() {
  createCanvas(600, 400);
  fill(255, 255, 255);
  textSize(30);
  rectMode(CENTER);
}

function draw() {
  background(0, 0, 0);
  text(counter, 10, 40);
  
  ballY = ballY + 5;
  circle(ballX, ballY, 20);

  if (ballY > height) {
    if (ballX > mouseX - 10 && ballX < mouseX + 10) {
      counter = counter + 1;
    } 
    
    ballY = 0;  
    ballX = random(600);
  }
  
  rect(mouseX, height - 10, 40, 20);  
}
```

</details>


## Challenge 7: Game Over

![img](pics/game-over.gif)

1. Öffne den Web Editor auf https://editor.p5js.org/.

2. Kopiere folgendes Programm in den Editor.

   ```js
   let ballX = 300;
   let ballY = 0;
   let counter = 0;
   let gameOver = false;
   
   function setup() {
     createCanvas(600, 400);
     fill(255, 255, 255);
     textSize(30);
     rectMode(CENTER);
   }
   
   function draw() {
     if (gameOver) {
       // Gib den Text "GAME OVER" in der nächsten Zeile aus
         
       return;
     }
       
     background(0, 0, 0);
     text(counter, 10, 40);
     
     ballY = ballY + 5;
     circle(ballX, ballY, 20);
   
     if (ballY > height) {
       if (ballX > mouseX - 10 && ballX < mouseX + 10) {
         counter = counter + 1;
       } else {
         // Verändere die gameOver-Variable in der nächsten Zeile
         
       }
       
       ballY = 0;  
       ballX = random(600);
     }
     
     rect(mouseX, height - 10, 40, 20);  
   }
   ```

3. Beende, wenn der Ball nicht gefangen wurde, das Spiel.

   - Im Programm ist bereits ein `else`-Zweig vorhanden.
   - Der Code im `else`-Zweig wird nur ausgeführt, wenn der Ball verfehlt wurde.
   - Setze also im `else`-Zweig, den Wert der Variable `gameOver` auf den Wert `true`.


4. Gib, wenn das Spiel verloren wurde, den Text "GAME OVER" in der Mitte des Spielfelds aus.

<details>
<summary>Lösung</summary>

```js
let ballX = 300;
let ballY = 0;
let counter = 0;
let gameOver = false;

function setup() {
  createCanvas(600, 400);
  fill(255, 255, 255);
  textSize(30);
  rectMode(CENTER);
}

function draw() {
  if (gameOver) {
    text("GAME OVER", 200, height/2);
    return;
  }
  
  background(0, 0, 0);
  text(counter, 10, 40);
  
  ballY = ballY + 5;
  circle(ballX, ballY, 20);

  if (ballY > height) {
    if (ballX > mouseX - 10 && ballX < mouseX + 10) {
      counter = counter + 1;
    } else {
      gameOver = true;
    }
    
    ballY = 0;  
    ballX = random(600);
  }
  
  rect(mouseX, height - 10, 40, 20);  
}
```

</details>



## Super Challenge 1: Jumping Ball

![img](pics/jumping-ball.gif)

1. Öffne den Web Editor auf https://editor.p5js.org/.

2. Kopiere folgendes Programm in den Editor.

   ```js
   let x = 300;
   let y = 0;
   let speed = 5;
   
   function setup() {
     createCanvas(600, 400);
     fill(255, 255, 255);
   }
   
   function draw() {
     background(0, 0, 0);
     
     y = y + speed;
     circle(x, y, 20);
   
     if (y > height) {
       y = 0;
     }
   }
   ```

3. Verändere das Programm, so dass der Ball zwischen Boden und Decke hin und her springt.



## Super Challenge 2: Crazy Jumping Ball

![img](pics/crazy-jumping-ball.gif)

1. Öffne den Web Editor auf https://editor.p5js.org/.

2. Kopiere folgendes Programm in den Editor.

   ```js
   let x = 0;
   let y = 0;
   let speedX = 3;
   let speedY = 5;
   
   function setup() {
     createCanvas(600, 400);
     fill(255, 255, 255);
   }
   
   function draw() {
     background(0, 0, 0);
     
     y = y + speedY;
     circle(x, y, 20);
   
     if (y > height) {
       speedY = -5;
     }
     
     if (y < 0) {
       speedY = 5;
     }
   }
   ```
   
3. Verändere das Programm, so dass sich der Ball schräg nach rechts bewegt.

4. Verändere das Programm, so dass der Ball auch vom linken und rechten Rand zurückspringt.



## Super Challenge 3: Red Jumping Ball

![img](pics/red-jumping-ball.gif)

1. Öffne den Web Editor auf https://editor.p5js.org/.

2. Kopiere folgendes Programm in den Editor.

   ```js
   let x = 0;
   let y = 0;
   let speedX = 2;
   let speedY = 3;
   let radius = 50;
   
   function setup() {
     createCanvas(600, 400);
     fill(255, 255, 255);
   }
   
   function draw() {
     background(0, 0, 0);
     
     let squareDistance = (mouseX-x)*(mouseX-x) + (mouseY-y)*(mouseY-y);
     
     // Prüfe hier, ob der Mauszeiger im Kreis liegt
     
     y = y + speedY;
     x = x + speedX;
     circle(x, y, radius);
   
     if (y > height || y < 0) {
       speedY = speedY * (-1);
     }
     
     if (x > width || x < 0) {
       speedX = speedX * (-1);
     }
   }
   ```

3. Verändere das Programm, so dass der Ball rot ist, wenn ihn der Mauszeiger berührt.
