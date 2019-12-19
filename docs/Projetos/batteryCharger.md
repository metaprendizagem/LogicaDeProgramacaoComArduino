#Batery Charger

Este projeto tem como objetivo simular de forma simples o controle de carga de uma bateria comum.

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
    const int pot = A0; 
    int valor; 

    void setup() {

      Serial.begin(9600); 
    }

    void loop() {

        valor = analogRead(pot); 
        valor = map(valor, 0, 1023, 0, 255);
        Serial.print("Valor do Potenciometro = "); 
        Serial.println(valor); 

        //Led Vermelho

        if(incomingByte >= 0 && incomingByte < 40){
            digitalWrite(vermelho, HIGH);
            Serial.println("Liga Vermelho");
        }
        else if(incomingByte >= 40 && incomingByte < 80){
            digitalWrite(vermelho, HIGH);
            Serial.println("Desliga Vermelho");
        }

        //Led Amarelo

        else if(incomingByte >= 80 && incomingByte < 120){
            digitalWrite(vermelho, HIGH);
            Serial.println("Liga Amarelo");
        }
        else if(incomingByte >= 120 && incomingByte < 160){
            digitalWrite(vermelho, HIGH);
            Serial.println("Desliga Amarelo");
        }

        //Led Verde
        
        else if(incomingByte >= 160 && incomingByte < 200){
            digitalWrite(vermelho, HIGH);
            Serial.println("Liga Verde");
        }
        else if(incomingByte >= 200){
            digitalWrite(vermelho, HIGH);
            Serial.println("Desliga Verde");
        }

        delay(250); 
    }
    ```

??? note "Código Comentado"
    ```c
    const int pot = A0; 
    int valor; 

    void setup() {

      Serial.begin(9600); 
    }

    void loop() {

        valor = analogRead(pot); 
        valor = map(valor, 0, 1023, 0, 255);
        Serial.print("Valor do Potenciometro = "); 
        Serial.println(valor); 

        //Led Vermelho

        if(incomingByte >= 0 && incomingByte < 40){
            digitalWrite(vermelho, HIGH);
            Serial.println("Liga Vermelho");
        }
        else if(incomingByte >= 40 && incomingByte < 80){
            digitalWrite(vermelho, HIGH);
            Serial.println("Desliga Vermelho");
        }

        //Led Amarelo

        else if(incomingByte >= 80 && incomingByte < 120){
            digitalWrite(vermelho, HIGH);
            Serial.println("Liga Amarelo");
        }
        else if(incomingByte >= 120 && incomingByte < 160){
            digitalWrite(vermelho, HIGH);
            Serial.println("Desliga Amarelo");
        }

        //Led Verde
        
        else if(incomingByte >= 160 && incomingByte < 200){
            digitalWrite(vermelho, HIGH);
            Serial.println("Liga Verde");
        }
        else if(incomingByte >= 200){
            digitalWrite(vermelho, HIGH);
            Serial.println("Desliga Verde");
        }

        delay(250); 
    }
    ```

## Arquivos para Download

[![Arquivo ino](../arq/ino.png)](../arq/)          [![Arquivo fzz](../arq/fzz.png)](../arq/)