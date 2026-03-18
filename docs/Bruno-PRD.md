# Product Requirements Document (PRD) - Monitoramento de Qualidade de Ar em Tempo Real

## 🎯 Visão Geral
* **Objetivo:** Coleta os dados, armazena-os e os exiba em uma aplicação para monitorar a qualidade do ar em tempo real. 
* **Público-alvo:** Pequenos empresários, marcenarias, pequenas gráficas com impressão 3D, etc.

## 🛠️ Stack Tecnológica (Single Source of Truth)
* **Firmware:** C/C++
* **Front-end:** Ferramentas que convertam os dados coletados do firmware para serem vizualidas convertidamente no mapa de calor.
* **Hardware:** ESP32, LoRa, Sensores: BME680, PMS5003

## ✅ Estado Atual do Sistema (Features Implementadas)
*(A IA deve atualizar esta lista sempre que terminar um ciclo de QA).*
* **Feature A:** Definição de quais hardwares iriam ser utilizados.
* **Feature B:** Estudo das tecnologias para o software do projeto (priorizando linguagens com o menor tempo de resposta possível).

## 🚀 Próximas Implementações (Backlog Imediato)
1.  **Feature C (Atual):** Definição das tecnologias a serem utilizadas para o software.
2.  **Melhoria D:** Início do código para os testes de precisão.

## 📜 Regras de Ouro (Constraints)
* **Filtragem de Ruído na Borda (Edge Computing):** Sensores físicos de baixo custo podem apresentar picos anômalos de leitura (ruído), para isso, é necessário aplicar métodos matemáticos para filtrar os dados e enviá-los para o software.

* **O "Elo Perdido" (Backend e Gateway):** Defina a arquitetura do Gateway (ex: The Things Network - TTN) e como os dados serão armazenados e servidos (ex: um broker MQTT e um backend leve) antes de iniciar o Front-end.

* **Otimização Extrema de Payload (Limitações do LoRa):** O ESP32 não deve enviar strings JSON formatadas. Os dados do BME680 e PMS5003 devem ser empacotados em bytes brutos (bits e bytes). A descompressão e formatação devem ser responsabilidade exclusiva do backend.

* **Resiliência a Quedas (Offline-First no Hardware):** Se o módulo LoRa perder conexão, o ESP32 deve armazenar os dados em um buffer circular local (na memória Flash ou RTC RAM) e enviá-los assim que a conexão for restabelecida, garantindo que o histórico de qualidade do ar não tenha buracos.

* **Definição Estrita de "Tempo Real" (Trade-off de Energia):** Estabeleça um intervalo de amostragem realista (ex: a cada 2 ou 5 minutos). Se houver um pico repentino de partículas, o firmware pode disparar um alerta imediato (interrupção), mas o envio de rotina deve ser espaçado.