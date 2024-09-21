# Projeto BLINK

## Descrição
O projeto BLINK é um dos primeiros experimentos realizados com o Arduino, onde um LED integrado pisca em intervalos regulares. O LED acende por um segundo e, em seguida, apaga por um segundo, criando um efeito de piscar.

## Código
```cpp
void setup() {
  pinMode(LED_BUILTIN, OUTPUT); // Configura o LED integrado como saída
}

void loop() {
  digitalWrite(LED_BUILTIN, HIGH); // Acende o LED (HIGH é o nível de tensão)
  delay(1000);                     // Espera por um segundo
  digitalWrite(LED_BUILTIN, LOW);  // Apaga o LED (LOW é o nível de tensão)
  delay(1000);                     // Espera por um segundo
}
```

## Materiais Necessários
- **1 LED (ou utilize o LED integrado do Arduino)**
- **1 Resistor (220 Ω, para limitar a corrente)**
- **1 Arduino Uno**
- **3 Fios de conexão (jumpers)**

## Montagem do Circuito
1. Conecte o ânodo (terminal positivo) do LED ao pino digital do Arduino (ou utilize o LED integrado).
2. Conectue o cátodo (terminal negativo) do LED ao GND do Arduino através de um resistor de 220 Ω.
3. Utilize os fios de conexão para organizar as conexões.

## Diagrama
![shhs](https://github.com/yan1415/ATIVIDADES_LIA/blob/main/BLINK/Cool%20Esboo-Stantia%20(1).png)
