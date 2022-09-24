## Sensor de Movimento Intermitente

A lâmpada permanece acesa enquanto o sensor sonoro (PIR) é interrompido em intervalos de 2 segundos.

###### Blocos:
![image](https://github.com/eduarda-alcantara/IOT-e-Edge-Computing/blob/main/SensorMovimento/blocos.jpg)

###### Código:
```
// C++ code
//
int i = 0;

void setup()
{
  pinMode(7, INPUT);
  Serial.begin(9600);
  pinMode(5, OUTPUT);
  pinMode(4, OUTPUT);
}

void loop()
{
  Serial.println(digitalRead(7));
  tone(5, 92, 1000); // play tone 30 (F#2 = 92 Hz)
  digitalWrite(4, HIGH);
  delay(2000); // Wait for 2000 millisecond(s)
  noTone(5);
}
```
