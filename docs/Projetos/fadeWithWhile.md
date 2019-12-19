#Fade with While

Este projeto tem como objetivo demonstrar como criar o efeito de fade em leds utilizando para isso a estrutura de repetição [While](https://www.arduino.cc/reference/pt/language/structure/control-structure/while/).

## Lista de materiais

 - 1 Arduino Uno Rev 3
 - 1 Cabo USB Tipo A-B
 - 1 Led
 - 1 Resistor 220Ω

## Modelo esquemático em Protoboard

![Modelo esquemático](../arq/)

??? note "Código"
    ```c
    int led = 9;            

    void setup() {
      
        pinMode(led, OUTPUT);
    }

    void loop() {

        int intensidadeDaLuz = 0;

        while(intensidadeDaLuz <= 255){

            analogWrite(led, intensidadeDaLuz);
            intensidadeDaLuz++;
            delay(30);
        }
    }
    ```

??? note "Código Comentado"
    ```c
    int led = 9;            

    void setup() {
      
        pinMode(led, OUTPUT);
    }

    void loop() {

        int intensidadeDaLuz = 0;

        while(intensidadeDaLuz <= 255){

            analogWrite(led, intensidadeDaLuz);
            intensidadeDaLuz++;
            delay(30);
        }
    }
    ```

## Arquivos para Download

[![Arquivo ino](../arq/ino.png)](../arq/)         [![Arquivo fzz](../arq/fzz.png)](../arq/)