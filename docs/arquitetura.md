Controle Automático: O sistema deve manter a temperatura entre 40°C (Ligar) e 60°C (Desligar) de forma autônoma.
Segurança: Interrupção imediata do aquecimento caso o sensor MQ-2 detecte níveis de gás acima do limite de segurança (Set-point: 700), independente da temperatura atual.
                * 0 a 300: Ar limpo (leitura de base)
                * 300 a 600: Presença leve de gases ou vapores
                * 700 ou +: Indica uma concentração significativa de gases inflamaveis ou fumaça.
Relé: Funciona como uma interface entre a lógica digital (3.3V) e a carga real (110V/220V), ira ligar e desligar a resistencia de aquecimento da estufa: 
                * Ligar: Quando a temperatura chegar a 40°C (nivel do gas esta seguro)
                * Desligar: Quando a temperatura atingir a meta ( Temp > 60°) ou quando o Gás ultrapassar a concentração max permitida ( interrupção de emergencia)
                * OBS: O rele sera ligado no pino NA, caso o ESP32 falhar ou perda de energia, o aquecedor seja desligado imediantamente.
