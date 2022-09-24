## Sensor de Movimento com Interruptor

O interruptor deslizante permite escolher qual dos equipamentos será ativado ao detectar movimento (Lâmpada ou Piezo).

###### Blocos:
![image][(https://github.com/eduarda-alcantara/IOT-e-Edge-Computing/blob/main/SensorMovimento/blocos.jpg)

###### Código:
```
// C++ code
//
void setup()
{
  pinMode(2, INPUT);
  Serial.begin(9600);
  pinMode(9, INPUT);
  pinMode(9, OUTPUT);
  pinMode(9, OUTPUT);
}

void loop()
{
  Serial.println(digitalRead(2));
  if (digitalRead(9) == 1) {
    tone(9, 523, 1000); // play tone 60 (C5 = 523 Hz)
  } else {
    digitalWrite(9, HIGH);
  }
  delay(10); // Delay a little bit to improve simulation performance
}
```
