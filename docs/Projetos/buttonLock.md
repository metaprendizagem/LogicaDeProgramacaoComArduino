#Button Lock

Este projeto tem como objetivo demonstrar como podemos criar um intertravamento a fim de bloquear a execução de um programa em um determinado ponto quando inserimos um sinal de entrada através de um botão.

## Lista de materiais:

 - 1 Arduino Uno Rev 3
 - 1 Cabo USB Tipo A-B
 - 1 Tactile Switch
 - 2 Led
 - 2 Resistor 220Ω
 - 1 Resistor 10KΩ

## Modelo esquemático em Protoboard

![Modelo esquemático](../arq/)

??? note "Código"
    ```c
    int botao = 8; 
    int ledBlink = 7; 
    int ledButton = 9;

    int estadoLedBlink, estadoLedButton;

    void setup() {

        pinMode(botao, INPUT); 
        pinMode(ledBlink, OUTPUT); 
        pinMode(ledButton, OUTPUT);
    }

    void loop() {

        estadoLedButton = digitalRead(botao); 

        if(estadoLedButton == HIGH){
            digitalWrite(ledButton, HIGH);
            while(estadoLedButton == HIGH){
                estadoLedButton = digitalRead(botao);
            }
        }

        digitalWrite(ledButton, LOW);

        if (estadoLedBlink == 1) { 
            digitalWrite(ledBlink, LOW); 
            estadoLedBlink = 0;
        } else { 
            digitalWrite(led, HIGH);
            estadoLedBlink = 1;
        }
        delay(500);
    }
    ```

??? note "Código Comentado"
    ```c
    int botao = 8; 
    int ledBlink = 7; 
    int ledButton = 9;

    int estadoLedBlink, estadoLedButton;

    void setup() {

        pinMode(botao, INPUT); 
        pinMode(ledBlink, OUTPUT); 
        pinMode(ledButton, OUTPUT);
    }

    void loop() {

        estadoLedButton = digitalRead(botao); 

        if(estadoLedButton == HIGH){
            digitalWrite(ledButton, HIGH);
            while(estadoLedButton == HIGH){
                estadoLedButton = digitalRead(botao);
            }
        }

        digitalWrite(ledButton, LOW);

        if (estadoLedBlink == 1) { 
            digitalWrite(ledBlink, LOW); 
            estadoLedBlink = 0;
        } else { 
            digitalWrite(led, HIGH);
            estadoLedBlink = 1;
        }
        delay(500);
    }
    ```

## Arquivos para Download

[![Arquivo ino](../arq/ino.png)](../arq/)[![Arquivo fzz](../arq/fzz.png)](../arq)