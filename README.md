# LDR
int led = 2;
int ldr = A5;
int vldr = 0;
void setup() {
  pinMode(ldr,INPUT);
  pinMode(led,OUTPUT);
  Serial.begin(9600);
}

void loop() {
  Serial.println(vldr);
  vldr = analogRead(ldr);
  if (vldr <= 20){
    digitalWrite(led,LOW);
    }
    else {
    digitalWrite(led,HIGH);
    }
}
