# Sequencial 3 Canais

## Descrição
Este projeto faz com que três LEDs acendam sequencialmente, criando um efeito visual interessante. Cada LED permanece aceso por um segundo antes de passar para o próximo, permitindo observar a sequência de iluminação.

## Código
```cpp
const int ledPin1 = 4; // Pino do primeiro LED
const int ledPin2 = 5; // Pino do segundo LED
const int ledPin3 = 6; // Pino do terceiro LED

void setup() {
  pinMode(ledPin1, OUTPUT); // Configura o pino do LED 1 como saída
  pinMode(ledPin2, OUTPUT); // Configura o pino do LED 2 como saída
  pinMode(ledPin3, OUTPUT); // Configura o pino do LED 3 como saída
}

void loop() {
  digitalWrite(ledPin1, HIGH); // Acende o LED 1
  delay(1000);                  // Espera por 1 segundo
  digitalWrite(ledPin1, LOW);  // Apaga o LED 1

  digitalWrite(ledPin2, HIGH); // Acende o LED 2
  delay(1000);                  // Espera por 1 segundo
  digitalWrite(ledPin2, LOW);  // Apaga o LED 2

  digitalWrite(ledPin3, HIGH); // Acende o LED 3
  delay(1000);                  // Espera por 1 segundo
  digitalWrite(ledPin3, LOW);  // Apaga o LED 3
}
```

## Materiais Necessários
- **1 Arduino Uno**
- **3 Resistores (220 Ω, para limitar a corrente)**
- **3 LEDs (Verde, Amarelo, Vermelho)**
- **1 Protoboard**
- **Fios de conexão (jumpers)**
- **Cabo USB para comunicação com o Arduino**
- **Software Arduino instalado e configurado**

## Montagem do Circuito
1. Conecte o ânodo (terminal positivo) do LED Verde ao pino digital 4 do Arduino, e o cátodo (terminal negativo) ao GND através de um resistor de 220 Ω.
2. Conecte o ânodo do LED Amarelo ao pino digital 5 do Arduino, e o cátodo ao GND através de outro resistor de 220 Ω.
3. Conecte o ânodo do LED Vermelho ao pino digital 6 do Arduino, e o cátodo ao GND através de mais um resistor de 220 Ω.
4. Utilize a protoboard e os fios de conexão para organizar o circuito.

## Diagrama
![sgyij](
