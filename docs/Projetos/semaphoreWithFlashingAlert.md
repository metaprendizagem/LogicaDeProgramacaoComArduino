#Semaphore with Flashing Alert

Este projeto tem como objetivo simular um semáforo porém com a função de pisca alerta comumente utilizada durante a noite.

## Lista de materiais:

 - 1 Arduino Uno Rev 3
 - 1 Cabo USB Tipo A-B
 - 1 Led Verde
 - 1 Led Amarelo
 - 1 Led Vermelho
 - 3 Resistor 220Ω

## Modelo esquemático em Protoboard

![Modelo esquemático](../arq/)

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
        
        int transicao = 3;

        while(transicao >=3){
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
            transicao--;
        }

        digitalWrite(vermelho, LOW);
        digitalWrite(amarelo, LOW);
        digitalWrite(verde, LOW);

        for(int indice = 0; indice <3; i++){
            digitalWrite(amarelo, HIGH);
            delay(150);
            digitalWrite(amarelo, LOW);
        }
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
        
        int transicao = 3;

        while(transicao >=3){
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
            transicao--;
        }

        digitalWrite(vermelho, LOW);
        digitalWrite(amarelo, LOW);
        digitalWrite(verde, LOW);

        for(int indice = 0; indice <3; i++){
            digitalWrite(amarelo, HIGH);
            delay(150);
            digitalWrite(amarelo, LOW);
        }
    }
    ```

## Arquivos para Download

[![Arquivo ino](../arq/ino.png)](../arq/)         [![Arquivo fzz](../arq/fzz.png)](../arq/)