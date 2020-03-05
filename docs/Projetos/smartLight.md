#Smart Light

Este projeto tem como objetivo demonstrar como realizar o controle de luminosidade de um led tendo como referência o valor de tensão lido em um potenciômetro

## Lista de materiais:

 - 1 Arduino Uno Rev 3
 - 1 Led
 - 1 Resistor 220Ω

## Modelo esquemático em Protoboard

![Modelo esquemático](../arq/smartLight.png)

??? note "Código"
    ```c
    int ldr = A0;
    int led = 11;
    int valor; 

    void setup() {

        pinMode(led, OUTPUT); 
    }
    void loop() {

        valor = analogRead(ldr);
        ldr valor = map(valor, 0, 1023, 0, 255);
        analogWrite(led, valor);
    }
    ```

??? note "Código Comentado"
    ```c
    int ldr = A0;
    int led = 11;
    int valor; 

    void setup() {

        pinMode(led, OUTPUT); 
    }
    void loop() {

        valor = analogRead(ldr);
        ldr valor = map(valor, 0, 1023, 0, 255);
        analogWrite(led, valor);
    }
    ```

## Arquivos para Download

[![Arquivo ino](../arq/ino.png)](../arq/)          [![Arquivo fzz](../arq/fzz.png)](../arq/)