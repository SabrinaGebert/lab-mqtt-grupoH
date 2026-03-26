# Escopo do Projeto — GrupoH

## Integrantes

-Sabrina Gebert - Tecnica em Eletrônica 


## Problema

 Em estufas de pintura ou limpeza de placas eletrônicas, a falta de controle automatizado gera dois riscos que podem ser críticos: a perda de qualidade do material por oscilação de temperatura/umidade e o risco de incêndio causado ao acúmulo de gases inflamáveis ​​em alta temperatura. 


## O que será monitorado

Temperatura/umidade e gases inflamáveis.



## Sensor / Dado

Temperatura e Umidade relativa via sensor DHT22 (Faixa: 0°C a 80°C) no ESP32
Segurança: Concentração de gases inflamáveis ​​e fumaça via sensor MQ-2 (Leitura analógica de 0 a 4095).


## Estrutura de Tópicos MQTT

| estufa/grupoH/ambiente/temperatura |  Temperatura atual      | ESP32 | Dashboard |    
| estufa/grupoH/ambiente/umidade     |  Umidade relativa       | ESP32 | Dashboard |
| estufa/grupoH/segurança/gas        |  Nivel_gases_detectados | ESP32 | Dashboard |
| estufa/grupoH/controle/aquecedor   |  On / Off               | ESP32 | Dashboard |
| estufa/grupoH/alerta/critico       |  Erro_e_emergencia      | ESP32 | Dashboard |


## Resultado Esperado

[O que será visível ao final — terminal, painel, alertas]



## Hardware / Software planejado

- Publisher: [ESP32 físico / Wokwi simulado]

- Broker: Mosquitto na VPS DigitalOcean (IP: SEU_IP)

- Subscriber: [Terminal / Node-RED / outro]



## Evolução planejada

[Se houver ambição de ir além do mínimo — dashboard visual, histórico, etc.]
