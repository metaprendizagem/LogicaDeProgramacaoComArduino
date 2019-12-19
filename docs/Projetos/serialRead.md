#Serial Read

Este projeto tem como objetivo demonstrar o uso da função [Serial.read()](https://www.arduino.cc/reference/pt/language/functions/communication/serial/read/)

## Lista de materiais

 - Arduino Uno Rev 3
 - Cabo USB Tipo A-B

## Modelo esquemático em Protoboard

![Modelo esquemático](../arq/)

??? note "Código"
    ```c
    int incomingByte = 0; 

    void setup() {
      Serial.begin(9600); 
    }

    void loop() {
      
        if (Serial.available() > 0) {
        
            incomingByte = Serial.read();

            Serial.print("I received: ");
            Serial.println(incomingByte, DEC);
        }
    }
    ```

??? note "Código Comentado"
    ```c
    int incomingByte = 0; 

    void setup() {
      Serial.begin(9600); 
    }

    void loop() {
      
        if (Serial.available() > 0) {
        
            incomingByte = Serial.read();

            Serial.print("I received: ");
            Serial.println(incomingByte, DEC);
        }
    }
    ```

## Arquivos para Download

[![Arquivo ino](../arq/ino.png)](../arq/)          [![Arquivo fzz](../arq/fzz.png)](../arq/)