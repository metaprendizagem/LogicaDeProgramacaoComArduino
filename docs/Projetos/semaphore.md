#Semaphore

Este projeto tem como objetivo simular o funcionamento de um semáforo.

## Lista de materiais

 - 1 Arduino Uno Rev 3
 - 1 Led Verde
 - 1 Led amarelo
 - 1 Led Vermelho
 - 3 Resistor 220Ω

## Modelo esquemático em Protoboard

![Modelo esquemático](../arq/semaphore.png)

??? note "Código"
    ```c
    int vermelho = 11;
    int amarelo = 10; 
    int verde = 9; 

    void setup() {

        pinMode(vermelho, OUTPUT); 
        pinMode(amarelo, OUTPUT); 
        pinMode(verde, OUTPUT);

    }
    void loop() {

        digitalWrite(vermelho, HIGH); 
        delay(1000); 
        digitalWrite(vermelho, LOW);
        digitalWrite(amarelo, HIGH);
        delay(1000);
        digitalWrite(amarelo, LOW);
        digitalWrite(verde, HIGH);
        delay(1000);
        digitalWrite(verde, LOW);
        delay(1000);
    }
    ```

??? note "Código Comentado"
    ```c
    int vermelho = 11;
    int amarelo = 10; 
    int verde = 9; 

    void setup() {

        pinMode(vermelho, OUTPUT); 
        pinMode(amarelo, OUTPUT); 
        pinMode(verde, OUTPUT);

    }
    void loop() {

        digitalWrite(vermelho, HIGH); 
        delay(1000); 
        digitalWrite(vermelho, LOW);
        digitalWrite(amarelo, HIGH);
        delay(1000);
        digitalWrite(amarelo, LOW);
        digitalWrite(verde, HIGH);
        delay(1000);
        digitalWrite(verde, LOW);
        delay(1000);
    }
    ```
## Arquivos para Download

[![Arquivo ino](../arq/ino.png)](../arq/)          [![Arquivo fzz](../arq/fzz.png)](../arq/)