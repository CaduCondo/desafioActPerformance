![JMeter Test](https://img.shields.io/badge/JMeter-5.6.3-orange)
![Status](https://github.com/CaduCondo/desafioActPerformance/actions/workflows/performance-jmeter.yml/badge.svg)

# 🚀 Desafio de Performance: BlazeDemo (JMeter)

Este repositório contém a solução do desafio técnico de performance, simulando a compra de passagens aéreas no site [BlazeDemo](https://www.blazedemo.com). O objetivo é validar a escalabilidade e o tempo de resposta do sistema sob carga.

---

## 🎯 Critérios de Aceitação (SLA)
Para aprovação, o script foi configurado para atingir os seguintes KPIs:
* **Vazão (Throughput):** 250 requisições por segundo (RPS).
* **Tempo de Resposta (90th Percentile):** Inferior a 2 segundos.

---

## 🛠️ Tecnologias Utilizadas
* **Ferramenta:** Apache JMeter 5.x
* **Linguagem:** Java 17
* **CI/CD:** GitHub Actions (Execução automatizada)
* **Hospedagem:** GitHub Pages

---

## 📂 Estrutura do Projeto
```text
├── .github/workflows/    # Configuração do Pipeline (CI/CD)
├── scripts/              # Script de teste (.jmx)
├── reports/              # Relatórios e evidências
└── README.md             # Documentação do projeto
```
---
## ⚙️ Como Executar os Testes
### 1. Via Interface Gráfica (GUI) - Apenas para validação
Abra o JMeter.

Clique em File > Open e selecione o arquivo scripts/desafioActPerformance.jmx.

Clique no botão de Play (verde) para validar o fluxo.

### 2. Via Linha de Comando (Non-GUI) - Teste Oficial
Para gerar os resultados reais sem interferência da interface, use o comando na raiz do projeto:
```bash
jmeter -n -t scripts/desafioActPerformance.jmx -l results.jtl -e -o reports/dashboard/
```

---
## 📈 Análise dos Resultados
O teste foi executado com sucesso através do GitHub Actions. Abaixo, a consolidação das métricas:
```table
Métrica             Valor Obtido    Status
Vazão (Throughput)  250+ RPS        ✅ OK
90th Percentile     < 2s            ✅ OK
Taxa de Erro        0.00%           ✅ OK
```
---

## 📊 Relatório Online (Dashboard)
Os resultados detalhados e os gráficos de performance gerados pelo pipeline de CI/CD podem ser visualizados diretamente pelo navegador:

👉 **[CLIQUE AQUI PARA ABRIR O DASHBOARD](https://caducondo.github.io/desafioActPerformance/)**
