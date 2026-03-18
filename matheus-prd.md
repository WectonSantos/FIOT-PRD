# Product Requirements Document (PRD) - Monitoramento de Qualidade do Ar em Tempo Real

## 🎯 1. Visão Geral
* **Objetivo:** Facilitar o acesso a informações atmosféricas por meio da infraestrutura LoRaWAN.
* **Público-alvo:** Microempreendedores, sociedade civil e centros acadêmicos.

## 🛠️ 2. Stack Tecnológica (Single Source of Truth)
* **Hardware:** Placa de prototipagem ESP32 com chip LoRa, acompanhada dos módulos BME680 e PMS5003.
* **Firmware:** Baseado em C e C++[cite: 31].
* **Frontend:** Sistema com dashboard interativo focado na interpretação dos índices coletados.

## ✅ 3. Estado Atual do Sistema (Features Implementadas)
* [x] **Especificação de Hardware:** Escolha de sensores econômicos para viabilizar o projeto (BME680 e PMS5003).
* [x] **Estudo de Gastos:** Definição de custos de implementação, manutenção e projeção de lucro.
* Resta realizar os testes de precisão dos dispositivos para, em seguida, desenvolver o código interno do hardware e a ferramenta de exibição.

## 🚀 4. Backlog Imediato (Próximas Implementações)
1. **[Feature Atual]:** Estudo aprofundado dos sensores e início dos testes de calibração.
2. **[Próxima Feature]:** Desenvolvimento e deploy do firmware.

## 📜 5. Regras de Ouro (Constraints)
* **Compressão de Dados:** Transformar informações em bytes antes do envio devido às limitações de pacote da rede LoRaWAN.
* **Gestão de Energia:** Otimizar o consumo energético para uso de baterias 18650, visando autonomia de meses.
* **Integridade da Informação:** Utilizar as camadas de criptografia da The Things Network para proteger os dados.
* **Escalabilidade Técnica:** Implementar novos projetos sempre em ambientes virtuais isolados para preservar a estrutura do software.