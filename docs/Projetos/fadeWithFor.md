#Fade with For

Este projeto tem como objetivo demonstrar como criar o efeito de fade em leds utilizando para isso a estrutura de repetição [For](https://www.arduino.cc/reference/en/language/structure/control-structure/for/).

## Lista de materiais

 - 1 Arduino Uno Rev 3
 - 1 Cabo USB Tipo A-B
 - 1 Led
 - 1 Resistor 220Ω

## Modelo esquemático em Protoboard

![Modelo esquemático](../arq/)

??? note "Código"
    ```c
    int led = 10;  

    void setup() {
      
    }

    void loop() {

        int intensidadeDaLuz;

        for (intensidadeDaLuz = 0; intensidadeDaLuz <= 255; intensidadeDaLuz++) {
            analogWrite(led, intensidadeDaLuz);
            delay(30);
        }
    }
    ```

??? note "Código Comentado"
    ```c
    int led = 10;  

    void setup() {
      
    }

    void loop() {

        int intensidadeDaLuz;

        for (intensidadeDaLuz = 0; intensidadeDaLuz <= 255; intensidadeDaLuz++) {
            analogWrite(led, intensidadeDaLuz);
            delay(30);
        }
    }
    ```

## Arquivos para Download

[![Arquivo ino](../arq/ino.png)](../arq/)         [![Arquivo fzz](../arq/fzz.png)](../arq/)