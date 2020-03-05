# Turn On/Off with Switch Case

Este projeto tem como objetivo demonstrar o uso da estrutura de repetição [Switch Case](https://www.arduino.cc/reference/pt/language/structure/control-structure/switchcase/) no controle de execução do programa.

## Lista de materiais

 - Arduino Uno Rev 3
 - Cabo USB Tipo A-B
 - 1 Led Verde
 - 1 Led Amarelo
 - 1 Led Vermelho
 - 3 Resistor 220Ω

## Modelo esquemático em Protoboard

![Modelo esquemático](../arq/turnOnOffWithSwitchCase.png)

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
        switch (incomingByte) {

        //Led Vermelho
          case 10:
            digitalWrite(vermelho, HIGH);
            Serial.println("Liga Vermelho");
            break;
          case 11:
            digitalWrite(vermelho, LOW);
            Serial.println("Desliga Vermelho");
            break;

        //Led Amarelo
          case 20:
            digitalWrite(amarelo, HIGH);
            Serial.println("Liga Amarelo");
            break;
          case 21:
            digitalWrite(amarelo, LOW);
            Serial.println("Desliga Amarelo");
            break;  

        //Led Verde
          case 30:
            digitalWrite(verde, HIGH);
            Serial.println("Liga Verde");
            break;
          case 31:
            digitalWrite(verde, LOW);
            Serial.println("Desliga Verde");
            break;  
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
        switch (incomingByte) {

        //Led Vermelho
          case 10:
            digitalWrite(vermelho, HIGH);
            Serial.println("Liga Vermelho");
            break;
          case 11:
            digitalWrite(vermelho, LOW);
            Serial.println("Desliga Vermelho");
            break;

        //Led Amarelo
          case 20:
            digitalWrite(amarelo, HIGH);
            Serial.println("Liga Amarelo");
            break;
          case 21:
            digitalWrite(amarelo, LOW);
            Serial.println("Desliga Amarelo");
            break;  

        //Led Verde
          case 30:
            digitalWrite(verde, HIGH);
            Serial.println("Liga Verde");
            break;
          case 31:
            digitalWrite(verde, LOW);
            Serial.println("Desliga Verde");
            break;  
        }
      }
    }
    ```

## Arquivos para Download

[![Arquivo ino](../arq/ino.png)](../arq/)         [![Arquivo fzz](../arq/fzz.png)](../arq/)