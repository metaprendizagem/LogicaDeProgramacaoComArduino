#Turn On/Off with If

Este projeto tem como objetivo demonstrar o uso da estrutura de repetição [If](https://www.arduino.cc/reference/pt/language/structure/control-structure/if/) no controle de execução do programa.

## Lista de materiais

 - Arduino Uno Rev 3
 - Cabo USB Tipo A-B
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

        Serial.begin(9600);
    }

    void loop() {

      if (Serial.available() > 0) {
        int incomingByte = Serial.read();
        Serial.print("I received: ");
        Serial.println(incomingByte);

        //Led Vermelho

        if(incomingByte == 10){
            digitalWrite(vermelho, HIGH);
            Serial.println("Liga Vermelho");
        }
        if(incomingByte == 11){
            digitalWrite(vermelho, HIGH);
            Serial.println("Desliga Vermelho");
        }

        //Led Amarelo

        if(incomingByte == 20){
            digitalWrite(vermelho, HIGH);
            Serial.println("Liga Amarelo");
        }
        if(incomingByte == 21){
            digitalWrite(vermelho, HIGH);
            Serial.println("Desliga Amarelo");
        }

        //Led Verde
        
        if(incomingByte == 30){
            digitalWrite(vermelho, HIGH);
            Serial.println("Liga Verde");
        }
        if(incomingByte == 31){
            digitalWrite(vermelho, HIGH);
            Serial.println("Desliga Verde");
        }

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

        Serial.begin(9600);
    }

    void loop() {

      if (Serial.available() > 0) {
        int incomingByte = Serial.read();
        Serial.print("I received: ");
        Serial.println(incomingByte);

        //Led Vermelho

        if(incomingByte == 10){
            digitalWrite(vermelho, HIGH);
            Serial.println("Liga Vermelho");
        }
        if(incomingByte == 11){
            digitalWrite(vermelho, HIGH);
            Serial.println("Desliga Vermelho");
        }

        //Led Amarelo

        if(incomingByte == 20){
            digitalWrite(vermelho, HIGH);
            Serial.println("Liga Amarelo");
        }
        if(incomingByte == 21){
            digitalWrite(vermelho, HIGH);
            Serial.println("Desliga Amarelo");
        }

        //Led Verde
        
        if(incomingByte == 30){
            digitalWrite(vermelho, HIGH);
            Serial.println("Liga Verde");
        }
        if(incomingByte == 31){
            digitalWrite(vermelho, HIGH);
            Serial.println("Desliga Verde");
        }

      }
    }
    ```

## Arquivos para Download

[![Arquivo ino](../arq/ino.png)](../arq/)         [![Arquivo fzz](../arq/fzz.png)](../arq/)