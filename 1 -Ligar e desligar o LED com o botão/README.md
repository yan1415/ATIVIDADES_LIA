# Ligar e Desligar o LED com o Botão

## Descrição
Este projeto demonstra como utilizar um botão para controlar um LED, contabilizando quantas vezes o botão foi pressionado. O LED integrado no Arduino acende quando o botão é pressionado e apaga quando solto. O número de pressões é exibido na porta serial.

## Código
```cpp
const int buttonPin = 2;         // Pino onde o botão está conectado
const int ledPin = LED_BUILTIN;  // Pino do LED integrado
int buttonPushCounter = 0;        // Contador de pressões do botão
int buttonState = 0;              // Estado atual do botão
int lastButtonState = 0;          // Estado anterior do botão

void setup() {
  pinMode(buttonPin, INPUT);      // Define o pino do botão como entrada
  pinMode(ledPin, OUTPUT);        // Define o pino do LED como saída
  Serial.begin(9600);             // Inicializa a comunicação serial
}

void loop() {
  buttonState = digitalRead(buttonPin); // Lê o estado atual do botão

  // Detecta mudanças de estado do botão
  if (buttonState != lastButtonState) {
    if (buttonState == HIGH) {        // Se o botão for pressionado
      buttonPushCounter++;            // Incrementa o contador
      Serial.println("on");           // Indica que o botão foi pressionado
      Serial.print("Número de pressões: ");
      Serial.println(buttonPushCounter); // Exibe o contador
    } else {
      Serial.println("off");           // Indica que o botão foi solto
    }
    delay(50); // Debounce do botão
  }

  lastButtonState = buttonState; // Atualiza o estado anterior
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
