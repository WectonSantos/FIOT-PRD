# Product Requirements Document (PRD) - Monitoramento de Qualidade do Ar em Tempo Real


## 🎯 1. Visão Geral
* **Objetivo:** Democratização do acesso de dados sobre a qualidade de ar utilizando LoraWan
* **Público-alvo:**  Microempreendededores, Sociedade e Instituições de Pesquisa

## 🛠️ 2. Stack Tecnológica (Single Source of Truth)
* **Hardware:** ESP32 com chip LoRa integrado, Sensores BME680 e PMS5003
* **Firmware:** C, C++
* **Frontend:** Software com dashboard interativo para interpretação dos dados

## ✅ 3. Estado Atual do Sistema (Features Implementadas)
* [x] **Definição do Hardware:** Foram selecionados sensores de baixo custo, BME680 e PMS5003
* [x] **Estudo Financeiro:** CAPEX, OPEX e projeção de ROI 
* Ainda é necessário testar a precisão dos sensores, e com base nisso, desenvolver o firmware que ficará dentro do microcontrolador e o software que irá exibir os dados

## 🚀 4. Backlog Imediato (Próximas Implementações)
1. **[Feature Atual]:** Estudo dos sensores, começo dos testes de precisão
2. **[Próxima Feature]:** Desenvolvivimento do firmware

## 📜 5. Regras de Ouro (Constraints)
* **Eficiência de Dados:** Sempre converter dados para bytes antes da transmissão devido à baixa largura de banda do LoRaWAN.
* **Gerenciamento Energético:** O sistema deve ser otimizado para operação via bateria (Li-Ion 18650) visando meses de autonomia.
* **Segurança:** Garantir a integridade das informações utilizando as camadas de segurança da The Things Network.
* **Escalabilidade:** Utilizar ambientes virtuais para cada novo projeto para manter a modularidade do software.
