#Up Down Blink

Este projeto tem como objetivo demonstrar como realizar o acionamento de uma barra de leds em sequência com a utilição da estrutura de repetição [For](https://www.arduino.cc/reference/en/language/structure/control-structure/for/).

## Lista de materiais:

 - 1 Arduino Uno Rev 3
 - 1 Cabo USB Tipo A-B
 - 1 Led Verde
 - 1 Led Amarelo
 - 1 Led Vermeho
 - 3 Resistor 220Ω

## Modelo esquemático em Protoboard

![Modelo esquemático](../arq/)

??? note "Código"
    ```c
    void setup() {
  
        for (int thisLed = 9; thisLed <= 11; thisLed++) {
            pinMode(thisLed, OUTPUT);
        }
    }

    void loop() {
      
        for (int thisLed = 9; thisLed <= 11; thisLed++) {
            digitalWrite(thisLed, HIGH);
            delay(1000);
            digitalWrite(thisLed, LOW);
        }

        for (int thisLed = 11; thisLed >= 9; thisLed--) {
            digitalWrite(thisLed, HIGH);
            delay(1000);
            digitalWrite(thisLed, LOW);
        }
    }
    ```

??? note "Código Comentado"
    ```c
    void setup() {
  
        for (int thisLed = 9; thisLed <= 11; thisLed++) {
            pinMode(thisLed, OUTPUT);
        }
    }

    void loop() {
      
        for (int thisLed = 9; thisLed <= 11; thisLed++) {
            digitalWrite(thisLed, HIGH);
            delay(1000);
            digitalWrite(thisLed, LOW);
        }

        for (int thisLed = 11; thisLed >= 9; thisLed--) {
            digitalWrite(thisLed, HIGH);
            delay(1000);
            digitalWrite(thisLed, LOW);
        }
    }
    ```

## Arquivos para Download

[![Arquivo ino](../arq/ino.png)](../arq/)         [![Arquivo fzz](../arq/fzz.png)](../arq/)