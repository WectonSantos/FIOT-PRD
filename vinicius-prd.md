# Product Requirements Document (PRD) - Monitoramento de Qualidade do Ar em Tempo Real

## 🎯 1. Visão Geral
* **Objetivo:** Universalizar a disponibilidade de métricas sobre a pureza do ar empregando a tecnologia LoRaWAN.
* **Público-alvo:** Pequenos empresários, a coletividade e órgãos de investigação científica.

## 🛠️ 2. Stack Tecnológica (Single Source of Truth)
* **Hardware:** Microcontrolador ESP32 com rádio LoRa nativo, integrado aos sensores BME680 e PMS5003.
* **Firmware:** Programação em linguagens C e C++.
* **Frontend:** Aplicação com painel de controle dinâmico para análise e visualização de dados.

## ✅ 3. Estado Atual do Sistema (Features Implementadas)
* [x] **Seleção de Dispositivos:** Definição de componentes de baixo custo, especificamente os modelos BME680 e PMS5003.
* [x] **Planejamento Econômico:** Detalhamento de CAPEX, OPEX e estimativa de retorno sobre o investimento.
* Ainda é preciso validar a fidelidade das leituras e, a partir disso, codificar o firmware do processador e o software de interface.

## 🚀 4. Backlog Imediato (Próximas Implementações)
1. **[Feature Atual]:** Análise técnica dos componentes e início das avaliações de acurácia.
2. **[Próxima Feature]:** Engenharia e construção do código-fonte do firmware.

## 📜 5. Regras de Ouro (Constraints)
* **Otimização de Tráfego:** Conversão mandatória de dados para formato binário (bytes) antes da transmissão para mitigar a baixa largura de banda.
* **Eficiência Energética:** O projeto deve priorizar o baixo consumo para permitir operação via células Li-Ion 18650 por vários meses.
* **Segurança de Dados:** Manter a confiabilidade do tráfego utilizando os protocolos de proteção da The Things Network.
* **Modularidade do Código:** Empregar ambientes virtuais em cada novo ciclo para garantir a organização do software.