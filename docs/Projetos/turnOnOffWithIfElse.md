# Turn On/Off with If Else

Este projeto tem como objetivo demonstrar o uso da estrutura de repetição If [Else](https://www.arduino.cc/reference/pt/language/structure/control-structure/else/) no controle de execução do programa.

## Lista de materiais

 - Arduino Uno Rev 3
 - Cabo USB Tipo A-B
 - 1 Led Verde
 - 1 Led Amarelo
 - 1 Led Vermelho
 - 3 Resistor 220Ω

## Modelo esquemático em Protoboard

![Modelo esquemático](../arq/turnOnOffWithIfElse.png)

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
        else if(incomingByte == 11){
            digitalWrite(vermelho, HIGH);
            Serial.println("Desliga Vermelho");
        }

        //Led Amarelo

        else if(incomingByte == 20){
            digitalWrite(vermelho, HIGH);
            Serial.println("Liga Amarelo");
        }
        else if(incomingByte == 21){
            digitalWrite(vermelho, HIGH);
            Serial.println("Desliga Amarelo");
        }

        //Led Verde
        
        else if(incomingByte == 30){
            digitalWrite(vermelho, HIGH);
            Serial.println("Liga Verde");
        }
        else if(incomingByte == 31){
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
        else if(incomingByte == 11){
            digitalWrite(vermelho, HIGH);
            Serial.println("Desliga Vermelho");
        }

        //Led Amarelo

        else if(incomingByte == 20){
            digitalWrite(vermelho, HIGH);
            Serial.println("Liga Amarelo");
        }
        else if(incomingByte == 21){
            digitalWrite(vermelho, HIGH);
            Serial.println("Desliga Amarelo");
        }

        //Led Verde
        
        else if(incomingByte == 30){
            digitalWrite(vermelho, HIGH);
            Serial.println("Liga Verde");
        }
        else if(incomingByte == 31){
            digitalWrite(vermelho, HIGH);
            Serial.println("Desliga Verde");
        }

      }
    }
    ```

## Arquivos para Download

[![Arquivo ino](../arq/ino.png)](../arq/)         [![Arquivo fzz](../arq/fzz.png)](../arq/)