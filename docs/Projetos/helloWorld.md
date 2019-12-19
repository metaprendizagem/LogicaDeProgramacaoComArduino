#Hello World

Este projeto tem como objetivo demonstrar o uso da função [Serial.println()](https://www.arduino.cc/reference/pt/language/functions/communication/serial/println/)

## Lista de materiais

 - Arduino Uno Rev 3
 - Cabo USB Tipo A-B

## Modelo esquemático em Protoboard

![Modelo esquemático](../arq/)

??? note "Código"
    ```c
    void setup() {
      Serial.begin(9600);
      Serial.println("Hello World!");
    }

    void loop() {

    }
    ```

??? note "Código Comentado"
    ```c
    void setup() {
      Serial.begin(9600);
      Serial.println("Hello World!");
    }

    void loop() {

    }
    ```

## Arquivos para Download

[![Arquivo ino](../arq/ino.png)](../arq/)          [![Arquivo fzz](../arq/fzz.png)](../arq/)