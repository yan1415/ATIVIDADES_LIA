# Enviando Dados para a Porta Serial

## Descrição
Este projeto demonstra como enviar o estado de um botão para a porta serial utilizando um Arduino. O estado do botão (pressionado ou solto) é exibido no monitor serial, permitindo monitorar suas interações em tempo real.

## Código
```cpp
const int pushButton = 2; // Pino onde o botão está conectado

void setup() {
  Serial.begin(9600);          // Inicializa a comunicação serial
  pinMode(pushButton, INPUT);  // Define o pino do botão como entrada
}

void loop() {
  // Lê o estado do botão
  int buttonState = digitalRead(pushButton);
  
  // Imprime o estado do botão na porta serial
  Serial.println(buttonState);
  
  // Atraso para estabilidade na leitura
  delay(100);
}
```

## Materiais Necessários
- **1 Botão**
- **1 Resistor (10 kΩ, para pull-up)**
- **1 Arduino Uno**
- **1 Protoboard**
- **6 Fios de conexão (jumpers)**

## Montagem do Circuito
1. Conecte um terminal do botão ao pino digital 2 do Arduino.
2. Conecte o outro terminal do botão a uma fonte de 5V.
3. Conecte um resistor de 10 kΩ entre o pino 2 e o GND para configurar o resistor pull-up.
4. Utilize a protoboard e os fios de conexão para organizar o circuito.

## Diagrama
![hdh](
