# Escopo do Projeto — GrupoH

## Integrantes

- Sabrina Gebert - Tecnica em Eletrônica 


## Problema

 Em estufas de pintura ou limpeza de placas eletrônicas, a falta de controle automatizado gera dois riscos que podem ser críticos: a perda de qualidade do material por oscilação de temperatura/umidade e o risco de incêndio causado ao acúmulo de gases inflamáveis ​​em alta temperatura. 


## O que será monitorado

Temperatura/umidade e gases inflamáveis.



## Sensor / Dados

- Temperatura e Umidade relativa via sensor DHT22 (Faixa: 0°C a 80°C) no ESP32
- Segurança: Concentração de gases inflamáveis ​​e fumaça via sensor MQ-2 (Leitura analógica de 0 a 4095).
- LCD 1602: Leituras dos sensores utilizados e alerta de critico.


## Estrutura de Tópicos MQTT

| estufa/grupoH/ambiente/temperatura |  Temperatura atual      | ESP32 | Dashboard |    
| estufa/grupoH/ambiente/umidade     |  Umidade relativa       | ESP32 | Dashboard |
| estufa/grupoH/segurança/gas        |  Nivel_gases_detectados | ESP32 | Dashboard |
| estufa/grupoH/controle/aquecedor   |  On / Off               | ESP32 | Dashboard |
| estufa/grupoH/alerta/critico       |  Erro_e_emergencia      | ESP32 | Dashboard |


## Resultado Esperado

- Controle Automático: O sistema deve manter a temperatura entre 40°C (Ligar) e 60°C (Desligar) de forma autônoma.
- Segurança: Interrupção imediata do aquecimento caso o sensor MQ-2 detecte níveis de gás acima do limite de segurança (Set-point: 700), independente da temperatura atual.
- 0 a 300: Ar limpo (leitura de base)
- 300 a 600: Presença de nível de gases ou vapores
- 700 ou +: Indica uma concentração significativa de gases inflamáveis ​​ou fumaça.
- LCD1602: O monitoramento será feito através de um display LCD1602, que apresentará as medições dos sensores e emitirá alertas visuais imediatos sempre que uma variável atingir níveis críticos


## Hardware / Software planejado

- Publisher: [ESP32 físico / Wokwi simulado]

- Broker: Mosquitto na VPS DigitalOcean (IP: SEU_IP)

- Subscriber: [Terminal / Node-RED / outro]



## Evolução planejada

[Se houver ambição de ir além do mínimo — dashboard visual, histórico, etc.]
