# Luzes de Sinalização de Garagem

## Descrição
Este projeto utiliza dois LEDs para simular um sistema de sinalização de garagem. Os LEDs acendem alternadamente, e o estado de cada LED é enviado para a porta serial, permitindo monitorar a operação do sistema em tempo real.

## Código
```cpp
const int ledPin1 = 13; // Pino do primeiro LED
const int ledPin2 = 9;  // Pino do segundo LED

const int interval = 500; // Intervalo de tempo em milissegundos

void setup() {
  Serial.begin(9600); // Inicializa a comunicação serial

  pinMode(ledPin1, OUTPUT); // Configura o pino do LED 1 como saída
  pinMode(ledPin2, OUTPUT); // Configura o pino do LED 2 como saída

  Serial.print("LED 1 está conectado ao pino ");
  Serial.println(ledPin1);
  Serial.print("LED 2 está conectado ao pino ");
  Serial.println(ledPin2);
}

void loop() {
  digitalWrite(ledPin1, HIGH); // Acende o LED 1
  digitalWrite(ledPin2, LOW);  // Apaga o LED 2
  Serial.println("LED 1 aceso, LED 2 apagado");
  delay(interval);

  digitalWrite(ledPin1, LOW);  // Apaga o LED 1
  digitalWrite(ledPin2, HIGH); // Acende o LED 2
  Serial.println("LED 1 apagado, LED 2 aceso");
  delay(interval);
}
```

## Materiais Necessários
- **1 Protoboard**
- **1 Arduino Uno**
- **2 LEDs**
- **2 Resistores (220 Ω, para limitar a corrente)**
- **3 Fios de conexão (jumpers)**

## Montagem do Circuito
1. Conecte o ânodo (terminal positivo) do LED 1 ao pino digital 13 do Arduino, e o cátodo (terminal negativo) ao GND através de um resistor de 220 Ω.
2. Conecte o ânodo do LED 2 ao pino digital 9 do Arduino, e o cátodo ao GND através de outro resistor de 220 Ω.
3. Utilize a protoboard e os fios de conexão para organizar o circuito.

## Diagrama
![hsuydyg](
