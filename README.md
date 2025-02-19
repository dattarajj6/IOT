//nocode  bulb j-12,13,, wire i-12 to GND ,,resister i-13,17,, wire h-17 to 5v
//withcode  bulb j-12,13,, wire i-12 to GND ,,resister i-13,17,, wire h-17 to 13 (ARD)
//button buib j-12,13,,wire i-12 to GND,,resister i-13,17,, wire h-17 to 8 (ARD),,resister g-19 ,23,,wire g-25 to 5V,, wire f-19 to GND,,, BUTTON F-23-25,e:-23,25,, wire d-23 to 2 (ARD)

//BUTTONCODE
#define LED_PIN 2
#define BUTTON_PIN 8

void setup() {
  pinMode(LED_PIN, OUTPUT);
  pinMode(BUTTON_PIN, INPUT);
}

void loop() {
  if (digitalRead(BUTTON_PIN) == HIGH) {
    digitalWrite(LED_PIN, HIGH);
  }
  else {
    digitalWrite(LED_PIN, LOW);
  }
}


//BLINKING
// the setup function runs once when you press reset or power the board
void setup() {
// initialize digital pin LED_BUILTIN as an output.
pinMode(LED_BUILTIN, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {
digitalWrite(LED_BUILTIN, HIGH); // turn the LED on (HIGH is the voltage level)
delay(10000); // wait for a second
digitalWrite(LED_BUILTIN, LOW); // turn the LED off by making the voltage LOW
delay(500); // wait for a second
}
