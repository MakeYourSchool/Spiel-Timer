# Spiel-Timer
----
Hier ist der Beispiel-Code für den Spiel-Timer, der in der Einführung zu den Remote Hackdays zusammen mit den SchülerInnen aufgebaut wird.

Beim Spiel-Timer handelt es sich um einen Timer, der eine festgelegte Zeit nach Betätigen eines Buttosn abwartet um schließlich einen angeschlossenen Summer zu betätigen. Der Timer könnte etwa für die Begrenzung der Zeit bei einzelnen Spielzügen im Schach oder anderen Spielen eingesetzt werden. 

## Aufbau

<img src=https://raw.githubusercontent.com/MakeYourSchool/Spiel-Timer/main/Abbildung/Spiel-Timer.jpg width=600px>

Bildquelle: *Wissenschaft im Dialog*

## Code

```
//Kommentare und Kopfzeile
const int buttonPin = 2;
const int buzzerPin = 6;
int buttonState = 0;

void setup() {
  //Ein- und Ausgänge initialisieren:
  pinMode(buttonPin,INPUT);
  pinMode(buzzerPin,OUTPUT);
}

void loop() {
  buttonState = digitalRead(buttonPin);
  
  if (buttonState==HIGH) {
    delay(5000);
    
    digitalWrite(buzzerPin,HIGH);
    delay(100);
    digitalWrite(buzzerPin,LOW);
    
    delay(500);
    
    digitalWrite(buzzerPin,HIGH);
    delay(100);
    digitalWrite(buzzerPin,LOW);
  }
}

```

