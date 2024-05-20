#include <NewPing.h>

#define M1 5
#define M2 7
#define DIRECTION1 4
#define DIRECTION2 6
#define Mot1 2
#define Mot2 3
#define DIR1 9
#define DIR2 12

char Command = 'S';

void setup() {
pinMode(Mot1, OUTPUT);
pinMode(DIR1, OUTPUT);
pinMode(Mot2, OUTPUT);
pinMode(DIR2, OUTPUT);
pinMode(M1, OUTPUT);
pinMode(M2, OUTPUT);
pinMode(DIRECTION1, OUTPUT);
pinMode(DIRECTION2, OUTPUT);
pinMode (10, OUTPUT); 
pinMode (11, OUTPUT);
Serial.begin(9600);
}

void loop() {
  Command = Serial.read();
  digitalWrite(M1, HIGH);
  digitalWrite(DIRECTION1, LOW);
  digitalWrite(M2, LOW);
  digitalWrite(DIRECTION2, HIGH);
  delay(600);
  digitalWrite(M1, LOW);
  digitalWrite(DIRECTION1, HIGH);
  digitalWrite(M2, LOW);
  digitalWrite(DIRECTION2, HIGH);
  delay(600);
}
