int Led1=4;
int Led2=5;
int Led3=6;
int Led4=7;
int salida;
void setup() {
Serial.begin(9600);
digitalWrite(Led1, OUTPUT);
digitalWrite(Led2, OUTPUT);
digitalWrite(Led3, OUTPUT);
digitalWrite(Led4, OUTPUT);
}

void loop() {
salida=(random(4));
delay(1000);
Serial.print(salida);
if(salida==0){
  digitalWrite(Led1, HIGH);
    digitalWrite(Led2,  LOW);
      digitalWrite(Led3,  LOW);
        digitalWrite(Led4, LOW);
}
if(salida==1){
  digitalWrite(Led1, LOW);
    digitalWrite(Led2, HIGH);
      digitalWrite(Led3, LOW);
        digitalWrite(Led4, LOW);
}
if(salida==2){
  digitalWrite(Led1, LOW);
    digitalWrite(Led2, LOW);
      digitalWrite(Led3, HIGH);
        digitalWrite(Led4, LOW);
}
if(salida==3){
  digitalWrite(Led1, LOW);
    digitalWrite(Led2, LOW);
      digitalWrite(Led3, LOW);
        digitalWrite(Led4, HIGH);
}
}
