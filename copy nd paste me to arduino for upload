//inspo from https://docs.arduino.cc/learn/electronics/lcd-displays#set-cursor-example

//takes serial input and scrolls it the screen as you type :) 

// include the library code:
#include <LiquidCrystal.h>

// initialize the library by associating any needed LCD interface pin
// with the arduino pin number it is connected to
const int rs = 13, en = 12, d4 = 11, d5 = 10, d6 = 9, d7 = 8;
LiquidCrystal lcd(rs, en, d4, d5, d6, d7);

void setup() {
  // set up the LCD's number of columns and rows:
  lcd.begin(16, 2);
  // initialize the serial communications:
  Serial.begin(9600);
}

void loop() {
  lcd.autoscroll();
  // when characters arrive over the serial port...
  if (Serial.available()) {
    // wait a bit for the entire message to arrive
    delay(100);
    // clear the screen
    lcd.clear();
    // read all the available characters
    while (Serial.available() > 0) {
      // display each character to the LCD
      lcd.write(Serial.read());
    }
    
  lcd.setCursor(16, 2);


  // set the display to automatically scroll:


  lcd.autoscroll();


  // print from 0 to 9:


  for (int thisChar = 0; thisChar < 100; thisChar++) {


    lcd.print("    ");


    delay(500);


  }
   lcd.noAutoscroll();


  // clear screen for the next loop:


  lcd.clear();
  }
}
