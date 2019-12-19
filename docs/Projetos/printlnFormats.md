#Println Formats

Este projeto tem como objetivo demonstrar os possíveis formatos de saída da função [Serial.println()](https://www.arduino.cc/reference/pt/language/functions/communication/serial/println/)

## Lista de materiais

 - Arduino Uno Rev 3
 - Cabo USB Tipo A-B

## Modelo esquemático em Protoboard

![Modelo esquemático](../arq/)

??? note "Código"
    ```c
    int analogValue = 0;    

    void setup() {

        Serial.begin(9600);

    }

    void loop() {
      
        analogValue = analogRead(0);

        Serial.println(analogValue); 
        Serial.println(analogValue, DEC); 
        Serial.println(analogValue, HEX);
        Serial.println(analogValue, OCT); 
        Serial.println(analogValue, BIN);

        delay(10);
    }
    ```

??? note "Código Comentado"
    ```c
    int analogValue = 0;    

    void setup() {

        Serial.begin(9600);

    }

    void loop() {
      
        analogValue = analogRead(0);

        // Imprime a leitura em vários formatos:
        Serial.println(analogValue);       // imprime como decimal (padrão) codificado em ASCII
        Serial.println(analogValue, DEC);  // imprime como decimal codificado em ASCII
        Serial.println(analogValue, HEX);  // imprime como hexadecimal codificado em ASCII
        Serial.println(analogValue, OCT);  // imprime como octal codificado em ASCII
        Serial.println(analogValue, BIN);  // imprime como binário codificado em ASCII

        delay(10);
    }
    ```

## Arquivos para Download

[![Arquivo ino](../arq/ino.png)](../arq/)         [![Arquivo fzz](../arq/fzz.png)](../arq/)